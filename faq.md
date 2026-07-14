
Häufige Fragen und deren Antworten
==================================


### Aus welchen Komponenten besteht HeiANNO und wie modular sind die?

* __heiANNO__ ist das Annotationen-Projekt der Uni Heidelberg. Das ist der
  organisatorische Rahmen, in dem wir unsere Anno-Software entwickeln.

* __`anno-server-22`__ stellt die veröffentlichten Annotationen
  maschinenlesbar bereit, basierend auf einer Postgres-Datenbank.
  Er sollte mit jeder Anwendung funktionieren, die
  [Web Annotation Protocol][w3-anno-protocol] verwendet;
  Details und Einschränkungen siehe Server-Dokumentation.

* __Anno-Backend__ war der Vorgänger von `anno-server-22`. Die Software ist
  veraltet und die API wich in wichtgen Punkten von den W3-Anno-Standards ab.

* __DWork__ ist die Web-Anwendung, die auf z.B. beim
  [Klosterarchiv Lorsch][saw_mainz72_p5] das Gesamterlebnis aus Navigation,
  Metadaten, mehreren Ansichtsmodi und auch Annotationen bereitstellt.

* __Anno-Snippets in DWork__ sind der Kleber, mit dem Anno-Frontend in DWork
  eingebunden wird. Hier wird im wesentlichen konfiguriert, wo auf der Seite
  Anno-Frontend angezeigt werden soll und wie es mit anderen Modulen der Seite
  interagieren soll.

* __Anno-Frontend__ übernimmt die Darstellung der Annotationen-Spalte,
  Darstellung des inhaltlichen Teils der Einzelseiten-Ansicht,
  und es stellt auch den Annotationen-Editor bereit.

* __heiImageViewer__ ist das Modul, das in DWork die Buchseiten darstellt,
  und stellt auch den Zonen-Editor bereit. Dass wir im Anno-Editor-Dialog
  nochmal einen neuen Zonen-Editor laden, obwohl DWork die Buchseite bereits
  auf tendenziell viel größerem Raum darstellt, ist eine Besonderheit unserer
  DWork-Arbeitsweise. Der im Frontend als Normalfall vorgesehene Weg ist
  eigentlich externe Bearbeitung: Dabei verschwindet der Anno-Editor-Dialog
  und die Annotationen-Spalte geht in den Wartemodus, zeigt sinngemäß
  "Warte auf Ergebnis der externen Bearbeitung… [Abbrechen]".
  Wenn die umgebende Webseite dann das Ergebnis liefert, erscheint wieder der
  Anno-Editor-Dialog.



### Kann ich den Anno-Server und das Anno-Frontend schon ausprobieren?

Ja, die jeweiligen __staging__-Branches
([anno-server-22](https://github.com/mk-pmb/anno-server-22/tree/staging) /
[anno-frontend](https://github.com/mk-pmb/anno-frontend/tree/staging))
sind weitgehend stabil und werden nur selten zurückgespult.

Eine Installationsanleitung (Server) bzw.
Hinweise für Entwickler zum lokalen Testbetrieb (Frontend)
sind in der jeweiligen Readme verlinkt.



### Wie wird `dc:dateAccepted` benutzt?

* Dienste können für "moderierte Veröffentlichung" konfiguriert sein.
  Annotationen werden dann erst nach Freischaltung öffentlich.
* Der Stempel `dc:dateAccepted` gibt den Zeitpunkt des Inkrafttretens
  der Freischaltung an.
  * Bei Suche über einen privilegierten API Endpoint, der das
    Freischalt-Kriterium umgeht, kann das Feld auch den Wert `false` tragen,
    um anzuzeigen, dass das Suchergebnis nur durch das Privileg sichtbar ist,
    jedoch noch keine Freischaltung vorliegt.
  * Der Stempel symbolisiert eine aktive Entscheidung, die auch hätte
    ausbleiben können.
    * Während der Entwicklung überlegten wir auch, bei Diensten mit
      unmoderierter Veröffentlichung den Stempel automatisch bei
      Einreichung zu erzeugen.
      * Die Kosten für Speicherung und Übertragung der dadurch zusätzlich
        anfallenden redundanten Daten könnten für manche Benutzer durch die
        leicht gesteigerte Konsistenz des Datenmodells wettgemacht werden.
        Diese Konsistenz lässt sich bei Bedarf (&rarr; Feature Request)
        jedoch billiger herstellen, indem der Stempel dynamisch bei Abruf
        der Annotation eingefügt wird.
      * Der automatisch gesetzte Stempel wäre entweder nicht von einem aktiv
        entschiedenen Stempel zu unterscheiden, dann würden wir verwirrende
        Information speichern (schlecht).
        Oder er müsste zusätzlich noch die Info tragen, ob er automatisch
        erstellt wurde, was dann wieder unsinnig teuer erscheint im Vergleich
        zu Einfügen bei Auslieferung.
* Wozu dient ein Freischalt-Datum in der Zukunft?
  (In unserem Frontend noch nicht verfügbar.)
  * Im Fall von Publikationen mit einer Sperrfrist kann schon während der
    Sperrfrist entschieden werden. Dies erleichtert ggf. die Urlaubsplanung
    der Moderatoren.
  * Datenschutz: Eine Freischaltung jeweils zum nächsten Morgen kann helfen,
    Rückschlüsse auf die genauen Dienstzeiten von Moderatoren zu erschweren.
  * Die Funktion könnte auch zu besserer gefühlten Gleichbehandlung von
    Autoren beitragen, indem empfundene Bevorzugung durch "Vorsprung"
    weniger zum Tragen kommt.




### Was ist eine "Anno ID", "Base ID", "Slug" oder "Version ID"?

Beispiel-Adresse: `http://anno.test/annos/b98243fb~1`

* __ID__
  ist, soweit nicht anders vermerkt, jeweils die Abkürzung für "Identifier".
  Siehe auch `.id` weiter unten.
  <small>(In Quellcode bitte nicht mit `idx` = index verwechseln.)</small>

* (veraltet) __Slug__
  war in alten Versionen unserer Anno-Software die Bezeichnung für den
  individuellen Teil der URL einer Annotation.
  Es ist [ein Fachbegriff aus der Suchmaschinen-Optimierung][wp-seo-slug],
  der besagt, dass der Identifier mit menschenlesbaren Stichworten
  angereichert ist, oft eine Variante der Überschrift.
  In diesem Sinne wird er auch in
  [Annotation Protocol Kap. 5.2][anno-proto-slug]
  verwendet, zwecks Vorschlag in der Einreichung,
  was unsere Software allerdings nicht anbietet.
  Vielleicht war das mal geplant; jedenfalls fand es nicht statt,
  und somit ist der Begriff nicht mehr angemessen. Wir verwenden daher
  in neueren Version stattdessen "Version Identifier".

* (veraltet) __Revision(snummer)__
  war in früheren Versionen unserer Anno-Software die Bezeichnung für die
  Versionen einer Annotation bzw. den Bearbeitungszähler, beginnend bei
  Nummer 1. Dies konnte zu Verwirrung führen, da es auch den Sprachgebrauch
  gibt, die erste Version "Originalfassung" oder "Erstveröffentlichung" zu
  nennen, und erst die zweite Version eine (die erste) "Revision" zu nennen.

* __Anno ID__ / Annotation Identity:
  Eine (meist vollständige, selten auch relative) URL/IRI einer Annotation,
  im Sinne der Definition des Feldes `id` nach [Anno Model][w3-anno-model]
  Kapitel 3.1. "ID" ist demnach hier die Abkürzung für "Identity".
  In der Beispiel-Adresse ist die Anno ID die gesamte Adresse.

* __Anno Namespace URL__:
  URL des Namensraumes für Annotationen eines bestimmten Anno Servers.
  Somit der nicht-individuelle Anfangsteil aller Anno IDs dieses Servers.
  Endet immer auf einen Schrägstrich.
  In der Beispiel-Adresse ist die Anno Namespace URL: `http://anno.test/annos/`

* __Version Identifier__:
  Eindeutige Bezeichnung einer speziellen Version einer Annotation.
  Darf keinen Schrägstrich enthalten.
  In der Beispiel-Adresse ist der Version Identifier: `b98243fb~1`

* __Base ID__ / Lineage Identifier:
  Der Versions-übergreifend die Annotation bezeichnende Anteil des
  Version Identifiers.
  In Kontexten, in denen "Base" mehrdeutig wäre, oder mehr auf die Abstammung
  späterer Versionen von vorherigen abgezielt wird statt auf die reine Syntax,
  kann dieser Teil auch "Lineage Identifier" genannt werden.
  In der Beispiel-Adresse ist die Base ID: `b98243fb`

* __Versionsnummer__:
  Eine Nummerierung, die angibt, die wie vielte "Auflage" einer Annotation
  bezeichnet wird. Die Zählung beginnt immer bei 1, und jede neu eingereichte
  Überarbeitung der Annotation erhält eine ganzzahlige Nummer, die höher ist
  als alle bisher für diese Annotation verwendeten Versionsnummern.
  (Lücken sind möglich, insbesondere durch nachträgliche Depublizierung.)
  In der Beispiel-Adresse ist die Versionsnummer: `1`

* __Versionsnummertrennzeichen__ / Version Number Separator:
  Ein Zeichen, das Base ID und Versionsnummer voneinander trennt.
  Wir verwenden dafür U+007E Tilde (`~`).
  In der Beispiel-Adresse ist das Versionsnummertrennzeichen: `~`
  * Ausnahme: In DOIs verwenden wir statt der Tilde meistens
    U+005F Low Line (_). Diese Tradition entstand, weil ein früher von uns
    eingesetzter DOI-Registrar die Tilde nicht zuließ.

* __.id__
  Sollte in Bezug auf (Versionen von) Annotationen wegen seiner
  Verwechselungsgefahr nur benutzt werden, wenn die Vorgaben eines Standards
  es erfordern.
  * Insbesondere sollte ein Version Identifier immer im Feldnamen selbst
    als solcher bezeichnet werden, damit man sich im Umkehrschluss darauf
    verlassen kann, dass ein Ausdruck wie `version.id` das `id`-Feld
    (gemäß [Anno Model][w3-anno-model]) der Version bezeichnet und somit
    eine Anno ID darstellt, d.h. potenziell eine absolute URL.



### Warum greift der DOI-Bot nicht direkt auf die Datenbank zu?

* Die Beschränkung auf die öffentlich abrufbaren Annotations-Schnittstelle
  als Datenquelle für den DOI-Bot ist eine Datenschutzmaßnahme, die auf
  einfache Weise sicherstellt, dass als Metadaten für die DOI ausschließlich
  Daten verwendet werden, die sowieso öffentlich abrufbar wären.
  * Jedes Fehlerpotenzial durch zwischen DOI-Bot und `anno-server-22`
    abweichende Berechtigungs-Konfiguration wird dadurch vermieden.
* Die Beschränkung auf Stempelung per HTTP PATCH zwecks Speicherung der
  vergebenen DOIs ist eine Sicherheitsmaßnahme, die das Schadenspotenzial
  eines fehlfunktionierenden (inklusive unerlaubt fremdgesteuerten) DOI-Bots
  reduziert (Principle of least privilege).
  * Insbesondere wird so vermieden, dem DOI-Bot Datenbank-Zugangsdaten
    hinterlegen zu müssen, mit denen bei alltagsüblichen Konfigurationen
    wesentlich mehr Schaden möglich wäre als nur die Eintragung fiktiver DOIs.
  * Die Autorisierung mittels unbewiesener Behauptung eines Benutzernamens
    innerhalb eines von Docker geschützten virtuellen Netzwerks nutzt exakt
    die von `anno-server-22` auch für menschliche Moderatoren vorgesehene
    Autorisierung, sodass durch den DOI-Bot keine zusätzliche Angriffsfläche
    entsteht.



### Wie groß dürfen Annotationen sein?

* Der Anno Server hat keine absichtliche Beschränkung, es gibt aber ein paar
  technische Randbedingungen:
  * Die Web API hat ein Upload Limit, das mit der Option `upload_size_limit`
    festgelegt werden kann. Der Standardwert beträgt 1 MB (Stand 2024-10-22).
  * Spätestens ab 8 KB muss Postgres die [Toast-Technik][pg-toast] anwenden.
    Die funktioniert transparent und üblicherweise auch sehr performant,
    dennoch kann das ein Anreiz sein, Annotationen deutlich kleiner zu halten.
  * Wenn Annotationen mehrere KB groß werden, enthalten sie möglicherweise
    im Text versteckte Rohdaten.
    [Davon raten wir grundsätzlich ab.](inline_blobs_are_bad.de.md)












  [pg-toast]: https://www.postgresql.org/docs/current/storage-toast.html
  [saw_mainz72_p5]: https://archivum-laureshamense-digital.de/view/saw_mainz72/0005/
  [w3-anno-model]: https://www.w3.org/TR/annotation-model/#annotations
  [w3-anno-protocol]: https://www.w3.org/TR/annotation-protocol
  [wp-seo-slug]: https://en.wikipedia.org/wiki/Slug_(web_publishing)





