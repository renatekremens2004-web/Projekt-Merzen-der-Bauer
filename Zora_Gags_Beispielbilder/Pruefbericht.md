# Zwei neue Zora-Gags

Genau zwei bestehende deutsche Einträge ersetzt, beide nach Erhalt des Zora-Saphirs:

- 402E: Der Tierarzt-Nachtrag entfällt. Stattdessen bemerkt der Zora, wie sau crazy die Musik für eine Sekunde klingt, wenn man Zoras Höhle verläßt.
- 402D: Mein allgemeiner Ruto-Nachtrag entfällt. Stattdessen kennt der Zora Mido, findet ihn einen Wichser und erzählt, daß Mido ausgerechnet ihm das Schwimmen erklären wollte.

Die nativen Gruppen bleiben bestehen: Zora-Typen 0/2/4 verwenden nach Jabu-Jabu 402D, Typen 1/3/5 verwenden 402E. Es werden keine NPCs versetzt, keine neuen Dialog-IDs angelegt und keine Musikdaten verändert. Der Gag handelt von der Musik; er erzeugt keinen zusätzlichen Audioeffekt.

Alle anderen Einträge dieses Kapitels sind im JSON-Vergleich identisch. Somit bleiben insbesondere Rockmusik, die Frauen-Frage, König Zoras Klimaanlagen, Rutos Geschichte und Thaddäus erhalten. Beide Seitenzahlen, Spielernamen und funktionalen Kontrollen bleiben erhalten. Insgesamt weiterhin 599 deutsche Nachrichten.

Die fertigen ROM-Nachrichtentabellen wurden mit der veröffentlichten Navi-Roast-Fassung verglichen: genau 402D/402E geändert, alle übrigen 2113 deutschen Nachrichtentexte bytegleich ohne Padding. Der ausführbare Code bleibt bytegleich; nur die deutsche Zeigertabelle folgt den neuen Textlängen. Alle 1509 Segmente, die CIC-Prüfsumme, 599 Textkontrollsequenzen und Textpuffer sowie RomPatcher.js geprüft. Alte Rechtschreibung mit verläßt.

Gezielte Laufzeitprüfung auf derselben Produktions-ROM, 4 MB, GLideN64 EnableClipping=True und EnableCustomSettings=False: native Zoras 0 und 1 in Raum 1 von Zoras Reich nach Erhalt des Saphirs; dazu englische Gegenprobe. Für die Aufnahme wird nur Link vor den nativen Gesprächspartner gestellt. Figuren und Kameras werden nicht versetzt. Kein kompletter Spieldurchlauf oder Hardwaretest. Unbearbeitete Bilder: previews/zora-gags/; Protokolle: validation/zora-gags/.

Gesamtpatch direkt auf die unveränderte Europa/PAL-1.0-ROM anwenden, nicht auf eine frühere Mod. Original-MD5: e040de91a74b61e3201db0e2323f768a. Normale Spielstände statt alter Emulator-Save-States verwenden. Normaler Spielstart, alle bisherigen Änderungen enthalten. Produktions-SHA256: e5265a6b63a509db46442920f6500c2f8a1dfd377ad3e7b277d42228a63c3db8.
