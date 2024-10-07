
Warum eingebettete Rohdaten eine schlechte Idee sind
====================================================

Der bisher häufigste Anwendungsfall für Rohdaten in unseren Annotationen sind
Bilder. Denkbar wären auch z.B. Musik, 3D-Modelle oder sonstige Dateien.


### Download-Zwang

Im Body eingebettete Rohdaten müssen von jedem Anno Client
(d.h. verarbeitendes Programm, z.B. unser Annotationen-Editor)
heruntergeladen werden, egal ob er das Datenformat überhaupt versteht.


### Duplikate

Wenn eine Annotation bearbeitet wird, enthält die neue Version eine
komplette Kopie der Rohdaten. Diese Duplikate verschwenden Speicherplatz
und daran gekoppelte Resourcen: Datenübertragung, Datenbank-Leistung,
Hauptspeicher in Clients;
letztendlich immer auch Strom (ggf. Akku-Zeit), Bearbeitungszeit
und Geräteverschleiß.


### Aufblähung durch Verpackung

Annotationen sind gemäß Anno-Standard primär für Text ausgelegt.
Um Binärdaten (z.B. Bilder) in Text "verstecken" zu können, müssen die
Daten verpackt werden (sog. "Base64-Kodierung"), was den Speicherbedarf
(und daran gekoppelte Resourcen) um mindestens ein Drittel erhöht.


### Unscheinbare Riesen

Multimedia-Inhalte sind üblicherweise gigantisch im Vergleich zu ihrem
Begleittext. Das Sprichwort "Ein Bild sagt mehr als tausend Worte"
ist hier noch untertrieben: Schon ein scheinbar kleines Bild kann leicht
so viel Daten verbrauchen wie der Text eines ganzen Buches.


### Überforderte Clients

Da der Anno-Standard auf Text ausgelegt ist, sind auch alle üblichen
Anno Clients auf Text ausgelegt.
Unerwartete erhöhte Belastung durch die vergleichsweise riesigen Einbettungen
können zu schlechterer (z.B. langsamerer) Funktion führem, im Extremfall
sogar zu komplettem Versagen, wenn z.B. ein mobiles Endgerät die erforderliche
Leistung nicht aufbringen kann.


### Veraltete Kodierungen

Immer mal wieder findet die Menschheit bessere Methoden, Daten zu kodieren.
Gerade bei Multimedia gab es mehrere bahnbrechende Effizienz-Steigerungen,
um den selben Inhalt mit weniger Datenverbrauch zu speichern.
Datenpakete sollten daher idealerweise in einer Form gespeichert werden,
die leicht aufgerüstet werden kann um von technologischen Verbesserungen
zu profitieren.


### Kompetenzbündelung

Auch für Dateiformate gilt: Je besser man sich damit auskennt, desto mehr
Spitzfindigkeiten und Fallstricke kennt man und kann sie berücksichtigen.
Neben der oben schon angesprochenen Kodierung gibt es gerade bei
Multimedia-Dateien oftmals Aspekte, an die nicht jeder gleich denkt,
z.B. enthaltene Zusatzdaten über verwendete Programme und Geräte,
bei Fotos auch Datum und Ort, teilweise persönliche Daten wie
ein Benutzername in einem "gespeichert von"-Feld, und weitere Anhaltspunkte
für Personen- und Verhaltensprofile.
Manchmal werden auch irrtümlich zu viele Daten mitgespeichert:
So sorgte z.B. im März 2023 ein Bug für große Aufregung, durch den weit
verbreitete Standard-Software beim Speichern von zugeschnittenen Bildern
versehentlich einen Großteil des originalen, unzugeschnittenen Bildes
verdeckt mitspeicherte.

Viele Gründe also, Datenpakete lieber auf für das jeweilige Format optimierte
Plattformen zu speichern, wo sie von auf das jeweilige Format und Medium
spezialisierten Experten verantwortungsvoll nachbetreut werden können.


### Das Web ist ein Dialog

Annotationen sollen keine Einbahnstraße sein. Der Anno-Standard lebt das vor,
indem Annotationen wiederum annotiert werden können.
Eine große interaktive Diskussion.
Im gleichen Geiste sollten auch in der Diskussion verwendete Datenpakete
wieder zu Diskussionsstoff werden können. Dafür sollten sie in einer per
URI benennbaren Form vorliegen – bei Einbettung in den Text ist das nicht
sinnvoll möglich.


### Anreicherung mit weiteren Daten

Selbst wenn es im ersten Moment scheint, als könne das Datenpaket (z.B. Bild)
sehr gut für sich selbst stehen bzw. als sei die Annotation genügend Kontext,
kann doch später der Wunsch entstehen, es mit weiteren Daten anzureichern:

* Abgewandelte/weitere Versionen
  * Vorschauen: Bei Bildern z.B. Verkleinerungen, bei Musik z.B. Spektrogramm.
  * nachträglich verfügbar gewordene bessere Versionen durch z.B. Fund,
    neu entwickelte bildgebende Verfahren, abgelaufene Geheimhaltung usw.
  * Extrakte: Bei Fotos z.B. abgebildete Personen und Gegenstände nochmal
    einzeln, bei Musik z.B. prominente Passagen.
* Provenienz
* Errata
* Bildbeschreibung für sehbehinderte Menschen
* Bildbeschreibung für künstliche Intelligenz
* Themenzuordnungen ("Tags")
* Obige Punkte auch mehrsprachig

















