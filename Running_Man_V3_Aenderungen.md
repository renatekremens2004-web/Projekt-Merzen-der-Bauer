# Running Man V3: neuer Text vor der Rettung der Zimmerleute

Der erwachsene Running Man im Gerudo-Zelt verwendet vor der Befreiung aller Zimmerleute Text 6086. Dieser Zustand hatte noch den Originaltext. Er erhält nun den gewünschten Text über die Zimmermänner, Boris und dessen Treppensturz; der korrigierte Anfang lautet „Normalerweise bin ich der, der rennt, doch gerade eher der, der pennt.“ Das spätere Rennangebot 607D und sämtliche Renn-, Fortschritts- und Gesprächslogik bleiben erhalten.

Nur eine bestehende deutsche Nachricht geändert. Alle übrigen Nachrichten und Sprachen sowie alle funktionalen Steuerzeichen unverändert. Textpuffer und Zeilenumbruch, beide PAL-Builds, ROM-Prüfsummen und Linker-Relokationen geprüft. Die bisherigen 35 Gesprächstrennungen bleiben enthalten. Beide BPS mit RomPatcher.js auf Vanilla und aktiver Quellvalidierung angewandt und mit dem jeweiligen Ziel byteweise verglichen. Für diese reine Textänderung keine neue Emulatorprobe und kein vollständiger Spieldurchlauf.

Je einen kumulativen BPS-Patch auf die unveränderte Europa/PAL-1.0-ROM anwenden, nicht auf eine bereits gepatchte Datei. Original-MD5: e040de91a74b61e3201db0e2323f768a. Deutsch wählen. Normal und Debug haben denselben Spielinhalt; die funktionierende Debugsteuerung bleibt unverändert.

Alle bisherigen Änderungen enthalten. Letzter normaler Textbuilder ist jetzt tools/build_running_man_prerescue.py, nach build_no_wayfinding_dialogue.py und vor optional build_debug_version.py. Kein neuer Schauspieler und keine Änderung an Modellen, Kollisionen oder Speicherpools.

normal Ziel-SHA256: a91acf14bacd7b29e3f1c9e6fc1a72ad249edd46eeb9cdb84234795cccbc69ca

debug Ziel-SHA256: e651e7fa0afc5a686180c139209e669a13259d3f24607cbe33a4752900b5784a
