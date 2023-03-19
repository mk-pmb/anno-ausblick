
<!-- <

U+23F3 hourglass with flowing sand (⏳)
U+2614 umbrella with rain drops (☔)
U+2615 hot beverage (☕)
U+26A0 warning sign (⚠)
U+26D4 no entry (⛔)
U+2705 white heavy check mark (✅)

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


2022
====

### Sommer

* ✅ Nur noch Standard-konforme Attribute oberster Ebene speichern.
* ✅ DOIs per Dublin-Core-Relation ausweisen.
* ✅ Antwort-Annotationen per Activity-Streams-Relation ausweisen.
* ✅ Antworten auf Antworten (… auf Antworten …) ausliefern
* ✅ Annotationen auch ohne Angabe einer genauen Revision ausliefern.
* ⛔ <s>Antwort-Annotationen in der Legacy-Suche so ausliefern,
  dass das aktuelle (2022-05-05) anno-frontend sie versteht.</s>
* ✅ Umwandlungs-Programm MongoDB &rarr; Postgres minimalistisch dokumentieren.
* ✅ Sitzungsverwaltung per Shiboleth, mit API-Endpunkt für anno-frontend.
  * ✅ Wer bin ich und wie lange noch?
* ✅ Globale ACL: Lesezugriff und Suchergebnis-Sichtbarkeit beschränken können.
* ✅ Dienst-spezifische ACL
* ✅ Werk-spezifische ACL
* ✅ Bei Abruf einer Einzelannotation mit bevorzugtem Antwort-Typ HTML,
  leite auf erste Target Scope URL weiter.


### nebenher

* 🚧 [Anno Protocol][anno-proto] lesen und vergleichen,
  wo noch Anpassungen nötig sind.


### bis 10.10.

* ✅ Alte Revisionen auflisten und ausliefern können.
  ([Diskussion: Welche property verwenden?](
  https://github.com/w3c/web-annotation/issues/446 ))
* ✅ Neue Annotationen einreichen können per "händischem" HTTP.
  * ✅ Einreichung neuer Annotationen per ACL beschränken können.
  * ✅ Datenformat der eingereichten Annotation grob prüfen.
  * ✅ Neu eingereichte Annotationen sofort ungeprüft veröffentlichen.
* ✅ Erzwinge Autoren-Kennung neu eingereichter Annotationen
  entsprechend Identität aus Sitzungsverwaltung.
* ✅ Optionale Fallback-Autoren-Kennung, wenn keine mit eingereicht wurde.
  * ✅ Risiken dokumentieren


### bis 17.10.

* ✅ Standard-konforme Suche nach eingeschränktem Target URL Präfix.
* ✅ anno-frontend soll Ober-Annotationen anhand der neuen Suche finden
  und vorerst ohne Unter-Annotationen darstellen.


### bis 24.10.

(—)


### bis 31.10.

(—)


### bis 07.11.

* ✅ Alte JWT-basierte Pseudo-Sessions entsorgen.
* ✅ anno-frontend soll die Sitzungs-Identität und -Restzeit darstellen.
* ✅ anno-frontend soll erlaubte Autor-Identitäten zur Auswahl anbieten.
  * ⛔ <s>und sich die zuletzt benutzte merken</s>
    * komplexer als erwartet, und scheint nicht wichtig &rArr; vertagt.
* ✅ anno-frontend soll die neue Annotationen-einreichen-API verwenden können.
* ✅ anno-frontend soll die Autor-Identität bei der Vorschau berücksichtigen.


### bis 14.11.

* ✅ Multi-Target-Support beim Einreichen neuer Annotationen.
* ✅ Multi-Target-Support in anno-frontend: UI-Konzept
* ✅ Entwürfe im Frontend: UI-Konzept


### bis 21.11.

* ⏳ Entwürfe im Frontend: einbauen
* ⏳ Multi-Target-Support in anno-frontend: einbauen.


### bis 28.11.

* ✅ Entwürfe im Frontend: einbauen


### bis 05.12.

* ✅ Entwürfe-Gruppierung nach Ähnlichkeit des Untersuchungsobjekts
* ✅ Entwürfe löschen können
* ⏳ Eigene Entwurfsbezeichnung

### bis 12.12.

* ✅ Eigene Entwurfsbezeichnung
* ✅ Entwürfe-UI verbessern


### bis 19.12.

* ✅ Multi-Target-Support in anno-frontend: einbauen.



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
* 🚧 MongoDB-Konverter: Autorennamen aus User Config übernehmen.


### bis 20.03.

* Dokumentiere PATCH-Ausrede für zwangsaktualisierte Autoridentität-Details.
* ACL: Dokumentiere mögliche Lizenz-Problematik bei Fremdbearbeiten.
* Server: Stempel vergeben können
  * Stempel `iana:sunset` für geplante oder nachträgliche Depublikation.
  * Stempel `dc:dateSubmitted` zur Beantragung der Freischaltung.
  * Stempel `dc:dateAccepted` zur Gewährung der Freischaltung.
* Sichtbarkeit von Annotationen einschränken:
  * Dienst-spezifische Option "Freischaltung erforderlich"


### bis 27.03.

* Server: Verlange `as:inReplyTo`, statt Target-Art zu erraten.
* Server: Sende `as:inReplyTo` für Antworten, zwecks Performance-Optimierung
  in unserem Frontend.
* MongoDB-Konverter: Benutze `as:inReplyTo` für Antworten.
* Server: Dienst-spezifisch nur freigeschaltete Annotationen ausliefern.
* Frontend: Einzel-Ansicht-Modus
  * spezifische Revision anzeigen
    (Vorbereitung für bald Freischaltungs-Ansicht)
  * Revisionen vergleichen


### bis 03.04.

* Frontend: Einzel-Ansicht-Modus: Revisionen freischalten können.
* RSS-Feed für freizuschaltende Annotationen.
* Frontend: Baue Antworten-Baum mittels `as:inReplyTo`,
  statt Target-Art zu erraten.


### bis 10.04.

* Erteilung einer DOI beantragen können.
* DOI-Vergabe manuell genehmigen können.
* Manuelle direkte DOI-Vergabe.
* Frontend: UI für DOI-Antrag und direkt anschließende Genehmigung,
  falls Benutzer beides darf.


### bis 17.04.

* Berechtigungs-Massenabfrage im Server
* Berechtigungsvorschau im Frontend


### später (unpriorisiert)

* Server: Plugin-System einbauen, Kern entschlacken für Performance
  * auslagern, soweit praktikabel:
    * Debug-Module in Plugin
    * Benutzer-Datenbank
    * Revisionen-Einreichungs-Code
* Erforsche [Web Access Control](https://solidproject.org/TR/wac):
  ACL standard-konformer?


### später (absteigende Priorität)

* Frontend: Unter-Annotationen hierarchisch darstellen mit Baumstruktur
  oben und Detail-Ansicht ausgewählter Einzelannotation darunter.
* Cron Job für Dienst-spezifische Config und ACLs synchronisieren
* Cron Job zur Vergabe genehmigter DOIs.
* Benachrichtigung für Moderatoren über Aktionsbedarf
* Benachrichtigung für Autoren über Antworten auf ihre Beiträge
* Frontend: neben GND-Schlagworten auch freie Schlagworte.
* Frontend: Verschlagwortung mit standardisierten Nicht-GND-Vorkabularen
  * z.B. Geonames
  * ggf. auch Zeitpunkte/-spannen
  * ggf. auch Geo-Koordinaten
* Komfortable Nutzer-/ACL-Pflege per Webformular
  (damit das nicht immer IT machen muss)
* ACL: Ermittlung zusätzlicher Werk-spezifischer Metadaten aus riesigen,
  stark redundanten YAML-Dumps (DWork "sammlung" + "oaisets")
* Ordentliche ACL-Beschränkung für Abruf der Versionshistorie.
* Einreichung von Annotationen nur wenn Lizenz in Liste akzeptierter Lizenzen.
* Aus Worddatei kopierte Endnotenverlinkungen (UBHD GitLab issue #4)
* Frontend: [Software-Lizenzen maschinenlesbar ausweisen
  ](https://www.gnu.org/software/librejs/free-your-javascript.html)




zurückgestellt
==============

* Optionaler detaillierter Vergleich der Autor-Identität, falls eine
  mitgesendet wurde. Wenn sie abweicht, verweigern statt ersetzen, denn das
  könnte bei Lizenzen wie CC-BY je nach Publikum problematisch sein.
  * Wird eigentlich auch von Anno-Protocol vorausgesetzt, würde aber
    in manchen Situationen zu unnötigem Unverständnis und Aufwand bei
    den Benutzern führen.









  [anno-proto]: https://www.w3.org/TR/annotation-protocol/
