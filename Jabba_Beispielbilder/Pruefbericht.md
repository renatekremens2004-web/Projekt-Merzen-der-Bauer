# Jabba im Hyrule-Feld

Gesamtpatch gegen unveränderte Europa/PAL 1.0, Vanilla-MD5 `e040de91a74b61e3201db0e2323f768a`, Ziel-SHA256 `d090fc67ed85e5416181ead5250af5996b86b58e3d05c7f7adf2cde4b6a6fdf6`. Alle bisherigen Änderungen enthalten, weiterhin 40 MiB ROM und tatsächliche 4 MiB N64-RAM.

## Modell und Auftritt

Bereitgestellte GLB ohne Rig mit 493.466 Dreiecken auf 2.391 reduziert: Körper 2.200, getrennte Augen 95/96. Die erste direkte Vereinfachung zerhackte Kontur und UVs; finale Fassung verwendet eine geschlossene Oberfläche mit Voxeln 0,085 und anschließendem gleichmäßigen Dreiecksbudget. Diffuse Originalfarben vom unveränderten dichten Modell auf eigene Kopf-/Körperatlanten übertragen. Originale Augenpositionen und Augen-UVs erhalten. Drei CI4-Texturen je 64×64 mit 16 Farben, native Beleuchtung/Nebel/Tiefentest. Höhe 78, Breite etwa 163, Tiefe 92 Spieleinheiten; nur gleichmäßige Skalierung. Zwei eigene starre Gruppen mit sehr kleiner Kopfrotation, keine Animation durch nichtuniforme Gliedmaßenskalierung.

Jabba bei −500/0/2400 seitlich des Weges Richtung Hyrule-Stadt. Kollisionsradius 42, Höhe 76, normale OC-Körperkollision, kein Angriff oder Treffer, kein Weg-/Questschalter. Fest bleibender Körper/Schwanz, keine für Bilder versetzte Figur. Normales A-Gespräch und native Kamera. Nur Kind/deutsch.

Die zwei normalen Kinder-Listen im Feld entsprechen dem Fortschritt vor/nach den drei Steinen; die Spielzeit bestimmt dort weiter Tag und Nacht. Beide Listen erhalten genau einen NPC und ein Objekt. Erwachsene sowie alle Spezial-, Flucht- und Abspann-Listen bleiben erhalten. Deshalb auch nach den drei Steinen als Kind ansprechbar, ohne in die Fluchtsequenz hineinzuragen.

## Speicher

Die erste Ablage im Raum ließ den Akteur im Feld nicht erscheinen. Die finale Fassung registriert deshalb ein eigenes Objekt `object_jabba`, ID 0x0192, und hängt dessen komprimiertes DMA-Segment an das Ende. Alle bisherigen Objekt-IDs und DMA-Indizes bleiben erhalten. Modell nur in den beiden normalen Kinder-Objektlisten; keine zusätzliche Aufnahme in Zwischensequenzen. Originale Objektsegmente unverändert. Grafik bindet das eigene geladene Segment 6 und stellt es sowie Segment 13 anschließend wieder her.

Im reservierten Objektpuffer bleibt in den normalen Kinder-Proben mindestens 178.688 Byte frei. Maximal 13 von 19 Objekt-Slots belegt. Raumpuffer 86.608 Byte einschließlich der kleinen zusätzlichen Listen, statt der teuren Modellablage dort. In allen sieben Proben meldet die native Zelda-Arena null fehlgeschlagene Belegungen; größte freie zusammenhängende Arena-Fläche mindestens 46,944 Byte. Fluchtprobe ebenfalls mit 4 MiB, ohne Jabba oder sein Objekt. Nicht mit ungenutztem Objektpuffer gleichzusetzen: Objektbank und Arena werden getrennt geprüft.

## Texte und Tabellen

Neue private ID 71B3 mit fünf manuell bestätigten Seiten; erst der vom Nutzer gelieferte huttische Satz, dann die deutsche Klammerübersetzung. Deutsche Großschreibung und „BAT“ wortgetreu. Kein Eingriff in Lesetempo oder feste Zeiten. Alle bisherigen Nachrichten in allen Sprachen sowohl als Quelle als auch kompiliert unverändert. Insgesamt 1.031 eigene Nachrichten; alle Roh-/Seitenpuffer geprüft.

Die neue Nachricht steht physisch vor der bisherigen letzten Nachricht 71B2. PAL liest die DMA-Länge aus dem nächsten Spracheintrag: Folgezeiger in Englisch, Deutsch und Französisch ausdrücklich geprüft, positive Länge unter 1.280 Byte. Kein nativer Dialogplatz zweckentfremdet. Neue englische/französische Reserveeinträge enthalten nur „Jabba.“ und sind wegen der Sprachprüfung nicht über diesen NPC zugänglich. Der Host-Builder `add_private_message` unterstützt dieselbe explizite Registrierung bei einem vollständigen Story-Neubau.

Alle 1.510 komprimierten Segmente gegen den unkomprimierten Build sowie CIC-6105-Prüfsumme geprüft. 3.664 native Kernfunktionen/Datensymbole bytegleich oder ausschließlich echte MIPS-Linker-Relokationen. Nachrichtentabellen und Objekttabelle um jeweils den einen neuen Eintrag ergänzt. Der Objektanzahlwert wächst auf 0x0193; beim Laden der Händler werden die bisherigen OBJECT_ID_MAX-Platzhalter konsistent von 0x0192 auf 0x0193 aktualisiert (16 geprüfte Wörter). Bestehende Objektumfangswerte und sämtliche Boß-/Charaktermodelle erhalten. Im Elf_Msg2-Overlay kommen vier private Helfer und die drei begrenzten Initialisierungs-/Update-/Zerstörungszweige hinzu; alle anderen Funktionen unverändert. Keine Änderungen an bestehenden Kern-Quelldateien oder an der Textsuchfunktion.

## Laufzeit und Lieferung

Sieben abgeschlossene Proben: Kind tags/nachts, jeweils vor/nach den drei Steinen; Erwachsener; englische Kinder-Fassung; native Fluchtsequenz. Vier Kinder-Gespräche geöffnet und durchgeblättert. Alle tatsächliche 4 MiB, keine beobachteten Grafikbefehlsfehler, Überläufe oder fehlgeschlagenen nativen Speicherbelegungen in diesen Proben. Bilder unveränderte Emulatoraufnahmen genau dieses Builds; lokale Spielstands-Fixtures bereiten nur Spieler/Fortschritt vor. Kein kompletter Durchlauf oder Hardwaretest in diesem Schritt.

RomPatcher.js mit aktiver Quellvalidierung erzeugt bytegenau die geprüfte ROM. BPS auf unveränderte Vanilla PAL 1.0 anwenden. Keine ROM, Spielstände, Savestates, RAM-Abzüge, ausführbare Dateien oder die dichte GLB veröffentlicht. Vorbereitete Modell-JSON/PNGs und Builder reichen zum Neubau.

Letzter Schritt nach `build_ben_ice.py`: `python3 tools/build_jabba.py <oot>`, danach normal bauen/komprimieren. Benötigte Quell-Snapshots einschließlich ursprünglicher Objekttabelle und Spec enthalten. Offline-Neuableitung mit Blender 4.3.2: `prepare_jabba_lowpoly.py`, `bake_jabba_colors.py`, `export_jabba.py`, jeweils mit `-- <arbeitsordner>` und entpacktem Nutzer-Upload unter `input/`. Die Vergleichsprüfung benötigt die private vorige ROM/ELF und Textobjekte; sie werden nicht mitgeliefert.
