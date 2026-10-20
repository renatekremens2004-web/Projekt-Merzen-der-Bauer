# LEGO Naboo-Starfighter statt X-Wing

Kumulativer Gesamtpatch auf unveränderte Europa/PAL 1.0. Vanilla-MD5 `e040de91a74b61e3201db0e2323f768a`; Ziel-SHA256 `988d540cb190bf093b1e9e5a1de7ec883107ac75ab52add553b4d8514f388b19`. Alle bisherigen Änderungen einschließlich Kenny und Stiefelkürzeln enthalten.

Der LEGO-X-Wing im Schattentempel wurde vollständig durch den vom Nutzer gelieferten LEGO-Naboo-Starfighter ersetzt. Gleicher Standort am Boden in Raum 0, keine zusätzliche Kollision, Actor- oder Objekt-ID. Der alte gXWingDL ist im fertigen Build nicht vorhanden. Native Raumgeometrie, Türen, Fallen, Wege, Licht, Nebel und Tiefentest bleiben erhalten.

Spielzeug mit natürlichen Proportionen: 36 Spieleinheiten lang, 19,24 breit und 5,47 hoch. Die importierten 116.755 Dreiecke wurden durch Vereinigung überlappender Bausteinschalen und anschließende Reduktion auf 1.400 Dreiecke reduziert. Gelb, Silber, dunkler Cockpitbereich und ursprüngliche Silhouette stammen aus den Materialfarben der Nutzerdatei. Keine Textur benötigt. Original-OBJ-SHA256: `52ea7c943a792ac9dcc908350e52bdb6d86dec95f8e5a3ab238ebf6cd27fb9a3`.

Kakariko-NPC, deutsche Nachrichten **507B und 507C**:

„Scheiße, ich hab' meinen Lego Naboo-Starfighter im Schattentempel liegen lassen!“

Zweite Seite bleibt: „Und die Bauanleitung ist natürlich auch noch drin!“

Manueller Seitenwechsel und Lesetempo unverändert. Beide Fortschrittsvarianten im Emulator durch natürliches Ansprechen getestet. Alle anderen bisherigen Dialoge in allen drei PAL-Sprachen als Quelle und kompiliert unverändert. Keine neuen Nachrichten-IDs.

Vier gezielte Emulatorproben mit echten 4 MiB RAM: Starfighter vor Ort, speicherkritischer Raum 9, Kakariko vor/nach Schattenamulett. Keine fehlgeschlagene native Speicherbelegung oder Grafikpufferfehler. Größte freie zusammenhängende Arena-Fläche im kritischen Raum mindestens 105,904 Byte. Gemeinsamer Raumpuffer sinkt von 259.680 auf 162.672 Byte; Objektpuffer bleibt unverändert. Sämtliche 1.512 komprimierten Segmente und CIC-6105-Prüfsumme geprüft. 3.664 Kernsymbole unverändert bzw. ausschließlich durch Linker-Relokationen angepaßt. Nur deutsche Nachrichten 507B/C und Raum-0-Darstellung geändert. RomPatcher.js mit Quellvalidierung liefert exakt die geprüfte Ziel-ROM. Kein vollständiger Durchlauf oder Hardwaretest.

**Baufolge:** `tools/build_naboo.py` unbedingt als letzten Builder **nach build_kenny.py** ausführen; ältere Builder stellen Zwischenstände wieder her. Beispiel: `python3 tools/build_naboo.py /pfad/zur/oot-decomp`, dann regulär bauen und komprimieren. Vorbereitete `tools/naboo_source.json` reicht für diesen Bau. Optionaler Neu-Export des Nutzer-OBJ/MTL mit Blender und `tools/export_naboo.py <Arbeitsordner>`; Upload unter input/LEGO_NabooShip. Der Export benötigt die ursprünglichen Nutzerdateien. Nativer Raum-Ausgangszustand unter tools/originals/xwing im Quellenpaket enthalten.

Quellenpaket enthält keinen ROM, Spielstand, Savestate, RAM-Abzug oder ausführbares Programm. Bilder sind unveränderte echte Emulatoraufnahmen des Ziel-Builds.
