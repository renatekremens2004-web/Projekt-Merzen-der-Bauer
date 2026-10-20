# Punk: sichtbare Arme und korrekte Jacke, v3

Kumulativer Gesamtpatch auf unveränderte Europa/PAL-1.0-ROM. Original-MD5 `e040de91a74b61e3201db0e2323f768a`. Ziel-SHA256 `d47361adcee8709b8dd2a1a4ce794a8dcc9808e2946a0fabd09883219bb4e7a4`. Alle bisherigen Änderungen enthalten; weiterhin 1.013 bearbeitete deutsche Nachrichten.

## Ursache und Korrektur

Die Arme waren vorhanden, aber kaum sichtbar. Die Vorlage hat dünne Arme. Im Export kamen zwei Fehler hinzu: Cube.008 enthält sowohl die Jacke als auch beide Arme; die pauschale Armzuordnung drehte auch den Oberkörper mit. Außerdem verschob die Polygonreduktion UV-Koordinaten zwischen getrennten Farbinseln. Gelbe Haut landete dadurch in dunklen Bereichen des Atlas.

Nur echte Armflächen werden jetzt den Armbewegungen zugeordnet. Die Jacke bleibt am Oberkörper. Schulterpunkte liegen an den tatsächlichen Ansätzen; die Ruhehaltung senkt die Arme um 45 statt 50 Grad ab. Gelbe Unterarme und Hände bekommen dieselbe stabile Hautfarbe wie der Kopf. Blau und Grün der Jacke werden vor der UV-Vereinfachung gesichert. Native Beleuchtung, Nebel und Tiefentest bleiben erhalten. Keine selbstleuchtenden Arme, kein breites Strecken auf ein fremdes Skelett und keine Vergrößerung der Figur.

Die Arme werden vor der Vereinfachung vom Oberkörper getrennt und erhalten mehr vom vorhandenen Geometriebudget; kleine Zierdetails weniger. Insgesamt 1.464 statt 1.463 Dreiecke, also praktisch gleiches Gesamtbudget. Kopf und Gesicht bleiben erhalten. Gleiche Höhe von 74 Spieleinheiten, weiterhin vier eigene starre Bewegungsteile. Keine neuen Akteure, Kollisionskörper oder Objekt-Slots. Raum-Puffer vor Ganons Schloß jetzt 132112 Bytes statt 134.816 in v2. In der gemessenen nativen Objektbank bleiben 144144 Bytes frei; diese Bank ist getrennt vom Raum-Puffer.

## Prüfung

Zwei erfolgreiche Emulatorproben auf genau der oben genannten ROM mit Mupen64Plus/GLideN64 und echten 4 MiB: normales Gespräch komplett lesen, schließen und wiederholen sowie eine Ganzkörperansicht ohne Textkasten. Native Gesprächs- und Spielkamera. Für die zweite Ansicht wird nur Links Position im lokalen Spielstand vorbereitet; der NPC bleibt am tatsächlichen Spielort. Vor Ganons Schloß gilt die native feste Dämmerungsbeleuchtung. Keine beobachteten Abstürze, Objektbanküberläufe oder fehlerhaften Grafikbefehle.

Alle 1.509 komprimierten Segmente, CIC-6105-Prüfsumme und 1.013 Textpuffer geprüft. 255 native Raum-Assets und 2.955 Kernfunktionen erhalten. Gegen die zuletzt veröffentlichte v2-ROM mit SHA256 `afcbd5fde6a4ef3f69fc58eb7c4f48dd49f26899ea6e8a0cb15e3011aeb87556` geprüft: sämtliche Nachrichten in allen Sprachen gleich. Normales Yellow-Guy-Raumsegment und Wario-Raumsegment bytegenau identisch. Alle anderen Segmente außerhalb des Punk-Raums und der notwendigen Tabellen erhalten bzw. ausschließlich mit echten MIPS-Linker-Relokationen verändert. Beim Elf-Msg2-Overlay sind zusätzlich genau die aus den neuen Modelldaten abgeleiteten Schulter-Pivots geändert; übriger Inhalt auf Bytegleichheit bzw. echte Relokationen geprüft.

Die entfernte Selbstvorstellung bleibt entfernt. Wario bleibt ausschließlich im jungen Kakariko. Die zehn Alters-/Sprachproben aus v1 und die früheren v2-Proben bleiben historische Nachweise; sie wurden nicht erneut ausgeführt. Vollständiger Durchlauf und echte N64-Hardware stehen weiterhin aus.

RomPatcher.js mit aktiver Quellvalidierung erzeugt aus Vanilla und BPS bytegenau die geprüfte ROM. Veröffentlicht werden ausschließlich Patch, Quellen, Protokolle und unveränderte echte Emulatorbilder. Keine ROMs, Spielstände, Emulatorzustände oder ausführbaren Programme.
