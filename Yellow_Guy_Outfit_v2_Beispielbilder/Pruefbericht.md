# Yellow Guy: Outfit-Korrektur v2

Kumulativer Gesamtpatch auf unveränderte Europa/PAL-1.0-ROM, Original-MD5 `e040de91a74b61e3201db0e2323f768a`. Ziel-SHA256 `afcbd5fde6a4ef3f69fc58eb7c4f48dd49f26899ea6e8a0cb15e3011aeb87556`. Alle bisherigen Änderungen enthalten, weiterhin 1.013 eigene deutsche Nachrichten.

## Korrektur

Im vorigen Export waren mehrere UV-texturierte Körperteile pauschal schwarz eingefärbt. Dadurch gingen die farbigen Ärmel, gelben Hautflächen und Aufnäher verloren. Diese Flächen verwenden nun die ursprünglichen UV-Koordinaten und die mitgelieferte yp.png. Das Original-Outfit enthält auch weiterhin dunkle Jacke und Stiefel. Rein schwarze Texel der Kleidung bekommen vor der N64-Beleuchtung einen kleinen Reflexionswert RGB 42/45/56, damit Formen erkennbar bleiben. Ein eigener 64×64-Ausschnitt erhält den PUNK-Aufnäher. Der Kopf bleibt wie zuvor.

Keine neue Geometrie: weiterhin 1.463 Dreiecke, identische Positionen und Normalen, gleiche Höhe von 74 Einheiten, dieselben vier Bewegungsteile. Native Beleuchtung, Nebel und Tiefentest. Die Kleidung wird nicht selbstleuchtend. Der Raum vor Ganons Schloß wächst gegenüber v1 um 11.024 auf 134.816 Bytes. Keine zusätzlichen Akteure, Kollisionskörper, Objekt-Slots oder Matrizen. In der gemessenen Objektbank bleiben 144144 Bytes frei; Raum-Puffer und Objektbank werden getrennt erfaßt.

608F beginnt jetzt „Oh. Hallo! Ich bin machen einen Ausflug. Nach ... hier. Hyrule.“ Die Selbstbenennung „Ich bin Yellow Guy“ ist entfernt. Der Punk stellt sich ebenfalls nicht mit diesem Namen vor. Alle anderen Dialoge, insbesondere Warios Kind-Zeitebene und seine Texte, bleiben gleich.

## Prüfung

Drei erfolgreiche Szenenproben auf genau dieser ROM mit Mupen64Plus/GLideN64 und tatsächlichen 4 MiB RAM: beide Gespräche vollständig lesen, schließen und wiederholen; dazu eine Ganzkörperansicht des Punks ohne Textkasten. Nur die lokale Spielerposition und der Fortschritt sind vorbereitet. NPC-Position, native Kamera und Beleuchtung werden nicht für die Bilder umgeschrieben. Keine beobachteten Abstürze, Objektbank-Überläufe oder fehlerhaften Grafikbefehle. Vor Ganons Schloß gilt die native feste Dämmerungszeit.

Alle 1.509 komprimierten Segmente mit dem vollständigen Neubau und die CIC-6105-Prüfsumme geprüft. 255 ursprüngliche Raum-Assets und 2.955 Kernfunktionen erhalten. Zusätzlich gegen die zuletzt veröffentlichte ROM mit SHA256 `3ccb86e313042254c168bd443f835b40a8095b6531641757d6599c6d94330676` geprüft: nur deutscher Text 608F geändert, alle anderen Nachrichten und Sprachen erhalten. Normales Yellow-Guy-Raumsegment und Wario-Raumsegment bytegenau identisch. Alle übrigen Segmente außerhalb der notwendigen ROM-Tabellen, deutschen Textdaten, Zeigertabellen und des Punk-Raums bleiben bytegleich oder enthalten ausschließlich echte MIPS-Linker-Relokationen. Punk-Geometrie, Normalen und Pivots ausdrücklich identisch. Alle 1.013 bearbeiteten Textpuffer erneut geprüft.

Die zehn Alters-/Sprach-/Tagesproben aus v1 bleiben in der Quellenhistorie als frühere Proben dokumentiert; sie werden nicht als erneut auf v2 ausgeführt ausgegeben. Ein vollständiger Durchlauf und echte N64-Hardware stehen weiterhin aus.

RomPatcher.js mit aktiver Quellvalidierung erzeugt aus Vanilla und BPS bytegenau die hier geprüfte Produktions-ROM. Nur Patch, Quellen, Prüfungen und unveränderte echte Emulatorbilder werden veröffentlicht; keine ROMs, Spielstände, Emulatorzustände oder ausführbaren Programme.
