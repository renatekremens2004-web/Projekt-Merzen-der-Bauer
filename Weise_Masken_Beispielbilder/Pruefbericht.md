# Weisen-Dialoge und Maskenreaktionen

205 deutsche Nachrichten gegenüber dem Wallace-Gesamtpatch geändert; insgesamt 954 eigene deutsche Story-Nachrichten. Thaddäus: Wassertempel, Halle, Abschied und Wassersiegel. Waluigi: Vorstellung, beide Merz-Antworten, Krafthandschuh-Auftrag, Ablehnung, Entführung, Eisenritter-Enthüllung, Halle und Geistersiegel. Begleittexte, männliche Bezeichnungen und Amulettinfos angepaßt. Junge Ruto bleibt Ruto. Alle vorherigen Modelle, Räume und Kapitel bleiben enthalten.

157 neue Masken-Nachrichten, darunter 58 getrennte unterstützende Gerudo-Reaktionsgruppen und Thaddäus' zusätzliche eigene Antwort. Andere Masken erhalten mehrere passende Sprüche und individuelle Reaktionen, nicht jeder NPC für jede Maske einen einzigartigen Text. Die 60×9-Zuordnung bleibt sprachabhängig, ursprüngliche Nullstellen und spezielle Masken-Verkaufsabläufe bleiben erhalten. Der Zora-Wal-Spruch setzt den Zora-Saphir voraus; ein einzelner Kokiri spricht mit der Maske des Wissens die 50 Rubine an.

## Validierung

ROM-SHA256 `03fd8d7124b11ea661b9d2b506a2c61ca076ce2279029557edcceda69c55aaa6`. 32 MiB, CIC-6105 korrekt, alle 1509 komprimierten Segmente gegen den unkomprimierten Neubau geprüft. Gegen veröffentlichte Wallace-Fassung `1bdb74d9e7dc2f128d0313bd6e4d6aa95dc908ceb9f65a7f40031df2f9aba838`: Modelle und Räume bytegleich; übrige nicht beabsichtigte Unterschiede streng als Linker-Relokationen geprüft. Änderungen in Code ausschließlich neue deutsche Maskentabelle, begrenzte Abfragefunktion und Kokiri-/Tauchspiel-Ausnahmen. Quellvergleich bestätigt unveränderte übrige Questlogik. Englische/französische Nachrichtensegmente bytegleich. Ursprüngliche Maskentabelle unverändert, deutsche Nullstellen erhalten. Neue Tabelle 1080 Bytes plus 8 Bytes Ausrichtung.

Alle 954 Textpuffer, Textketten, Antwortsteuerungen und festen Szenenzeiten geprüft. Lange manuell weitergeschaltete Gespräche in zusätzliche Seiten aufgeteilt und nötigenfalls gestrafft, insbesondere 403E und 6023. Kein Vergrößern des nativen Textpuffers. Keine Änderung fester Lesezeiten. Namensersetzung überspringt ausdrücklich verfaßte Storytexte.

RomPatcher.js validiert die unveränderte Original-ROM (MD5 e040de91a74b61e3201db0e2323f768a) und erzeugt bytegleich die finale ROM. Vollständige Berichte unter validation/weise-masken.

11 abgeschlossene gezielte Emulatorläufe mit Dialogausgabe sind in runtime-checks.json dokumentiert. Jeder Eintrag nennt tatsächlich getesteten ROM-Hash und Text-IDs. Frühere Proben wurden vor den letzten vier Geschlechts-/Namenskorrekturen an den Hexentexten 6031–6034 aufgezeichnet; sie sind ausdrücklich als solche erkennbar. last-wording-delta.json bestätigt, daß sich seit diesen Proben ausschließlich diese vier deutschen Nachrichten geändert haben. Die abschließende statische Prüfung gilt für den finalen Hash. Nur vollständige Läufe mit erreichter Dialogausgabe werden gezählt; verworfene Start-/Kamera-/NPC-Auswahlproben nicht als Nachweis des beabsichtigten Zielgesprächs verwenden.

Mupen64Plus/GLideN64, tatsächliche 4 MiB. Fortschritt, Inventar und Spielerstarts vorbereitet; NPCs bleiben an ihren nativen Positionen. Gespräche über normale A-/C-Eingaben, keine direkt gestarteten Textboxen. Bilder sind unveränderte Emulator-PNGs; Aufnahmen.json nennt die jeweilige Testrevision. Kein kompletter Spieldurchlauf oder N64-Hardwaretest.

## Neubau

README-Reihenfolge verwenden: build_story.py liest alle Story-JSONs, build_habeck.py stellt die vorhandenen sicheren TEXTID-Ketten her, build_mask_reactions.py ergänzt Zuordnungen und begrenzte Actor-Ausnahmen, build_sage_names.py abschließend. Die beiden aktuellen Dialogübersichten werden aus dem gebauten Textbestand exportiert, nicht aus einem Vorschlag.
