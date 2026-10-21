# Zora-Reich und Tauchspiel – V11

19 deutsche Nachrichten überarbeitet. Gelobte Texte 4007, 400C, 400D, 400F und 4010 unverändert. Der ausdrücklich beschriebene Kind-König-Text ist 401A; der erwachsene König 4013 bleibt erhalten. 4055 bleibt die Siegmeldung, 4056 die Schuppenübergabe. Startanzeige jetzt „Let's go!“. Auswahlantworten, Preise, EVENT/PERSISTENT/TEXTID, Bewegungsabläufe und feste Lesezeiten unverändert.

Kumulative Normal- und DEBUG-Patches enthalten alle bisherigen Änderungen; jeweils direkt auf die unveränderte europäische PAL-1.0-ROM anwenden. Nicht auf eine bereits gepatchte ROM. Die DEBUG-Ausgabe behält L+R halten und Z drücken.

Validierung: alle anderen Text-IDs und Sprachen bytegleich; alle funktionalen Textcodes unverändert. Kompilierte Textpuffer und PAL-Zeilenbreiten geprüft. Normal und DEBUG mit korrekter N64-Prüfsumme; sämtliche ROM-Segmentänderungen außerhalb der deutschen Texte ausschließlich als notwendige Linker-Adressverschiebungen geprüft. Beide BPS mit RomPatcher.js auf Vanilla angewendet und bytegleich mit den geprüften Builds verglichen. Laufzeitproben separat dokumentiert; kein vollständiger Spieldurchlauf.

Laufzeit: Neue Thaddäus-Einleitung, Ja-Auswahl, Abzug von 20 Rubinen, Let’s go, regulärer Zeitablauf bis zur Niederlage und gesonderte Ablehnung bei Geldmangel mit echten 4 MiB geprüft. König-Bewegung und Schuppenübergabe in dieser Runde über identische native Codes und unveränderten Spielcode geprüft, nicht gesondert durchgespielt.

Größter geänderter Rohtext: 644 von 1280 Bytes; größte dekodierte Seite (konservative Obergrenze): 140 von 200 Bytes.
