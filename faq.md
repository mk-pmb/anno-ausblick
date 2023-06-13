
Häufige Fragen und deren Antworten
==================================


### Kann ich den Anno Server schon ausprobieren?

Ja, der [staging branch](https://github.com/mk-pmb/anno-server-22/tree/staging)
beinhaltet schon die meisten wichtigen Features.
Eine Installationsanleitung ist in der Readme verlinkt.




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













