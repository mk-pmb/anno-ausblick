﻿
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
* ✅ Bugfix: Frontend: Versionsauswahländerung und ihr Hook funktionieren
  wieder auch für den neueste-Version-Eintrag.
* ⏳ Suchergebnisse debuggen: Anscheinend sickern Daten von nicht
  freigeschalteter Version durch?


### bis 02.10.

* ✅ Server Bugfix: Verabsolutiere bei Einreichung relative URLs in vielen
  Feldern. (Relevant v.a. beim Import von Test Fixtures.)
* ✅ Server Bugfix: Dangling Promise bei ACL-Prüfung für Einzelannotation.
* ✅ Server: Ablehnung wegen veraltetem `dc:replaces`-Bezug:
  Fehlermeldung soll `iana:working-copy` angeben.


### bis 09.10.

* ✅ Doku: FAQ: Warum greift der DOI-Bot nicht direkt auf die Datenbank zu?
* ✅ Server Bugfix: Datenbank-Schema auf Multi Target Annos angepasst.
* ✅ Frontend: pURL-Button ausblenden wenn DOI vorhanden.
* ✅ Frontend: Weise auf ggf. weitere Untersuchungsgegenstände hin.
* ✅ Frontend: Einzelansicht: Zeige ggf. Link zu beantworteter Annotation.


### bis 16.10.

* ✅ Neues Freischaltung-Konzept: "Freischaltung fehlt"-Stempel bei Einreichung
  wenn der Dienst es vorsieht, und unterbleibt bei unmoderierten Diensten.
  * ✅ Automatische Stempelung bei Einreichung funktioniert.
  * ✅ Einzelabruf beachtet den "Freischaltung fehlt"-Stempel.
  * ✅ Bei mangels Freischaltung verweigertem Einzelabruf werden die Header
    "Version-History" und "Latest-Version" mitgesendet, damit man eine
    Chance hat, eine frühere Version zu entdecken.


### bis 23.10.

* ✅ Suche funktioniert mit neuem Freischalt-Ansatz.
* ✅ Frontend: Debug Panel zeigt wieder auch proprietäre Felder.
* ✅ Frontend: DOI-Button zeigt, ob echte DOI oder nur Vorschau.
* ✅ RSS für auf Freischaltung wartende Annos ist umgestellt.
* ✅ Stempel haben Effekt-Einhängepunkte zur Vor- und Nachbereitung.


### bis 30.10.

(—)


### bis 06.11.

* ✅ Bugfix: Öffentlicher Endpunkt verheimlicht nicht freigeschaltete
  Einzelannos wieder.
* ✅ Neue proprietäre API zum Abruf nicht freigeschalteter Einzelannos.
  * ✅ Frontend: Freischalt-Ansicht auf die neue API umrüsten.


### bis 13.11.

* ✅ Latest Version Redirect soll Freischaltung und Depublikation beachten.
* ✅ Latest Version Redirect soll `working-copy` Header angeben.
* ✅ Server: Versionshistorie auf neue Freischaltung umrüsten
* ✅ Versions-Historie im Frontend reparieren
* ✅ Stempel-Effekte für Freischaltung implementieren



### Jahresbericht-Eckpunkte

* Verbesserungen bei Entwürfen und Multi-Target-Annotationen
* Antworten auf Annotationen
* Annotationen bearbeiten
* weitere Verbesserung der Standardkonformität
* Freischaltung und nachträgliche Depublikation
* Einzelansicht-Modus, u.a. zwecks Druckansicht
* Installation des Servers vereinfacht und Anleitung dafür erstellt
* Datenbank-Imoport-Tool (anno.json &rarr; Postgres)
* Vorbereitungen für DOI-Vergabe, DOI-Bot angefangen
* Sprachauswahl für Annotationen
* Fehlerbehebungen

<!-- Eingereicht 2024-02-01 -->










