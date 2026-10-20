# Triangle Guy, Brunnenfund und flacher Thaddäus

Kumulativer BPS-Gesamtpatch für die unveränderte Europa/PAL-1.0-ROM (Original-MD5 e040de91a74b61e3201db0e2323f768a). ROM-SHA256 `0c62cdcbb5ab278e5e785df3308bf3ea9844c74b99edbc513f162513891a0c4c`. Alle bisherigen Änderungen enthalten; 1.000 eigene deutsche Nachrichten. Alte Rechtschreibung und native Textsteuerung erhalten.

## Figuren und Fundstücke

Triangle Guy steht in der finalen Ganon-Arena bei −800/1086/−550, innerhalb des Feuerrings am Rand, von Zelda, Schwert und zentralen Kampfflächen entfernt. 904 statt 13.646 Dreiecke; ursprüngliche Proportionen, 88 Einheiten hoch. Statischer friedlicher NPC, normale manuelle A-Ansprache, keine Kollision oder Angriff-/Trefferannahme. Er startet kein Gespräch automatisch. Der neue Helfer bietet Text nur im freien Spiel an, nicht während einer aktiven Zwischensequenz. Die native Gesprächsfunktion pausiert Boß-Akteure; nach dem Schließen läuft der Kampf weiter. Nachricht 608A enthält den gewünschten Entschuldigungssatz.

Schwangerschaftstest: Seitenkammer 6 des Brunnens, −415/1/−1010, am vorderen seitlichen Boden abseits der Pflanze und der fliegenden Töpfe. 144 statt 1.110 Dreiecke, 14 Einheiten lang; 64×64 CI4. Nur als Kind. Z und C-Up für Nachricht 608B: „Oof, hier liegt ein Schwangerschaftstest. Mein Beileid...“.

Flacher Thaddäus: Morphas Boßraum, 545/1/545 auf dem festen Eckboden. Das ganze Modell liegt außerhalb des mittleren Wasserbeckens und vor den Stacheln. Es bleibt auch bei abgesenktem Wasser nach dem Kampf dort. 1.145 statt 152.304 Dreiecke, Konturhüllen entfernt; 83,44 breit, 14,87 hoch und 105 lang. Ein 64×64-CI4-Atlas, statisch, keine Physik, Kollision, Schadensannahme oder Animation. Z und C-Up für die blaue Navi-Nachricht 608C: „Scheiße Mann, der Typ ist tot!!“. Der lebendige Thaddäus und seine Weisen-Auftritte bleiben erhalten.

Alle drei benutzen das vorhandene Elf_Msg2-Overlay mit eindeutig auf Szene/Raum/Parameter begrenzten Ergänzungen. Die Modell-Daten werden nur mit ihrem Raum geladen. Keine zusätzlichen Objekt-Slots. Native Beleuchtung, Nebel und Tiefentest. Keine veränderten Türen, Schalter, Kollisionsflächen, Wasserstände oder Boß-Auslöser. Die finale Versiegelungs-Zwischensequenz benutzt weiter ihre ursprüngliche alternative Akteursliste ohne Triangle Guy.

## Speicher und Laufzeit

Tatsächliche 4 MiB RAM im Mupen64Plus/GLideN64-Emulator. Die Objektbank hat bei Morpha 183.952 Bytes Reserve; es gibt keinen zusätzlichen Objektbank-Bedarf. Der maximale Raum-Puffer wächst dort von 63.328 auf 113.216 Bytes, bei Ganon von 16.720 auf 41.344 Bytes; im Brunnen bleibt der Maximalpuffer bei 133.312 Bytes. Das Elf-Msg2-Overlay wächst um weniger als 4 KiB.

Die gepatchte ROM-Datei ist jetzt 40 MiB groß: Der bisherige komprimierte Stand lag bereits knapp unter 32 MiB, und die neuen Daten überschreiten die nächste Dateigrenze. Das ist Dateispeicher, keine Erhöhung des benötigten N64-Arbeitsspeichers. Kein Expansion Pak erforderlich.

Vergleich bei identischen vorbereiteten Spielständen und Emulator-Einstellungen, nacheinander ohne zweiten Emulator. Gemessen sind Host-Zeiten zwischen Emulator-Frame-Callbacks nach der Aufwärmphase, ohne Bildschirmaufnahmen im Meßfenster. Diese Werte sind ein Vergleich dieses Emulators, keine behauptete Hardware-Bildrate.

| Kampfsituation | Vorher Median / P95 (ms) | Mit Fundstück Median / P95 (ms) |
| --- | --- | --- |
| Ein Tentakel | 28.35 / 53.91 | 29.31 / 46.20 |
| Zwei Tentakel | 27.58 / 48.69 | 31.45 / 57.55 |

Da sich die zufälligen Kampfverläufe beim ersten Vergleich unterschieden, folgt eine zusätzliche kontrollierte Probe: derselbe gespeicherte Zustand derselben Produktions-ROM, einmal mit rein im Test ausgeblendetem Fundstück und einmal normal sichtbar. Alle protokollierten Boß-Zustände, Spielerpositionen und Lebenspunkte stimmen dabei exakt überein. Je 600 Meßwerte: ausgeblendet 33.13 / 69.57 ms, sichtbar 30.95 / 48.08 ms (Median/P95). Der sichtbare Lauf war hier schneller; die Host-Streuung erlaubt keine Aussage über einen Geschwindigkeitsgewinn. Ein zusätzlicher Laufzeiteinbruch durch das Fundstück ist in dieser Kontrolle nicht erkennbar. Das Ausblenden erfolgt ausschließlich über den Draw-Zeiger des lokalen Test-Akteurs, ohne Änderung an der ROM oder der Boß-KI. Gespeicherter Zustand und RAM-Daten werden nicht veröffentlicht.

Für die zusätzliche Zweitentakel-Streßprobe setzt ausschließlich das lokale Testprogramm einmal Morphas HP auf 14 und den nativen Treffzähler auf 3. Danach erzeugt und bewegt die unveränderte Boß-KI den zweiten Tentakel selbst. Diese Vorbereitung ist in den Testprotokollen sichtbar und nicht Bestandteil der Produktions-ROM. In beiden Vergleichs-ROMs sind drei Morpha-Akteure (Kern und zwei Tentakel) nachgewiesen. Keine Abstürze, RSP-Darstellungsfehler oder Objektbank-Überläufe in diesen Proben.

## Weitere Prüfung

7 bestätigte funktionale Emulatorproben auf der finalen ROM: Brunnenfund mit Wiederholung; erste Morpha-Ankunft; weitere Ansicht von Thaddäus; Untersuchung bei aktivem Kampf samt Rückkehr zum Spiel; vorbereiteter Nach-Boß-Zustand mit entferntem Morpha und erhaltenem Fund; englische Gegenprobe ohne Ergänzung; vollständiges natives Ganon-Intro mit anschließendem Weg zum NPC und seiner normalen Gesprächsseite. Für die Ganon-Probe wurde Link regulär über den vorbereiteten Spielstand mit zwanzig Herzen ausgestattet. Drei Gespräche wurden geöffnet und geschlossen; im anschließenden unverteidigten Kampf starb Link regulär. Das wird nicht als gewonnener Boßkampf ausgegeben. Keine Positionen von NPCs, Boß-Akteuren oder Kameras im Emulator umgeschrieben. Verworfene frühe Vorschau-/Steuerungsproben werden nicht als bestanden gezählt.

Alle 1.509 komprimierten Segmente gegen den Neubau geprüft, CIC-6105-Prüfsumme korrekt. 1.000 Textpuffer mit maximalem Spielernamen geprüft. Gegenüber der vorherigen Fassung ändern sich nur die drei neuen deutschen Nachrichten. Alle übrigen deutschen sowie sämtliche englischen/französischen Nachrichten erhalten. 89 ursprüngliche Raum-Assets einschließlich Akteurslisten, Türen, alternativen Szenenbefehlen und Geometrie anhand von Originalbytes/echten MIPS-Relokationen erhalten. Der gesamte übrige ROM-Inhalt bleibt bytegleich oder enthält nur echte Linker-Relokationen. 2.955 Kernfunktionen sowie alle geprüften bisherigen Kampf- und Elf-Msg2-Funktionen erhalten. Beide Boß-Overlays bleiben unverändert oder nur neu gelinkt; keine Änderung an Angriffen, Trefferpunkten, Tod oder Ablauf.

RomPatcher.js mit aktiver Quellvalidierung erzeugt aus Vanilla und BPS bytegenau die geprüfte Produktions-ROM. Kein vollständiger Spieldurchlauf und kein Hardwaretest. Keine ROM, Spielstände, Emulator-Zustände, RAM-Abbilder oder ausführbaren Dateien veröffentlicht. Bilder sind unveränderte echte Emulatoraufnahmen.
