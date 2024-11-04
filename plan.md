
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


### bis 25.03.

* ✅ DOI-Bot: Erfolgs- und Fehlerberichte als RSS ausgeben.
* ✅ Frontend: Berechtigungsvorschau


### bis 01.04.

(–)


### bis 08.04.

* ✅ Anno-Suche: Stoppuhr zur Untersuchung langsamer Antworten
* ✅ Server loggt jetzt mit Zeitstempeln.
* ✅ Frontend Doku: Wann und warum muss man Target nachjustieren?
* ✅ Doku: Übersicht der Konfigurationsmöglichkeiten
* ✅ Doku: Übersicht aller unterstützter ACL-Privilegien
* ✅ anno-mongo2postgres: Verwende Autor-Identitäten aus alter users.yml
* ✅ anno-mongo2postgres: Antwort-Verschachtelung wiederherstellen
* ✅ Konfig-Migrator für alte users.yml


### bis 15.04.

* ✅ Anno- und Konfig-Migrator auf Testserver installiert.
* ✅ Anno-Migrator verwirft jetzt ungültige URNs.
* ✅ Server: Diverse Bugs in Version History gefixt.
* ✅ Shibbolet/Proxy-Beispiel Hinweis: benötigt Apache Modul allowmethods
* ✅ DevDock Config: Syntaxfehler behoben, /app-Fehler erklärt.


### bis 22.04.

* ✅ Prüfen: Freischaltung von Multi-Target-Annotationen nur möglich,
  wenn für alle Targets berechtigt.
* ✅ Zusammenspiel von Frontend und DOI Bot testen/debuggen.
* ✅ Bugfix: Server: Revision auch über Autor-Endpunkt zulassen.
* ✅ Frontend: Versionshistorie: Zeige Bearbeiten-Schaltfläche nur für neueste.
* ✅ Cron Job: Digi-Metadaten updaten


### bis 29.04.

* ✅ Server Config: Vererbung auch für Services eingebaut
* ✅ Testprojekt für Mirador 3 aufgesetzt
* ✅ Vorarbeiten für Anno-Ausgabe im IIIFv3-Format


### bis 06.05.

* ✅ Mongo-Konverter auf manuellen Download der DOI-Liste umgebaut
* ✅ Skript zur Korrektur der Redirect URLs bestehender DOIs


<!-- 13. bis 27.5. ohne wesentliche Neuerungen: Urlaub, Feiertage,
  dann versuchter Umstieg auf neue Anno-Server-Version. -->


### bis 03.06.

* ✅ GitHub-Repos auf UBHD-Account umgebaut
* ✅ Progressive Migration für Mongo-Konverter
* ✅ DOI-Bot-Option `anno_doi_versep_exceptions` für `_` vs. `~`


### bis 10.06.

* ✅ Mongo-Konverter weiter verbessert
* ✅ DOI-Bot: Bessere Fehlermeldung, wenn eine Anno "HTTP/410 Gone" ist.


### bis 17.06.

* ✅ mongo2pg: Linking bodies ohne source werden jetzt zu TextualBodies
* ✅ DOI-Bot Version Separator Exceptions repariert
* ✅ DOI-Bot ignoriert zurückgezogene Annos jetzt resilienter


### bis 24.06.

* ✅ Frontend: Buttons reparieren
* ✅ Frontend: Viewer: Standardkonforme Links und Schlagworte anzeigen können
* ✅ Revisionen einreichen auch solange Vorversion noch nicht freigeschaltet


### bis 01.07.

* ✅ Bugfix für Suche im Gastmodus
* ✅ Frontend: Editor: Erzeuge Links und Schlagworte standardkonform.
* ✅ HeiImageDraw ausprobiert


### bis 08.07.

* ✅ Benutzerdefinierter IP Range für Docker Bridge
* ✅ Revisionen erben Creator-Feld aus Initialversion


### bis 15.07.

* ✅ Anno-Snippet refactored


### bis 22.07.

* ✅ mongo2pg: Mehr kaputte Bodies repariert
* ✅ mongo2pg + Server: Unicode combining characters normalisieren


### bis 29.07.

* ✅ mongo2pg: HTML Bodies weiter aufräumen.
* ✅ Frontend: HTML-Editor: unnütze Formatierungen abschalten.
* ✅ Server: Provisorische HTML-Entschärfung für eingereichte Annotationen.


### bis 06.08.

* ✅ Server: ACL-Preview auch wenn Suchergebnis leer
* ✅ Server: Login Session Redirect
* ✅ Frontend: Warte-Modus für externen Target-Editor außerhalb
* ✅ Frontend: Editor-Tab für externen Target-Editor


<!-- … Urlaub … -->

### bis 23.09.

* ✅ DOI-Bot Cron Task repariert


### bis 30.09.

* ✅ DOI-Bot kann DOIs für Anno-Versionen vervollständigen
* ✅ Frontend: Konflikt zwischen HTML-Editor und -Sanitizer debuggen:
  Problem reproduziert.
  <!-- Mongo-Dump 2024-05-28, Anno BoapBOs3S-urC58dHJ6Ivg -->


### bis 07.10.

* ✅ Server: Bugfix: Gäste sehen anonyme nicht-freigeschaltete Annos nicht mehr.
* ✅ Server: HTTP-konforme Fehlermeldung wenn eingereichte Anno zu groß.
* ✅ Server: Upload Size Limit konfigurierbar machen.


### bis 14.10.

* ✅ Frontend: HTML-Editor-Modul komplett refactoren, damit es sich dem
  Anno-Editor passiv unterordent. (Statt mit eigenen Event Hooks aktiv
  den HTML Sanitizer zu sabotieren.)


### bis 21.10.

* ✅ Frontend: Position der HTML-Editor Popups reparieren
* ✅ Frontend: Neues HTML-Editor-Modul anbinden.
* ✅ Frontend: Sanitizer wird nicht mehr bei jeder Änderung im HTML-Editor
  sofort aufgerufen, sondern erst, wenn eine Benutzeraktion (z.B. Vorschau,
  Entwurf speichern, Einreichen) es erfordert.
* ✅ Frontend: Debug-Panel kann anzeigen, was der HTML Sanitizer geändert hat.


### bis 04.11.

* ✅ Frontend: Kleinere UI-Optimierungen
* ✅ Server Bugfix: DOI-Bot-RSS-Fehler
* ✅ Server Bugfix: URL-Target in Resource umwandeln zwecks Metadaten-Zuweisung
* ✅ Server: Eindeutige Ref-Nummer für zensierte Fehlermeldungen


### bis 11.11.

* Server: Legacy Endpoint, der `dc:title` im `body` mit ausgibt.
* Annotationen mit IIIF v3 kompatibel machen,
  Mirador 3 Zonendarstellung erforschen.
  * IIIF hat auch "Annotation" aber die projizieren Bilder auf Canvases.
  * IIIF v2 ignorieren.


### bis 18.11.

* Doku: Docker Images updaten (Mails vom 2024-08-20 früh.)
* Doku: Privilege Escalation durch Docker Templates vermeiden
  <!-- (
  Wenn ein Docker-berechtigter Benutzer Docker Templates aus einem für annsrv
  schreibbaren Verzeichnis verwendet, kann das für Privilege Escalation genutzt
  werden. &rArr; Tutorial für wie man ein statisches Compose File auf einem
  Staging-System generiert und aufs Produktivsystem kopiert.
  ) -->
* Frontend: DOI-Vorschau soll Kleinbuchstaben zeigen
* Frontend: Freitext-Schlagworte ermöglichen


### bis 25.11.

* Upgrade postgres auf v16.
* Inline Blobs (Bild/Video) im Body verbieten
* Leere `alt=`-Attribute aus `img`-Tags entfernen
* DOI-Bot: "latest"-Log möglichst erst nach Rerun-Wartezeit drehen.
* Suchergebnisse nach Datum (wenn vorhanden, des VÖ-Stempels) sortieren!
  besonders bei RSS.









### nahe Zukunft

* Server: Plugin-System einbauen
* DOI-Bot: Vorversionen in Metadaten verlinken
  (gitlab:Webservices/heiper/-/issues/4)
* Frontend: Unter-Annotationen hierarchisch darstellen mit Baumstruktur
  oben und Detail-Ansicht ausgewählter Einzelannotation darunter.
* Frontend: Verschlagwortung mit standardisierten Nicht-GND-Vorkabularen
  * Projekt-spezifische Vorkabulare
    * Erstmal per Plugin und/oder XRQ laden.
    * Später abruf via Nils' Normdatenserver? Lässt sich der GND-Code
      wiederverwenden?
  * ggf. auch Zeitpunkte/-spannen
  * ggf. auch Geo-Koordinaten
* Anno-Frontend modularisieren. Siehe Mail "Re: l10nOverrides" 2024-07-31 06:38
* Bei Bildern immer auch Scope angeben.
  https://www.w3.org/TR/annotation-model/#scope-of-a-resource



### später (absteigende Priorität)

<details>

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
* Benachrichtigung für Autoren über Antworten auf ihre Beiträge
* Frontend: Verschlagwortung mit Geonames

</details>



### später (unpriorisiert)

<details>

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
* Frontend: Auswahl für Lizenz und Sprache nur bei Bedarf aufklappen
  (insb. wenn noch nicht gewählt), sonst zugeklappt kompakt nebeneinander.
* Cron Job: Benutzer-Config aus externer Datenbank laden.
* [Annotorious](https://annotorious.github.io/) erkunden
* Musik-Anno-Leute fragen: Noten auch als MIDI? ggf. mit Player im Browser?
  Upgraden auf interaktiv-kreatives Erlebnis mit MIDI-Editor?
  * Erstmal mit aktuellen SoundFonts von LAN-Server zeigen dass möglich,
    dann ggf. weiterforschen wie man kompaktere Soundfonts machen kann,
    ob z.B. Teile von FluidSynth nach asm.js compilieren. Ggf. Patente klären!
* Zwecks Übersicht und Marketing: Diagramm, welche Arbeitsgruppen unsere
  Annos wofür verwenden.

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
