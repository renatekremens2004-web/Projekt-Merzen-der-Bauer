# V57: Hunting-Rifle- und Flammenwerfer-Soldaten

V57 enthält alle bisherigen Änderungen. Genau einen der beiden BPS-Patches auf eine **saubere europäische PAL-1.0-ROM** anwenden (MD5 `e040de91a74b61e3201db0e2323f768a`), nicht auf eine bereits gepatchte ROM.

## Hunting Rifle in Darunias Raum

Der vorbereitete Hunting-Rifle-Gorone steht jetzt in der erwachsenen Version von Darunias Büro in Goronia. Er steht seitlich vor dem hinteren Bereich; Eingang, Durchgang und Statue bleiben erreichbar. Sein Text:

> Der Feuertempel war einst das Heiligtum der Goronen. Friedrich Merz benutzt ihn nun als Arbeitslager. Er liebt Arbeit wie kein anderer, sagt er.

## Flammenwerfer-Soldat vor dem Gerudotal

Auf der **Hyrule-Feld-Seite** vor dem Gerudotal steht ein zusätzlicher Soldat bei den dortigen Truppen. Er steht auf einer ebenen Fläche, mit Abstand zum Zaun und zu den vorhandenen Panzern. Sein Text:

> Ich habe diesen Flammenwerfer, um den Gerudo ein Stück vom Todesberg mitzubringen.

Die Gasmaske ist an den breiten Goronenkopf angepaßt und verdeckt das Gesicht. Sie dreht sich mit dem Kopf. Die gelben Tanks sitzen als aufrechtes Paar am Rücken und bewegen sich mit dem Oberkörper. Der Flammenwerfer ist an die rechte Hand gebunden; die vorhandene linke Handhaltung stützt ihn.

Beide Soldaten bleiben dauerhaft aufrecht, blinzeln, atmen und richten den Kopf zum Spieler. Sie sind freundliche Gesprächspartner. Die Waffen sind getragene Requisiten; keine zusätzliche Angriffs-, Schuß- oder Feuerlogik. Beide Figuren erscheinen nur im normalen deutschen Spiel als Erwachsener. Kinder- und Credits-Header bleiben unverändert. Die Gespräche sind wiederholbar und verketten sich nicht mit anderen NPC-Texten.

## Modell- und Speicherbudget

- Hunting Rifle: 128 Dreiecke.
- Flammenwerfer: 200 Dreiecke, gegenüber 280 im Quellmodell reduziert.
- Rückentanks: 228 Dreiecke.
- Gasmaske: 426 Dreiecke; Gesichtsform und Filter bleiben erhalten.

Die beiden neuen Figuren verwenden eine eigene Ausrüstungsbank mit **42.192 Bytes**, einschließlich des passenden Helms. Sie wird nur in Darunias erwachsenem Raum und dem erwachsenen Hyrule-Feld geladen. Die bisherige gemeinsame Ausrüstungsbank wächst nicht; die Gewehr- und Schrotflinten-Soldaten behalten ihre Modelle und ihr Verhalten. Alle Texturen sind für den N64 aufbereitet.

Mit nativen 4 MiB geprüft: In Darunias Raum sind 13 Objekt-Slots belegt und 157.808 Bytes in der Objektbank frei. Beim Flammenwerfer-Soldaten sind es ebenfalls 13 Slots und 107.616 freie Bytes. Link konnte vom Feld aus mit normaler Steuerung zum Flammenwerfer-Soldaten laufen und ihn ansprechen. Nach dem Gespräch im Büro wurde regulär in die große Halle von Goronia gelaufen, einschließlich vollständig geladener Folgeobjekte und des dortigen bisherigen Soldaten; dort blieben 169.088 Bytes frei.

## Prüfung und Grenzen

Normale und DEBUG-Version: neue Figuren samt Gesprächen geprüft. Zusätzlich Tag/Nacht am Feld, Abwesenheit beider Figuren als Kind, Erreichbarkeit und der Raumübergang aus Darunias Büro. Die folgenden Daten stimmen weiterhin mit V56 überein: 405 bisherige Objektbanken, 386 andere Räume, alle 101 Szenen einschließlich der Credits-Kameras und alle drei Musiksegmente. Sämtliche bisherigen Texte wurden in allen vier Sprachblöcken unverändert erhalten.

Die normale Produktionsversion wurde nach dem DEBUG-Build wiederhergestellt. Beide BPS-Patches wurden mit einem unabhängigen Patcher angewandt und mit den getesteten ROMs verglichen. Die Bilder zeigen echte Emulatoransichten; nur für die Nahansichten wurde eine Testkamera verwendet. Ein vollständiger neuer Spieldurchlauf ist durch diese gezielten Tests nicht ersetzt.

## Quellen und DEBUG

Nach V56 folgt `python3 tools/build_special_soldiers_v57.py /pfad/zum/oot-decomp`. Die neuen Texte stehen in `story/special_soldiers_v57_de.json`. Das zuvor separat vorbereitete Hunting-Rifle-Asset wird jetzt von dieser Version verwendet. Die neuen Aufsätze lassen sich mit `tools/export_special_soldiers_v57.py` aus den mitgelieferten Mesh-Daten reproduzieren; der Export verändert keine Decomp-Dateien.

Das Quellenpaket enthält die originale Masken-DAE und die beiden glTF-Modelle; deren Binärpuffer sind verlustfrei als Daten-URI im glTF eingebettet. Die ursprünglichen Modell-Rohdaten bleiben damit vollständig vorhanden. Es sind keine ROMs oder Emulator-Speicherstände enthalten.

DEBUG bleibt optional und wird zuletzt mit `tools/build_debug_version.py` erstellt. L+R halten und Z drücken öffnet das Menü; die bisherigen Optionen für alle Items, Gewänder und Credits bleiben erhalten.
