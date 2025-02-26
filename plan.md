
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
U+1F56E book (🕮)
U+1F578 spider web (🕸)
U+1F5D1 wastebasket (🗑)
U+1F5D9 cancellation x (🗙)
U+1F6A7 construction sign (🚧)

> -->


Planteile vergangener Jahre:
[2022](old/22/plan.2022.md)
[2023](old/23/plan.2023.md)
[2024](old/24/plan.2024.md)


2025
====

<!-- Mo 06.01. entfiel weil Feiertag -->

### bis 13.01.

* ✅ Anno-Digi-Anleitung probelesen
* ✅ Vorjahr zusammenfassen für Jahresbericht


### bis 20.01.

* ✅ IIIF v3 in Mirador funktioniert für Einzelrechtecke.
* 🛤 heiImageViewer vorantreiben


### bis 27.01.

* ✅ IIIF v3 in Mirador funktioniert für Polygone.
* ✅ IIIF v3 in Mirador hat jetzt klickbaren Link zur Annotation.
* 🛤 heiImageViewer vorantreiben: bessere Internationalisierung.


### bis 03.02.

* ✅ Besprechung TIB-Vokabulardienst
* ✅ IIIF v3 in Mirador funktioniert für all unsere Formen.
* 🛤 heiImageViewer vorantreiben
* ⏳ Postgres Anno-ID-Spalten auf custom data type umbauen (begonnen)
* ✅ anno-doc: wkhtml probiert: wird nicht mehr gewartet.


### bis 10.02.

* ✅ IIIF v3 in Mirador kann SVG-Selektoren jetzt skalieren.
* 🛤 heiImageViewer vorantreiben


### bis 17.02.

* ✅ Digi-Demo eingerichtet, DWork aufgeräumt.
* ✅ Besprechung TIB-Vokabulardienst


### bis 24.02.

* ✅ Anno-Server: Fälschliche Ergebnisanzahlbegrenzung der Suche entfernt.
* ☔ TIB Vokabular-API ausprobiert, vorerst erfolglos.


<!-- 3.3. entfällt -->

### bis 08.03.

* Postgres Anno-ID-Spalten auf custom data type umbauen + Migrator dafür
* 🛤 heiImageViewer vorantreiben





### nahe Zukunft

* Anno Server: Einstellen können, wie viele alte Logs man behalten möchte.
* heiImageViewer Bugs siehe GitLab
* heiImageViewer Release Skript bauen
  * braucht bessere i18n
    * Anhand von anno-frontend vorturnen, damit Gustavo es nachbauen kann.
* Anno-Frontend: Schlagworte-API-Demo
  * Alternative zum TIB-Vokabulardienst: https://api.dante.gbv.de/start/
* Anno-Frontend: Schlagworte-Wolke über Anno-Liste.
  * Nur-Schlagworte-Annos darin verstecken.
  * Anno-Server soll dann vermutlich Nur-Schlagworte-Annos
    ohne Text und Titel erlauben.
* Anno-Frontend: Sortierung leichter testbar machen und testen

* Server: Legacy Endpoint, der `dc:title` im `body` mit ausgibt.
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



* Anno-Frontend in HeidIcon integrieren
* Inline Blobs (Bild/Video) im Body verbieten
* Leere `alt=`-Attribute aus `img`-Tags entfernen
* DOI-Bot: "latest"-Log möglichst erst nach Rerun-Wartezeit drehen.
* Suchergebnisse nach Datum (wenn vorhanden, des VÖ-Stempels) sortieren!
  besonders bei RSS.


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
* Quill (unser HTML-Editor für den TextualBody) benutzt veraltetes Event
  DOMNodeInserted und wird bald nicht mehr unterstützt, warnt Firefox.





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
