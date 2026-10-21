# Gewandicons und separate Debugversion

Die normale Version ergänzt passend orange und hellblaue Fundtext-/Inventaricons. Die Debugversion enthält dieselben kumulativen Inhalte und zusätzlich die gezielt freigeschaltete native Szenenauswahl sowie den nativen Pause-Inventar-Editor. Alle bisherigen Figuren und 1.155 eigenen deutschen Nachrichten enthalten. [Bedienung](../Debug_Bedienung.md).

Normale Ziel-SHA256: `6ee50c4dc1b9be8286651acbbe672b1063a18d6e40487b329e608ea0f4c6536f`. Debug-Ziel-SHA256: `4d3084c986d3cad88c369fdc4c2bb0eff7876c8fea98d61f2d681ddaa45b8303`. Beide BPS auf Vanilla Europa/PAL 1.0 anwenden, nicht übereinander; Original-MD5 e040de91a74b61e3201db0e2323f768a.

## Umsetzung

Iconfarben werden nach dem nativen DMA in denselben 4.096-Byte-Puffern angepaßt. Nur die dominante Stoffarbe ändert sich; neutrale Kragen-/Gürteldetails, Alpha und Schattierung bleiben erhalten. Beide Pause-Ladepfade und das Itemicon im Fundtext verwenden dieselbe Routine. Die normale altersabhängige Graufärbung nicht benutzbarer Ausrüstung bleibt erhalten. Schwarzes Schattengewandicon und Schutzwirkung bleiben unverändert. Keine weitere Textur, kein neuer Speicherpuffer und keine Veränderung der gemeinsam benutzten NPC-Farbpalette.

Debugspezifisch: Controller 1 L+R halten und Z drücken, native sichere GameState-Transition; beim Verlassen des laufenden Spiels Szenenflags sichern. B wechselt das Alter, native Altersausrüstung wird mitgewechselt; ein bisher unbenutzter Kind-Cache erhält eine gültige Grundausrüstung. Menü öffnet nicht erneut über sich selbst und unterbricht keine bereits geplante GameState-Transition. Die zwei 64DD-Testaktionen wurden aus der Liste entfernt; unenthaltene Testkarten bleiben ausgeblendet. Menütexte werden nur in diesen beiden Menüdateien übersetzt, ohne globale Übersetzungseinstellungen zu verändern.

Start und L öffnet den vorhandenen Pause-Editor. Dessen ursprünglicher Rücksprung von Zeile 0 auf die ungültige Zeile 22 wurde auf die letzte der elf gültigen Zeilen korrigiert. Ein direkt vom Titel gestarteter Testzustand bleibt über Ortswechsel erhalten und hat weiterhin keinen echten SRAM-Slot. Sram_WriteSave fängt 0xFF ab; normale Speicherplätze werden nicht umgeleitet. Save-Struktur und Prüfsummenbereiche bleiben gleich. Kein globaler DEBUG_FEATURES-Build: retail DEBUG_FEATURES=0, ursprüngliche Speicherpools und 4 MiB erhalten.

## Prüfung

Beide PAL-Builds und ROM-Prüfsummen geprüft. Vergleich aller 1.526 DMA-Einträge mit der veröffentlichten Schattengewandfassung; alle veränderten übrigen Worte müssen echte Linker-Relokationen sein. Native Symbole in den betroffenen Segmenten außerhalb der ausdrücklich erlaubten Menü-/Iconfunktionen bleiben bis auf Relokationen identisch. Sämtliche Raum-, Modell-, Kollisions-, Itemobjekt- und Dialogdaten bleiben erhalten; alle bisherigen Sprachtextdaten sind bytegleich. Hosttest der tatsächlich verwendeten C-Iconroutine an 2.048 Originalpixeln prüft Farben, neutrale Details, Alpha, Puffergrenzen und Cache-Writeback.

Die finale Debug-ROM wurde in den aufgeführten Emulatorproben mit echten 4 MiB getestet, ohne SaveContext-Injektion: Titel-Hotkey, Szenenwahl, Inventar-Editor, Navigation über die erste/letzte Zeile, Rubinänderung 150 auf 151, Rückkehr ins Spiel, wiederholtes Menüöffnen, Kakariko, Wassertempel und Brunnen sowie Wechsel Erwachsener/Kind mit korrekter Ausrüstung. Ein separat kopierter echter SRAM-Spielstand wurde über Titel/Dateiauswahl geladen; Schattengewandflag und Nachbarflag bleiben nach Orts-/Alterswechsel erhalten. Die orange/hellblauen Icons sind als Erwachsener sichtbar, als Kind greift die normale graue Nichtbenutzbarkeitsdarstellung. Kleinste gemessene zusammenhängende Spielarenareserve 67,120 Byte, kleinste Objektpufferreserve 90,864 Byte. Keine fehlgeschlagenen Belegungen oder gemeldeten Grafik-/Objektpufferüberläufe. Kein vollständiger Spieldurchlauf und kein Hardwaretest.

Beide BPS wurden mit RomPatcher.js und aktiver Quellvalidierung auf Vanilla angewandt; die Ergebnisse sind bytegleich zu den jeweiligen geprüften ROMs. Alle Bilder sind unveränderte Emulatoraufnahmen.

## Reproduzieren

Nach dem bisherigen kumulativen Build zuletzt build_shadow_tunic.py und build_tunic_icons.py ausführen. Für die separate Debugversion anschließend optional build_debug_version.py ausführen; mit dessen --restore-Schalter zu den normalen Produktionsquellen zurückkehren. PAL bauen mit VERSION=pal-1.0 COMPARE=0 PYTHON=python3, normales retail DEBUG_FEATURES=0 beibehalten. Die normalen Produktionsquellen enthalten keine freigeschalteten Debugmenüs. Quellenpaket ohne ROM, Spielstände, SRAM, Savestates, ELF oder ausführbare Programme.
