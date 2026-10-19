# LEGO X-Wing und der vergessliche Kakariko-Bewohner

Geliefertes LEGO-Modell: 4270 gültige Dreiecke, 24 Spieleinheiten Spannweite, einheitliche Skalierung. Szenenlicht, Normalen, Materialfarben, Z-Puffer und Nebel. Raum 0 im Schattentempel, (-1750,-63,-300). Dekoration ohne Collider oder Item-/Rätselwirkung. Modelle und NPCs werden nicht zu Aufnahmezwecken versetzt.

Der Mann im blauen Hemd unten im erwachsenen Kakariko, native Position (-876,0,572), erhält 507B/507C vor/nach dem Schattenamulett. Erste Seite: „Scheiße, ich hab' meinen Lego X-Wing im Schattentempel liegen lassen!“ Zweite vorhandene Seite: „Und die Bauanleitung ist natürlich auch noch drin!“ Insgesamt 599 Nachrichten. Native Kontrollen und feste Lese-/Kamerazeiten bleiben erhalten. Die Dachbewohner-Nachrichten 5050–5056 bleiben gegenüber der vorherigen Veröffentlichung bytegleich.

## Statische Prüfung

Build, CIC-6105-Prüfsumme und Kompression aller 1509 Segmente geprüft. Vergleich mit dem veröffentlichten N64-in-Jabu-Gesamtpatch. Alle übrigen Änderungen müssen geprüfte Linker-Relokationen sein. Bean-, Thaddäus-, Habeck-, Nintendo-64-Objekte sowie Kakarikos Raumdatei sind bytegleich. Alle ursprünglichen Bytes von Schattentempel-Raum 0 bleiben erhalten, außer dem letzten 8-Byte-Endbefehl seiner opaque Raum-Displayliste, der zur angehängten Modell-Displayliste verzweigt. Keine neuen Actors und keine Änderungen an Kollision, Türen, Truhen oder Gegnern. Alle 599 Textkontrollsequenzen und Textpuffer geprüft. Keine Änderungen am Quellcode des Dorfmannes oder des Dachbewohners.

## Laufzeitprüfung

Gezielte Starts mit derselben Produktions-ROM, 4 MB, Mupen64Plus/GLideN64; EnableClipping=True, EnableCustomSettings=False. Modellansichten im nativen Raum, Gespräch vor/nach Schattenamulett sowie englischer Text als Gegenprobe. Teststarts setzen nur normalen Fortschritt, Sprache, Alter und Links Position; Figuren und Modell bleiben an ihren Produktionspositionen. Native automatisch ausgelöste Schädelwand-Texte werden per A geschlossen. Bilder sind unbearbeitete Emulatoraufnahmen. Prüfprotokolle und Helfer: validation/xwing/.

Kein vollständiger Dungeon-/Spieldurchlauf oder N64-Hardwaretest. Der Text ist tagsüber draußen verfügbar; nachts verwendet der Bewohner seine ursprüngliche Innenraumroute. Alte Emulator-Save-States können alte Daten enthalten; normale Spielstände verwenden.

Original Europa/PAL 1.0: MD5 e040de91a74b61e3201db0e2323f768a. Den Gesamtpatch in RomPatcher.js direkt auf die unveränderte Original-ROM anwenden, nicht auf eine frühere Mod. Produktions-SHA256: c78155650c054c3111d1e97119f63c8070f951cbcb04390324d681283de1c09b.
