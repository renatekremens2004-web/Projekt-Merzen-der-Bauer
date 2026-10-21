# Charakterbewegung V4

Alle hinzugefügten lebenden Figuren auf vorhandene Bewegungspfade geprüft. Die meisten Gäste besitzen bereits eine entspannte Grundpose und Kopf-/Armbewegungen. Triangle Guy war die verbleibende komplett starre Figur und erhält eine eigene sparsame Bewegung.

## Triangle Guy

Arme aus der T-Pose abgesenkt; kleine Ruhebewegung, sanftes Drehen und eine asymmetrische Hand-/Armgeste während des eigenen Gesprächs. Keine Größenänderung und keine Skalierung der Körperteile. Gesicht, Originaltext einschließlich Triforce-Zusatz, Standort, Ansprechbedingungen und Boss-/Kameralogik bleiben erhalten. Vorhandene Geometrie wird in drei starre Gruppen gegliedert: Körper sowie zwei Arme mit Händen. Kein Polygon hinzugefügt: weiterhin 1102 Dreiecke. Drei statt einer Grafikmatrix bedeuten 128 zusätzliche Bytes im bestehenden Grafikpuffer pro Zeichnung. Keine neuen Schauspieler, Objektslots, Texturen oder vergrößerten Speicherpools.

## Vorhandene Bewegungen geprüft und erhalten

- Doc und Marty: Kopfbewegungen und Armgesten an beiden Standorten.
- Mystery Inc.: Shaggy, Fred, Daphne, Velma und Scooby besitzen eigene Kopf-/Arm- bzw. Schwanzbewegungen.
- Fanboy, Chum Chum, Ben 10 und Crocker: Kopf- und Armbewegungen; Auftritte und Auftau-Bedingungen unverändert.
- Pepsiman, Mauzi, Jimmy Neutron, Mr. Mackey, Shrek und Mr. Monopoly: bestehende Bewegungen im Stand und beim Sprechen.
- Wawario, Wawaluigi, beide Yellow-Guys und Wario: bestehende Kopf-/Armgesten.
- Jabba: sparsame Kopfbewegung passend zur liegenden/sitzenden Figur.
- Lebender Kenny: dezentes Schwingen; seine tote Version bleibt ausdrücklich statisch.
- Wallace als Kind: Kopf-/Armbewegungen. Erwachsener Wallace: vorhandene Bewegungen, Laufanimation und Gesten einschließlich Weisen-/Creditsauftritten beibehalten.
- Thaddäus, Waluigi, Mr. Bean, Robert Habeck, Krabbelminen-Frau als Waldweise sowie Burns/Smithers im Phantomkampf: vorhandene Skelett-/Szenenanimationen erhalten.
- Tripple T behält Auftauch- und anschließende Tanzanimation; Okto seine vorhandene freundliche Oktorok-Bewegung.

Toter Kenny, flacher Thaddäus, Fundstücke, Fahrzeuge und Modelle von Gegenständen bleiben absichtlich statisch. Keine willkürliche Neuanimation der bereits funktionierenden Figuren oder Credits-Sitzpose.

## Prüfung

Quellvergleich: ausschließlich neue Triangle-Guy-Zeichenfunktion und deren Zuweisung; kein Eingriff in Update-, Gesprächs-, Boss-, Kollisions- oder Speicherlogik. Die vollständige Textdatei ist bytegleich mit Running Man V3, einschließlich der zuletzt ergänzten 6086. Beide PAL-Builds mit gültiger N64-Prüfsumme. DMA-Segmente mit V3 verglichen: abgesehen von Elf_Msg2 und dem Triangle-Modell im Ganon-Raum sind Änderungen einzeln als Linker-Relokationen geprüft.

Laufzeitprobe der normalen Endfassung mit tatsächlichen 4 MiB und aktivierter Grafik-Clipping-Option: Ganon-Enthüllung, Annäherung über Controller und beide Gesprächsteile 608A. Keine Figuren für das Bild versetzt und keine Boss-/Animationszustände injiziert; nur vorher vorhandene Spieler-/Fortschritts-Testdatei für den Einstieg. Objektspeicher meldet 58224 Bytes frei. Keine ungültigen Grafikkommandos, Vertexfehler oder Abstürze in dieser Probe. Gesicht und abgesenkte Arme anhand der aufgenommenen Frames kontrolliert. 18 Sekunden kontinuierliche MP4 bei PAL 50/3 Spielbildern pro Sekunde, ohne Ton. Dies ist eine gezielte Probe, kein vollständiger Spieldurchlauf und kein Konsolentest. Die übrigen vorhandenen Animationen wurden in diesem Schritt anhand ihrer Quellpfade geprüft, nicht alle erneut im Emulator abgespielt.

Beide BPS zusätzlich mit RomPatcher.js und aktiver Quellvalidierung auf Vanilla angewandt und byteweise gegen die gebauten Ziele geprüft.

## Anwendung und Quellen

Je einen kumulativen BPS-Gesamtpatch auf die unveränderte Europa/PAL-1.0-ROM anwenden, nicht auf eine bereits gepatchte ROM. Original-MD5 e040de91a74b61e3201db0e2323f768a. Deutsch wählen. Alle bisherigen Änderungen enthalten. Normale und DEBUG-Fassung haben dieselben Spielinhalte; Debugsteuerung bleibt unverändert.

Letzter normaler Builder: tools/build_character_life.py nach build_running_man_prerescue.py und vor optional build_debug_version.py. Das Quellenarchiv enthält den letzten Stand, den neuen Builder/Zeichenhelfer, die Prüfungen und die vorherige Actor-Quelldatei zur reproduzierbaren Anwendung. Keine ROMs, Saves, SRAM, Savestates, ELF oder ausführbaren Programme.

normal Ziel-SHA256: c37e6b381dbfb9cd7e883b3bcc2b097c86f4ba4ce7e79be91db3641cbedbc61e

debug Ziel-SHA256: 85ae211c86db76bebc6c55826797529ee63426a76a3cbf5530d5679eac676302
