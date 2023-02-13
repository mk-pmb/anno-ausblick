
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

* ✅ Umstellung Datenformat auf `dc:title`
* ✅ Antwort-Annotationen einreichen können
* ✅ anno-frontend: Unter-Annos finden und vorerst nur chronologisch darstellen.
* Bearbeiten eigener Annotationen ermöglichen.
  * ✅ Bodies bearbeiten mit anno-frontend.
  * ✅ Autorenkennung wechseln mit anno-frontend.
  * ACL-Berechtigung: Revision zu eigener Annotation speichern…
    * … mit abweichenden Bodies
    * … mit abweichenden Targets
    * … mit abweichender Autorenkennung innerhalb der erlaubten eigenen


### bis 30.01.

* Bearbeiten fremder Annotationen ermöglichen.
  * ✅ Bodies bearbeiten mit anno-frontend.
  * Autorenkennung wechseln durch manuelle Eingabe der ID.
  * ACL-Berechtigung: Revision zu fremder Annotation speichern…
    * … mit abweichenden Bodies
    * … mit abweichenden Targets
    * … mit beliebig abweichender Autorenkennung


### bis 06.02.

* Sichtbarkeit von Annotationen einschränken:
  * Postgres Views lernen
  * "Zurückgezogen am"-Datum verbirgt Annotationen
    * erstmal manuell via Datenbank-Admin
    * mittels anno-frontend einzelne Revision
    * mittels anno-frontend optional auch alle früheren Revisionen
  * "Veröffentlichung am"-Datum zwecks Entwurf-Stadium
    * Zeitstempel 0 = noch nicht zur VÖ vorgesehen.
    * Müssen dem Autor und Moderatoren trotzdem irgendwie angezeigt werden.


### bis 13.02.

* Eingeschränkte Sichtbarkeit:
  Neue Annos von Moderatoren freischalten lassen.
* Schreibschutz für Annotationen: nur noch Moderatoren dürfen updaten.
  * Zusammen mit "Zurückgezogen am"-Datum wird daraus Möglichkeit zu
    erzwungener Depublikation.
  * Vorerst ohne Integration in anno-frontend:
    Kommt hoffentlich so selten vor, dass manuell bannen
    und in DB eintragen ausreicht.


### bis 20.02.

* Erteilung einer DOI beantragen können.
  * mit ACL-Bindung, Standard: verboten.
* DOI-Vergabe manuell genehmigen können.
  * mit ACL-Bindung, Standard: verboten.
* anno-frontend: UI für DOI-Antrag und direkt anschließende Genehmigung,
  falls Benutzer beides darf.
* Manuelle direkte DOI-Vergabe.
  * mit ACL-Bindung, Standard: verboten.


### später (absteigende Priorität)

* anno-frontend: Unter-Annotationen hierarchisch darstellen mit Baumstruktur
  oben und Detail-Ansicht ausgewählter Einzelannotation darunter.
* Cron Job für Dienst-spezifische Config und ACLs synchronisieren
* Cron Job zur Vergabe genehmigter DOIs.
* Benachrichtigung für Moderatoren über Aktionsbedarf
* Benachrichtigung für Autoren über Antworten auf ihre Beiträge
* anno-frontend: neben GND-Schlagworten auch freie Schlagworte.
* anno-frontend: Verschlagwortung mit standardisierten Nicht-GND-Vorkabularen
  * z.B. Geonames
  * ggf. auch Zeitpunkte/-spannen
  * ggf. auch Geo-Koordinaten
* Komfortable Nutzer-/ACL-Pflege per Webformular
  (damit das nicht immer IT machen muss)
* ACL: Ermittlung zusätzlicher Werk-spezifischer Metadaten aus riesigen,
  stark redundanten YAML-Dumps (DWork "sammlung" + "oaisets")
* Ordentliche ACL-Beschränkung für Abruf der Versionshistorie.
* Einreichung von Annotationen nur wenn Lizenz in Liste akzeptierter Lizenzen.
* Druckansicht für Einzelannotation
* Aus Worddatei kopierte Endnotenverlinkungen (UBHD GitLab issue #4)



zurückgestellt
==============

* Optionaler detaillierter Vergleich der Autor-Identität, falls eine
  mitgesendet wurde. Wenn sie abweicht, verweigern statt ersetzen, denn das
  könnte bei Lizenzen wie CC-BY je nach Publikum problematisch sein.









  [anno-proto]: https://www.w3.org/TR/annotation-protocol/
