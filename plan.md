
<!-- <

U+23F3 hourglass with flowing sand (⏳)
U+2614 umbrella with rain drops (☔)
U+2615 hot beverage (☕)
U+26A0 warning sign (⚠)
U+26D4 no entry (⛔)
U+2705 white heavy check mark (✅)
U+2699 gear (⚙)

U+1F4A4 sleeping symbol (💤)
U+1F4A5 collision symbol (💥)
U+1F534 large red circle (🔴)
U+1F534 large red circle (🔴)
U+1F56E book (🕮)
U+1F578 spider web (🕸)
U+1F5D1 wastebasket (🗑)
U+1F5D9 cancellation x (🗙)
U+1F6A7 construction sign (🚧)

> -->


Planteile vergangener Jahre:
[2022](old/22/plan.2022.md)


2023
====

### bis 09.01.

* ✅ Entwürfe als Vorlage speichern
* ✅ Bugfix: SVG-Zone aus Entwurf laden
* ✅ Scope-Target-Gleichsetzung (Option `targetScopeImpliesSource`)
  bei Entwürfen berücksichtigen
* ⏳ anno-frontend: Antwort auf Annotationen ermöglichen.


### bis 16.01.

* ✅ anno-frontend: Antwort auf Annotationen ermöglichen.
* ✅ Server: Antwort-Annotationen speichern
* ✅ Server: Antwort-Annotationen ausliefern können


### bis 23.01.

* ☔ Umstellung Datenformat auf `dc:title`
* ☔ Frontend Bugfixes


### bis 30.01.

* ☔ Frontend Bugfixes
* ✅ Umstellung Datenformat auf `dc:title`


### bis 06.02.

* ☔ Frontend Bugfixes
* ⏳ Frontend: Unter-Annos finden und vorerst nur chronologisch darstellen.
* ⏳ Antwort-Annotationen einreichen können
* ⏳ Bearbeiten eigener Annotationen ermöglichen.


### bis 13.02.

* ✅ Frontend: Unter-Annos finden und vorerst nur chronologisch darstellen.
  * ✅ optional doch auch verschachtelt.
* ✅ Antwort-Annotationen einreichen können (Frontend)
* ⏳ Antwort-Annotationen einreichen können (Server)
* ✅ Bearbeiten eigener Annotationen ermöglichen.
  * ✅ Bodies bearbeiten mit anno-frontend.
  * ✅ Autorenkennung wechseln mit anno-frontend.
  * ✅ ACL-Berechtigung: Revision zu eigener Annotation speichern…
    * ✅ … mit abweichenden Bodies
    * ✅ … mit abweichenden Targets
    * ✅ … mit abweichender Autorenkennung innerhalb der erlaubten eigenen


### bis 20.02.

(—)


### bis 27.02.

* ✅ Antwort-Annotationen einreichen können (Server)
* ✅ Mehr serverseitige Konsistenzprüfung für eingereichte Annotationen
* ✅ Frontend: Zone Editor: SvgSelector verwerfen, wenn er leer wäre.


### bis 06.03.

* ✅ Bearbeiten fremder Annotationen ermöglichen.
  * ✅ Bodies bearbeiten mit anno-frontend.
  * ⛔ Autorenkennung wechseln durch manuelle Eingabe der ID.
      (Zurückgestellt, weil wir es vorerst nicht brauchen.)
  * ✅ ACL-Berechtigung: Revision zu fremder Annotation speichern…
    * ✅ … mit abweichenden Bodies
    * ✅ … mit abweichenden Targets
    * ✅ … mit beliebig abweichender Autorenkennung
* ⛔ Schreibschutz für Annotationen: nur noch Moderatoren dürfen updaten.
  * Kommt bei uns hoffentlich so selten vor, dass wir es per ACL regeln
    können.


### bis 13.03.

* ✅ Fehlersuche: Antwort-Annotation fehlt in Suchergebnis.
  * Ursache war veraltete URL in importierter Annotation.
* ✅ MongoDB-Konverter: Tools für gründlichere URL-Umwandlung.
* ✅ MongoDB-Konverter: Autorennamen aus User Config übernehmen.


### bis 20.03.

* ⛔ <s>Dokumentiere PATCH-Ausrede für zwangsaktualisierte
  Autoridentität-Details.</s> (Änderung eher doch nicht verboten.)
* ✅ ACL: Dokumentiere mögliche Lizenz-Problematik bei Fremdbearbeiten.
* ⏳ Server: Stempel vergeben können


### bis 27.03.

* ✅ Server: Stempel vergeben können
  * ✅ Stempel `iana:sunset` für geplante oder nachträgliche Depublikation.
  * ✅ Stempel `dc:dateSubmitted` zur Beantragung der Freischaltung.
  * ✅ Stempel `dc:dateAccepted` zur Gewährung der Freischaltung.
* ✅ Bugfix: Einreichung von Revisionen wieder möglich


### bis 03.04.

* ✅ Frontend: Einzel-Ansicht-Modus
  * ✅ spezifische Revision anzeigen
    (Vorbereitung für bald Freischaltungs-Ansicht)


### bis 10.04.

* ✅ Frontend: Revisionen vergleichen
* ✅ Umbau der ACL-Prüfung als Vorbereitung auf Dienste mit Freischaltung
* ✅ Annos mit fehelnder Freischaltung verbergen: In der Suche.
* ✅ Einzel-Auslieferung beachtet Depublikationsdatum


### bis 17.04.

* ⏳ Freischaltung: Umsetzung in der Datenbank


### bis 24.04.

* ✅ Installation des Anno-Server vereinfachen + offizielle Anleitung


### bis 02.05.

* ✅ Stempel nochmal weitgehend umbauen wegen neuem Datenbank-Schema
  für die Freischaltung
* ✅ Suchfunktion flexibilisieren für dynamisch hinzugefügte Kriterien
    (z.B. eben Freischaltung bzw. -sanfrage)


### bis 08.05.

* ✅ Suchfunktion fragt alle Stempel ab
* ⏳ Suchfunktion: Datenbank-Abfrage modularisieren


### bis 15.05.

* ✅ Suchfunktion: Datenbank-Abfrage modularisieren
* ⏳ Depublizierte Annotationen nicht ausliefern: In Suchergebnissen

### bis 22.05.

* ✅ Depublizierte Annotationen nicht ausliefern: In Suchergebnissen
* ✅ Einzel-Auslieferung: Verweigerung mangels Freischaltung nur wenn
  alle beteiligten Dienste Freischaltung erfordern.
* ✅ Autoren sehen eigene auf Freischaltung wartende Annos.
* ✅ Suchergebnisse, die durch privilegierte Suche trotz fehlender Freischaltung
  angezeigt werden, sollen eine entsprechende Markierung tragen, und das
  Frontend sollte darauf hinweisen.
* ✅ Frontend: Einzel-Ansicht-Modus: Revisionen freischalten können.
* ✅ RSS-Feed für freizuschaltende Annotationen.


### bis 29.05.

(—)


### bis 05.06.

(—)


### bis 12.06.

* ✅ Server: Markiere Suchergebnisse, die nur aufgrund von Privilegien sichtbar
  sind, mit `{ "dc:dateAccepted": false }`.
  <small>(Proprietäre Erweiterung. Wird nur auf privilegierten Endpoints
  ausgegeben. Standard-konforme Endpoints verheimlichen solche Annotationen
  einfach.)</small>
* ✅ Frontend: Zeige, ob Annotation freigeschaltet ist oder nur aufgrund von
  Privilegien sichtbar ist.
* ✅ Frontend: Freischalten-Button funktioniert.
* ✅ Frontend: Anzeige für Autoren, wenn für ihre Annotation ein
  Freischaltungstermin in der Zukunft vorliegt. (Unser Frontend kann derzeit
  keine Freischaltung in der Zukunft, doch kann der Anschein entstehen, wenn
  die Uhrzeit des Browsers von der des Servers abweicht.)


### bis 19.06.

* ✅ Server: Verlange `as:inReplyTo`, statt Target-Art zu erraten.
* ☔ Server: Sende `as:inReplyTo` für Antworten. (Leider noch buggy.)
* ⛔ <del>Frontend: Baue Antworten-Baum mittels `as:inReplyTo`,
  statt Target-Art zu erraten.</del>
  (Basierte auf falscher Annahme. Target-Art wird sowieso nicht erraten.)
* ✅ RSS-Formatierer für Anno-Listen. (Vorbereitung für RSS Feeds.)


### bis 26.06.

* ✅ CLI Tool zum umformen von Annotationen zu Postgres-Befehlen.


### bis 03.07.

* ✅ Server sendet `as:inReplyTo` jetzt zuverlässig.
* ✅ Frontend: Sende `as:inReplyTo` bei Einreichung.
* ✅ URL-basierte Autorisierung für RSS-Feeds.


### bis 10.07.

* ✅ Server: RSS-Feed für auf Freischaltung wartende Annotationen.
* ✅ Server: Halb-geheime proprietäre Stempel ermöglichen.
  (Werden nur auf privilegierten Endpoints ausgegeben.)
* ✅ Frontend: Erteilung einer DOI manuell genehmigen können, auch ohne Antrag
  dafür. (Ein vorgelagertes Antragsverfahren können wir bei Bedarf ergänzen.)
* ✅ Frontend: DOI-Vorhersage.


### bis 17.07.

* ✅ Falsche alte Namensgebung "Slug" und Mehrdeutigkeit von "Anno ID"
  beheben: im Frontend.


### bis 25.07.

* ✅ Falsche Namensgebung … beheben: in anno-server-22.


### bis 31.07.

* ⏳ Falsche Namensgebung … beheben: im Mongo-Umwandler.


### bis 07.08.

(—)


### bis 14.08.

* ✅ Falsche Namensgebung … beheben: im Mongo-Umwandler.
* ⚙ Installation und -sanleitung testen/verbessern
* ⏳ DataCite DOI Bot Adapter


### bis 21.08.

* ⚙ Installation und -sanleitung testen/verbessern
* ⏳ DataCite DOI Bot Adapter


### bis 29.08.

* ⚙ Installation und -sanleitung testen/verbessern
* ✅ DataCite DOI Bot Adapter: Meta Data Mapping funktioniert.
* ✅ Standard-konformere Darstellung unserer Semantic Tags recherchiert.


### bis 04.09.

* ✅ Frontend: Sprach-Auswahl
* ✅ Semantic Tags umbenennen zu Semantic Links.
* ✅ Weiterleitungsziel für mit Browser abgerufene Anno konfigurierbar machen,
  insbesondere zwecks Permalink auf Kommentare.
  Digi verwendet Scope + `/` + Slug + `/image,info`.


### bis 11.09.

* ✅ Frontend: Sprache Pflichtfeld wenn Text vorhanden.
* ✅ Frontend: Sprach-Dropdown im Bootstrap-Stil.
* ✅ Frontend: Vorschau im Editor verbirgt untere Buttonbar.
* ✅ Frontend: Versionsauswahl-Dropdown durch Versionshistorie-Button ersetzt.


### bis 18.09.

* ✅ Frontend: Config + API: Letzte Rückstände des alten Begriffs "Revision"
  auf "Version" geändert.
* ⏳ Server: ACL-Prüfung für Versionshistorie
  * Auf dem Weg dahin viele neue Freischaltung-bezogene Bugs entdeckt.


### bis 25.09.

* ✅ Bugfix: Bearbeitung fremder Beiträge wieder möglich.
* Bugfix: Moderator soll nach Bearbeitung fremder Beiträge die neue Version
  sehen dürfen (v.a. zwecks dann auch freischalten).
* Server: Ablehnung wegen veraltetem `dc:replaces`-Bezug:
  Fehlermeldung soll `iana:working-copy` angeben.
* Server: Versionshistorie soll `iana:working-copy` angeben.
* ⏳ Server: ACL-Prüfung für Versionshistorie
* Server: Bei Einreichung automatisch DOI genehmigen, falls vorige Revision
  eine hatte.
  (Falls Freischaltung erforderlich ist, erteile nur bedingte Genehmigung.)
  * DOI-Automatismen per Config abschaltbar machen.


### bis 02.10.

* Latest Version Redirect soll Freischaltung und Depublikation beachten.
* Latest Version Redirect soll `working-copy` Header angeben.
* Frontend: Wenn Fehlermeldung einen `working-copy` Header hat und der vom
  eingereichten `dc:replaces` abweicht, biete an, mit geändertem `dc:replaces`
  zu wiederholen.
* Generischer DOI-Bot: Ermittelt auf DOI wartende Annotationen und reicht sie
  an Anbieter-spezifische Adapter weiter.


### bis 09.10.

* Berechtigungs-Massenabfrage im Server
* Berechtigungsvorschau im Frontend
* Prüfen: Freischaltung von Multi-Target-Annotationen nur möglich,
  wenn für alle Targets berechtigt.


### bis 16.10.

* Zusammenspiel von Frontend und DOI Bot testen/debuggen.




### später (unpriorisiert)

<details>

* Server: Prüfe, welche Anforderungen bei der Einreichung wir mittels der
  "MAY add information"-Regel oder PATCH-Ausrede lockern können, und ob
  diverse Annahme eines Datenänderungsverbots wirklich gelten.
* Muss die Einreichung Turtle-Format akzeptieren wg. LDP 5.2.3.5?
* Erforsche [Web Access Control](https://solidproject.org/TR/wac):
  ACL Standard-konformer?
* Frontend: Abruf der Versionshistorie: Antwortformat strenger prüfen,
  z.B. warnen wenn nicht AnnotationCollection oder mehrere Seiten.
* Sicherstellen, dass alle administrativen Einreichungswege (z.B. anno2pg)
  Stempel-relevante Felder wie `dc:dateAccepted` und `iana:sunset` als
  Stempel speichern statt nur in `anno_data.details`.
* Semantic Links: Prädikate vereinfachen: Anno-Model enthält `dc:` als
  Namensraum, wir brauchen da also keine vollen URLs.
* Frontend: Freitext-Schlagworte erlauben
* Frontend: Auswahl für Lizenz und Sprache nur bei Bedarf aufklappen
  (insb. wenn noch nicht gewählt), sonst zugeklappt kompakt nebeneinander.

</details>



### später (absteigende Priorität)

<details>

* Frontend: Unter-Annotationen hierarchisch darstellen mit Baumstruktur
  oben und Detail-Ansicht ausgewählter Einzelannotation darunter.
* Cron Job für Dienst-spezifische Config und ACLs synchronisieren
* Benachrichtigung für Moderatoren über Aktionsbedarf
* Benachrichtigung für Autoren über Antworten auf ihre Beiträge
* Frontend: neben GND-Schlagworten auch freie Schlagworte.
* Frontend: Verschlagwortung mit standardisierten Nicht-GND-Vorkabularen
  * z.B. Geonames
  * ggf. auch Zeitpunkte/-spannen
  * ggf. auch Geo-Koordinaten
* Server: Verbessere Container-Konformität
  * u.a. "The IRI for the Annotation MUST be the IRI of the Container with
    an additional component added to the end."
  * Sende `Accept-Post`-Header
  * LDP 5.2.3: "server-imposed constraints […] must be advertised"
* LDP 5.2.3.9: "without requiring detailed knowledge of application-specific
  constraints"
* LDP 5.2.3.4 interaction model
* LDP 5.2.8.1 link headers
* Dokumentiere potenzielle Nichterfüllung von LDP 5.2.3.2 und 5.4.2.1
  z.B. durch Erfordernis der Freischaltung, und wie man sie vermeiden kann.
* Server: Plugin-System einbauen, Kern entschlacken für Performance
  * auslagern, soweit praktikabel:
    * Debug-Module in Plugin
    * Benutzer-Datenbank
    * Revisionen-Einreichungs-Code
* Komfortable Nutzer-/ACL-Pflege per Webformular
  (damit das nicht immer IT machen muss)
* ACL: Ermittlung zusätzlicher Werk-spezifischer Metadaten aus riesigen,
  stark redundanten YAML-Dumps (DWork "sammlung" + "oaisets")
* Ordentliche ACL-Beschränkung für Abruf der Versionshistorie.
* Einreichung von Annotationen nur wenn Lizenz in Liste akzeptierter Lizenzen.
* Aus Worddatei kopierte Endnotenverlinkungen (UBHD GitLab issue #4)
* Frontend: [Software-Lizenzen maschinenlesbar ausweisen
  ](https://www.gnu.org/software/librejs/free-your-javascript.html)

</details>



zurückgestellt
==============

<details>

* Optionaler detaillierter Vergleich der Autor-Identität, falls eine
  mitgesendet wurde. Wenn sie abweicht, verweigern statt ersetzen, denn das
  könnte bei Lizenzen wie CC-BY je nach Publikum problematisch sein.
  * Wird eigentlich auch von Anno-Protocol vorausgesetzt, würde aber
    in manchen Situationen zu unnötigem Unverständnis und Aufwand bei
    den Benutzern führen.

</details>








  [anno-proto]: https://www.w3.org/TR/annotation-protocol/
