# Nintendo-64-Gag in Jabu-Jabu

Ein zusätzlicher Eintrag in Raum 3 der normalen Jabu-Jabu-Fassung: auf der unteren Plattform bei Rutos erstem Sturz, Position (130, -1113, -3180). Die Konsole ist 10 Spieleinheiten breit und behält die Proportionen des gelieferten Modells einschließlich Ocarina-of-Time-Kassette, Controller und Kabel. 1376 Dreiecke. Keine Änderung an Links Größe.

Ein privater deutscher Text 0125 aus der freien Retail-Platzhalterzeile verwendet die funktionalen Steuerzeichen des ursprünglichen Navi-Hinweises 0148. Der Inhalt ist der gewünschte Satz; er paßt auf eine normale, manuell geschlossene Seite. Insgesamt 597 deutsche Nachrichten. Die drei Fortsetzungen der vorherigen Habeck-Rede bleiben erhalten.

## Umsetzung

Der Raum bekommt genau einen zusätzlichen Elf_Msg2-Prüfpunkt. Die vorherigen acht Einträge bleiben unverändert. Parameter 3F25 wählt Nachricht 0125 und keinen Switch. Rotation Z=1 erhält den Prüfpunkt nach dem Lesen. Die native Zielerfassung, C-Up-Behandlung, Textschließung und Wiederholung werden unverändert verwendet. Keine Änderungen am Spieler, an Navi, an Gegnertexten oder an globalen Zieltextregeln.

Nur ElfMsg2_Init erhält für genau diese Parameter in Szene Jabu-Jabu/Raum 3 einen zusätzlichen Zweig: gleiche Skalierung 0.01, Fokus 3 Einheiten über dem Boden und eine eigene Draw-Funktion. Sie verwendet die Szenenbeleuchtung und Normalen. Andere Prüfstellen behalten ihr ursprüngliches Verhalten. In anderen Sprachen wird nur diese neue Instanz ausgeblendet. Die restlichen englischen/französischen Texte bleiben unverändert. Der reine Dekogegenstand hat keinen Weg-blockierenden Collider und keine Gegenstands- oder Schalterwirkung.

Die Modelldaten liegen ausschließlich am Ende der Raum-3-Datei; andere Navi-Prüfstellen laden kein zusätzliches Modell. Der Overlay wächst von 1136 auf 1536 Bytes. Raum 3 wächst von 29024 auf 142496 Bytes. Nach Entfernen des zusätzlichen Actor-Eintrags bleiben alle ursprünglichen Raumdaten bytegleich, abgesehen von der Actor-Anzahl und 82 geprüften Segmentzeiger-Verschiebungen um jeweils 16 Bytes. Die vorhandene Raumgeometrie bleibt erhalten.

## Verifikation

Build, PAL-Prüfsumme und Kompression aller 1509 Segmente erfolgreich geprüft. Vergleich mit der veröffentlichten Habeck-Fassung: Änderungen auf die deutschen Nachrichten, den Elf_Msg2-Overlay, Raum 3 und erforderliche Adreßdaten begrenzt. Bean-, Thaddäus- und Habeck-Objekte bleiben bytegleich. Die ursprünglichen Elf_Msg2-Funktionen sind bis auf den beschriebenen Init-Zweig quellgleich; die Darstellung ist eine neue Funktion. Alle 597 funktionalen Textkontrollsequenzen geprüft, einschließlich der vorhandenen Habeck-Fortsetzungen. Der neue Text bleibt innerhalb der Textpuffer- und Font-Breiten-Grenzen.

Gezielte Laufzeitprüfung mit derselben komprimierten Produktions-ROM, 4 MB, Mupen64Plus/GLideN64, EnableClipping=True, EnableCustomSettings=False:

- Kinder-Link in Raum 3: normale Z-Zielerfassung und C-Up öffnen 0125. Wiederholtes Öffnen funktioniert; die Instanz bleibt aktiv. Position, uniforme Skalierung und unverändertes Schalterwort im Protokoll.
- Seitliche Größen-/Bildprobe mit Kinder-Link. Derselbe Kommentar erscheint. Auch ein nativer Biri-Navi-Text 0617 wird im selben Raum beobachtet; der neue Text ersetzt keine Gegner-Roasts.
- Englische Gegenprüfung in Raum 3: die neue Instanz ist nicht aktiv, kein Text 0125.
- Gegenprüfung in Raum 0: keine Konsole, kein Text 0125.

Teststarts setzen Szene, Raum, Tageszeit, Inventar-/Storyfortschritt und Spielerposition. Die Konsole und alle Gegner bleiben an ihren Produktionspositionen aktiv. Für die seitliche Aufnahme werden die Herzen einmal am Beginn des Teststarts aufgefüllt und Z/C-Up früh gedrückt. Das ist eine Aufnahmehilfe und kein Eingriff in die ausgelieferte ROM. Die Wiederholungsprüfung startet mit nativ gesetztem Raum-3-Clear-Bit, also nach dem Besiegen der Raumgegner. Ein voriger langer Leerlaufstart ohne dieses Bit führte zu Links Tod durch Biri und zählt nicht als bestandene Interaktionsprüfung. Aufnahmen sind unbearbeitete Emulatorbilder. Ergebnisse und Helfer liegen unter validation/n64-jabu/.

Kein kompletter Dungeon-/Spieldurchlauf und kein Hardwaretest. Ein erneutes Öffnen wurde geprüft, ein vollständiger Raumwechsel hin und zurück nicht separat durchgespielt; die native persistente Prüfpunktkonfiguration und die statische Raumliste bleiben dafür maßgeblich. Alte Emulator-Save-States können noch alte Raum-/Overlay-Daten enthalten; normale Spielstände verwenden.

Original-ROM: Europa/PAL 1.0, MD5 e040de91a74b61e3201db0e2323f768a. Ergebnis-SHA256: c52e5777e6c4bb6630ef43435183660778d35df4164eebd3c751d349dec1d8ac. Den Gesamtpatch direkt auf die unveränderte ROM anwenden, nicht auf eine frühere Mod-Fassung.
