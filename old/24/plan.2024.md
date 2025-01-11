
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

* ✅ Server: ACL-Benutzergruppen reparieren
* ✅ Server: Kleinere Bugfixes und Refactoring


### bis 18.11.

* ✅ HTML-Sanitizer entfernt unnützen Whitespace jetzt zuverlässiger
* ✅ Users config converter: UUID-Bug behoben. Erzeugt jetzt bei Umwandlung
    auch Korrektur-Skript für die alten UUIDs.


### bis 25.11.

* ✅ Autor-UUID-Umstellung
* ✅ Postgres-Update auf v16
* ✅ Frontend: Phantom-Multitargets debuggen


### bis 02.12.

* ✅ Daily Anno Dumper funktioniert
* ✅ IIIF-Anno-Beispiel nachgebaut und in Mirador getestet


### bis 09.12.

* ✅ IIIF Einzel-Rechteck für Single Target Anno funtioniert


### bis 16.12.

* ✅ Frontend: "Als Vorlage speichern"-Checkbox umbauen
* ✅ Frontend: Bessere Hilfe-Button-Topics
* ✅ Frontend: Vorlagen-Speicherung reparieren (noch ungetestet)



### Jahresbericht-Eckpunkte








