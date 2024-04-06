
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
[2023](old/23/plan.2023.md)


2024
====

### bis 08.01.

* ✅ Generischer DOI-Bot: Ermittelt auf DOI wartende Annotationen und reicht sie
  an Anbieter-spezifische Adapter weiter.
  * ✅ DOI-Bot funktioniert mit Dummy-Debug-Adapter


### bis 15.01.

* ✅ DOIs veröffentlichen (statt nur Draft speichern).
* ✅ DOI-Bot ignoriert jetzt Lücken in der Versionshistorie.
* ✅ DOI-Bot beschwert sich jetzt wenn der RSS Feed kaputt ist
  (z.B. weil Anno Server noch nicht gestartet).
* ✅ DOI-Bot sammelt einen kumulativen "fail score" über mehrere Botläufe
  hinweg, und resetet ihn bei erfolgreichem Botlauf.
* ✅ DOI-Bot startet jetzt automatisch neu und wartet dann erstmal.
* ✅ DOI-Bot Logs zeigen jetzt an relevanten Stellen Datum und Zeit.


### bis 22.01.

* ✅ Bessere Tests und Debug-Tools für den DataCite-Adapter
* ☔ DataCite API debuggen
* ✅ Server: Bei DOI-Stempelung, lösche den DOI-Bedarf-Stempel.
* ✅ DOI-Bot: Installationsanleitung


### bis 29.01.

* ✅ Bugfix: Moderator soll nach Bearbeitung fremder Beiträge die neue Version
  sehen dürfen (v.a. zwecks dann auch freischalten).
* ✅ DOI Bot: Bei Annos, die schon eine DOI haben, die alte DOI (mit ggf.
  noch Tilde) verwenden.
* ✅ DOI für Latest Version Redirect registrieren funktioniert testweise im
  DataCite-Adapter.
* ✅ DOI Bot: doppelte Absicherung: Abbruch, wenn die zu updatende DOI von in
  Anno deklarierter (schon vorhandener) DOI abweicht.
* ✅ Server: Installationsanleitung verbessert
* ✅ Neu registrierte DOIs aufstempeln funktioniert seitens DOI-Bot,
  * ☔ aber der Server verweigert (neuer ACL Bug).


### bis 05.02.

(–)


### bis 12.02.

* ✅ ACL-Bug beim DOI aufstempeln debuggt


### bis 19.02.

* ✅ Server: Bei Einreichung automatisch DOI genehmigen, falls vorige Revision
  eine hatte.
  * ✅ DOI-Automatismen per Config abschaltbar machen.


### bis 26.02.

* ✅ Server: Config-Mechanismus zur Einbindung beliebiger Zusatzdaten
* ✅ Server: Doku für neues ACL-Konzept


### bis 04.03.

* ✅ Neue ACL-Features (Schleifen + Zusatzdaten laden) funktionieren.
* ✅ Frontend: Planung für neuen Zoneneditor
* ✅ Frontend zur testweisen Einbindung eines externen
  Zoneneditors vorbereitet.


### bis 11.03.

* ✅ Bugfixes in neuen ACL-Beispieldateien
* ✅ DOI-Bot: Informativere Fehlermeldungen


### bis 18.03.

* ✅ DOI-Bot: RSS-Suche über Docker-internes Netzwerk
* ✅ DOI für Latest Version Redirect registrieren/updaten
* DOI-Bot: Erfolgs- und Fehlerberichte als RSS ausgeben.


### bis 25.03.

* Frontend: Berechtigungsvorschau
* Doku: Übersicht der Konfigurationsmöglichkeiten



### nahe Zukunft

* Prüfen: Freischaltung von Multi-Target-Annotationen nur möglich,
  wenn für alle Targets berechtigt.
* Zusammenspiel von Frontend und DOI Bot testen/debuggen.




### später (unpriorisiert)

<details>

* Frontend: Versionshistorie: Schloss in Auswahlliste wenn widerrufen.
* Frontend: Versionshistorie: Zeige Bearbeiten-Schltfläche nur für neueste.
* Frontend: Debug: Zalgo bearbeiten können solange noch nicht freigeschaltet.

* Postgres-Adaper: Umhülle mehrteilige Datenbank-Interkationen mit
  [Transaktionen](https://node-postgres.com/features/transactions).
* Server: Versionshistorie soll `iana:working-copy` angeben.
  (Größere Tüftelei: Wie ins MultiSearch SQL einschieben damit geschickt?)
  * Auch Suchergebnisse für Autoren sollen `iana:working-copy` angeben.
* Frontend: Wenn Fehlermeldung einen `working-copy` Header hat und der vom
  eingereichten `dc:replaces` abweicht, biete an, mit geändertem `dc:replaces`
  zu wiederholen.


* Server: Prüfe, welche Anforderungen bei der Einreichung wir mittels der
  "MAY add information"-Regel oder PATCH-Ausrede lockern können, und ob
  diverse Annahme eines Datenänderungsverbots wirklich gelten.
* ACL: Können wir mehrere Targets und Privilegien im selben Durchgang prüfen?
* ACL: Können wir machen, dass für Versionshistorie in Freischalt-Ansicht
  Freischaltberechtigung auf ein einziges Target ausreicht?
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

* [Annotorious](https://annotorious.github.io/) erkunden

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
* Server: Abruf der "aktuelle Version"-URL mit Header `Accept-Datetime`
  soll den Suchzeitraum einschränken.
* Server: Header `Accept-Datetime` für Suche nach Subject Target URL

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
