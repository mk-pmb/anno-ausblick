
Sehr bald
=========

* ✅ Nur noch Standard-konforme Attribute oberster Ebene speichern.
* ✅ DOIs per Dublin-Core-Relation ausweisen.
* ✅ Antwort-Annotationen per Activity-Streams-Relation ausweisen.
* ✅ Antworten auf Antworten (… auf Antworten …) ausliefern
* ✅ Annotationen auch ohne Angabe einer genauen Revision ausliefern.
* ⛔ <s>Antwort-Annotationen in der Legacy-Suche so ausliefern,
  dass das aktuelle (2022-05-05) anno-frontend sie versteht.</s>
* ✅ Umwandlungs-Programm MongoDB &rarr; Postgres minimalistisch dokumentieren.
* 🚧 [Anno Protocol][anno-proto] lesen und vergleichen,
  wo noch Anpassungen nötig sind.
* 🚧 Sitzungsverwaltung per Shiboleth, mit Integration in anno-frontend
  * Wer bin ich und wie lange noch?
* Globale ACL: Lesezugriff und Suchergebnis-Sichtbarkeit beschränken können.
* Dienst-spezifische ACL
* Werk-spezifische ACL
* Alte Revisionen auflisten und ausliefern können.



Bald
====

* Neue Annotationen einreichen können per "händischem" HTTP.
* Multi-Target-Support beim Einreichen neuer Annotationen.
* Neu eingereichte Annotationen sofort ungeprüft veröffentlichen.
* anno-frontend soll die neue Annotationen-einreichen-API verwenden können.
* Einrichung neuer Annotationen per ACL beschränken können.
* Multi-Target-Support in anno-frontend
* anno-frontend auf neue API und dc:/as: Relationen umrüsten.



Sommer '22
==========

* Erzwinge Autoren-Kennung neu eingereichter Annotationen
  entsprechend Identität aus Sitzungsverwaltung.
  * Wenn Autor-Identität mitgesendet wurde und abweicht, verweigern.
    Nicht einfach ersetzen – wäre problematisch bei Lizenzen wie CC-BY.
* anno-frontend soll die erzwungene Autor-Identität bei Vorschau
  und Einreichung berücksichtigen.
* Bearbeiten eigener Annotationen ermöglichen.
  * mittels anno-frontend.
  * mit ACL-Bindung, Standard: verboten.
* Bearbeiten fremder Annotationen ermöglichen.
  * mittels anno-frontend.
  * mit ACL-Bindung, Standard: verboten.
* Sichtbarkeit von Annotationen einschränken:
  * Postgres Views lernen
  * "Zurückgezogen am"-Datum verbirgt Annotationen
    * erstmal manuell via Datenbank-Admin
    * mittels anno-frontend einzelne Revision
    * mittels anno-frontend optional auch alle früheren Revisionen
  * "Veröffentlichung am"-Datum zwecks Entwurf-Stadium
    * Zeitstempel 0 = noch nicht zur VÖ vorgesehen.
    * Müssen dem Autor und Moderatoren trotzdem irgendwie angezeigt werden.
    * Eigene unveröffentlichte Entwürfe "löschen" mittels zurückziehen.
* Eingeschränkte Sichtbarkeit:
  Neue Annos von Moderatoren freischalten lassen.



Herbst '22
==========

* Schreibschutz für Annotationen: nur noch Moderatoren dürfen updaten.
  * Zusammen mit "Zurückgezogen am"-Datum wird daraus Möglichkeit zu
    erzwungener Depublikation.
  * Vorerst ohne Integration in anno-frontend:
    Kommt hoffentlich so selten vor, dass manuell bannen
    und in DB eintragen ausreicht.
* Erteilung einer DOI beantragen können.
  * mit ACL-Bindung, Standard: verboten.
* DOI-Vergabe manuell genehmigen können.
  * mit ACL-Bindung, Standard: verboten.
* anno-frontend: UI für DOI-Antrag und direkt anschließende Genehmigung,
  falls Benutzer beides darf.
* Manuelle direkte DOI-Vergabe.
  * mit ACL-Bindung, Standard: verboten.
* Cron Job zur Vergabe genehmigter DOIs.
* Cron Job für Dienst-spezifische Config und ACLs synchronisieren
* Anno-Frontend: neben GND-Schlagworten auch freie Schlagworte.
* Anno-Frontend: Verschlagwortung mit standardisierten Nicht-GND-Vorkabularen
  * z.B. Geonames
  * ggf. auch Zeitpunkte/-spannen
  * ggf. auch Geo-Koordinaten









  [anno-proto]: https://www.w3.org/TR/annotation-protocol/
