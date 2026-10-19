# Wallace in Dodongos Höhle

## Verhalten und Standort

Ein zusätzlicher, ansprechbarer NPC am westlichen Rand des Bombenblumen-Treppenraums, Raum 2, Position (-2250, 0, -1160). Er steht abseits von Bombenblumen, Türen, Treppe und Laufweg. Es ist weder der Eingangsraum noch die große Eingangshalle. Sein Standort ist Teil der veröffentlichten Raumdatei, nicht für Bilder verschoben. Nur Kind-Link und deutsche Sprache. Als Erwachsener wird der Actor vor Zeichnen und Teilnahme an Kollisionen entfernt. Die zerstörbare Treppe, Bombenblumen, Gegner und Rätsel behalten ihre Originaldaten.

Wallace läßt sich über A normal ansprechen, hat eine blaue freundliche Zielmarkierung, keine Angriffsfunktion und keine Schadensannahme. Eine zivile OC-Zylinderkollision läßt ihn als festen NPC im Raum stehen. Kein Gegnerstatus, kein Zusammenhang mit Raum-Fertig-Markierung, keine Änderungen an Schaltern oder Questbelohnungen. Das Gespräch kann beliebig wiederholt werden.

Er erzählt über sein Interesse an den Goronen, Forschung zum Überleben unter extremen Klimabedingungen des Todesbergs und wie Merz' Kohleabbaufiasko ihn in der Höhle festgesetzt hat. Nachricht 019A, fünf manuell weitergeschaltete Seiten, 460 kompilierte Bytes unter dem nativen 1280-Byte-Limit. Keine vorhandene eigene Nachricht ersetzt. 749 eigene Story-Nachrichten plus 15 reine Namensänderungen, insgesamt 764 bearbeitete deutsche Nachrichten. Feste Lesezeiten unverändert.

## Modell, Animation und Licht

Gewählt wurde wallace.zip/source/wallacerig.blend: 4249 Dreiecke und vier kleine Texturen. wallace (2).zip enthält 7148 Dreiecke und größere Texturen. wallace (1).zip war wegen des Übertragungslimits von 32 MiB nicht zugänglich. Die funktionsfähige gewählte Variante konnte vollständig eingelesen werden; der beschädigte optionale Shape-Key-Verweis wurde beim Offline-Export verworfen. Fremde Blender-Skripte wurden nicht ausgeführt.

N64-Modell: 1444 Dreiecke, vier eigene starre Teile (Körper, Kopf, linker/rechter Arm), 90 Spieleinheiten Höhe. Arme für eine natürliche Ruhehaltung offline abgesenkt. Dezentes Kopfnicken und Armschwingen, beim Gespräch zusätzliche kleine Armgesten. Nur Rotationen um feste eigene Achsen: keine fremden Knochenlängen, Streckung oder Scherung. Keine Portierung des unnötig großen 212-Knochen-Controller-Rigs. Vier CI4-Texturen (dreimal 64×64, einmal 16×16), native Szenenbeleuchtung mit Oberflächennormalen und Bodenschatten. Keine künstliche Vollbeleuchtung.

Das Modell liegt im Raumsegment und benötigt keinen zusätzlichen Objektbank-Eintrag. Der bestehende Elf_Msg2-Actor hat einen streng nach Szene/Raum/Parametern begrenzten NPC-Modus. Andere Navi-Prüfstellen, N64-Konsole und Majoras Maske behalten ihre bisherigen Pfade. Der optionale Zylinder vergrößert die Instanzstruktur von Elf_Msg2; der bisherige Präfix bleibt erhalten und das Profil allokiert die vollständige neue Größe. Beim Zeichnen wird auch während eines Raumwechsels das zu Wallace gehörende aktuelle/vorherige Raumsegment gewählt und anschließend die Segmentzuordnung wiederhergestellt.

## Prüfungen

Finale ROM-SHA256: `1bdb74d9e7dc2f128d0313bd6e4d6aa95dc908ceb9f65a7f40031df2f9aba838`. Vergleich mit dem veröffentlichten Wald-/Navi-/Salia-Build `0fbfcd1d49f9196be409e7d91c8384b35cc7b35d168865392892bc0a0b8a40f8`. Alle 1509 komprimierten Segmente inklusive CIC-6105-Prüfsumme und Roundtrip geprüft; 1267 Segmente bytegleich. Intendierte Änderungen ausschließlich in makerom/dmadata, deutscher Nachricht 019A samt Zeigertabelle, ovl_Elf_Msg2 und ddan_room_2. Sonstige Unterschiede sind streng überprüfte Linker-Relokationen. Frühere Modelle, andere Räume und vorhandene Texte bleiben erhalten. Sämtliche 764 Textpuffer, native Steuerbefehle und feste Zeiten geprüft.

Der Raum 2 wächst von 32160 auf 71200 Bytes. Der native gemeinsame Raum-Puffer, über alle 23 Verbindungen berechnet, wächst von 159216 auf 184000 Bytes: 24784 Bytes zusätzlich. Geprüft wird die tatsächliche engineeigene Berechnung der größtmöglichen verbundenen Raumkombination. Keine neue Objektbank-Reservierung.

Fünf finale Mupen64Plus-/GLideN64-Proben mit tatsächlich 4 MiB: normales Kindesgespräch mit allen fünf Seiten und Wiederansprache; Erwachsener ohne Wallace; Kind nach gesetzter Raum-Fertig-Markierung; englische Sprache ohne deutschen Spezial-NPC; nativ durch die Tür hinausgehen und wieder zurück. Der Raumwechsel-Lauf bereitet den Spieler am Korridor und den gelösten Türzustand vor und steuert anschließend nur normale Stick-/A-Eingaben; er versetzt keine NPCs und ruft keine Raum- oder Dialogfunktion direkt auf. Wallace wird entladen und bei der Rückkehr neu gespawnt. Alle Läufe schließen ohne Speicherfehler ab. Einzelheiten und Minima stehen in validation/wallace/runtime-checks.json.

Die anfängliche Händler-Nische wurde verworfen, weil die beiden Deku-Händler Link während des Gesprächs beschießen konnten. Ein verworfener Teleport-Test hat keinen Raumwechsel erreicht und wird nicht als bestandener Nachweis gewertet. Die finalen Tests verwenden den veröffentlichten Treppenraum-Standort. Spielerstarts/Fortschritt sind vorbereitet; Bilder sind unveränderte Emulator-PNGs. Kein vollständiger Spieldurchlauf und kein Test auf echter N64-Hardware. RomPatcher.js validiert die Original-ROM und erzeugt bytegleich die finale ROM.

## Neubau

Den vollständigen README-Ablauf anwenden; build_wallace.py nach den anderen Modell-/Raumbauern und build_wald_dialoge.py, build_sage_names.py abschließend. Der produktive Neubau benötigt wallace_source.json und models/wallace/*.png, keine Blender-Datei oder Blender-Ausführung. export_wallace.py dokumentiert nur die optionale erneute Offline-Ableitung aus der Nutzerdatei. verify_wallace.py OOT BASELINE.z64 erwartet die vorangegangene Wald-/Navi-/Salia-Vergleichs-ROM und ihre baseline.map. Keine vollständigen ROMs, Saves oder ELF-Dateien im öffentlichen Quellpaket.
