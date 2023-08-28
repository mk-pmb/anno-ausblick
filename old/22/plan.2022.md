
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



