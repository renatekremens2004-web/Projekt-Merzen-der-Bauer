# Sechs neue Alltagsgags in Hyrule und Kakariko

Alle sechs neuen Nutzerideen auf bisher originale NPC-Gespräche verteilt. Genau neun deutsche Nachrichteneinträge geändert; alle 626 vorherigen eigenen Texte bleiben bytegleich. Insgesamt 635 bearbeitete Nachrichten.

| Figur | Text-IDs | Erreichbarkeit |
| --- | --- | --- |
| Zimmermann Typ 2, Kakariko | 506A / 506B | Milchwerbung: tagsüber draußen, nachts im Gasthaus; zwei/eine native Seiten. |
| Hyrules Marktplatz-Nachtwachen | 7003 | Autobatterien für Zitteraale. Die zwei Wachen teilen den Eintrag nativ. |
| Alter Besucher im Hyrule-Magieladen | 7120 | König Zoras geschmolzene Eisbestellung. |
| Besucher im Hyrule-Basar | 7121 | Beschwerde über Mr. Tentakels unfaires Minispiel. |
| Zimmermann Typ 3, Kakariko | 5077 / 5078 | Krabbelminen-Fan: tagsüber draußen, nachts im Gasthaus. TIME und der Hinweis auf Boris am Abend bleiben erhalten. |
| Wache am Schloßtor | 7002 / 7006 | Mond-Gag nachts bzw. nach den drei Steinen. Der Hinweis auf das gesperrte Schloß folgt weiterhin. Zollpreis/Ja-Nein und Toröffnung bleiben unangetastet. |

Die vorherigen Dialoge der beiden Zimmerleute, Ladenbesucher, Nachtwachen und Schloßtorwache hatten keine eigenen Anpassungen. Andere NPC-Instanzen mit demselben Modell hatten teilweise bereits eigene Texte. Keine NPCs versetzt oder angehalten, keine neuen Actor-Zweige, keine Änderungen an Kameras, Licht, Preisen oder Aufgaben. Alle Texte in alter Rechtschreibung; schnelleres Schreibtempo erhalten. Keine festen Lese-/Szenenzeiten geändert.

## Prüfung

- Vorfassung SHA256 299b3ee6ad2f0f785b45445f61e006fca9bb98734f5a76a20b025b8cfd9d8d56.
- Produktions-SHA256 691db63c5c1ce03ee84436dbda05a524076e17c76f7bfb82b3df27135204f723.
- ROM-Vergleich: nur 506A/506B/5077/5078/7002/7003/7006/7120/7121 als Nachrichtentext geändert; übrige 2106 deutsche Einträge sowie englische/französische Texte erhalten.
- Alle 635 funktionalen Kontrollsequenzen, PAL-Breiten, erforderlichen Namens-/Zeitvariablen und Puffer geprüft. Native Mindestseitenzahlen erhalten, zusätzliche Seiten nur manuell weitergeschaltet. TIME von 5077/5078, Brückenzoll-Auswahl und feste Cutscene-Zeiten erhalten.
- Alle 1509 komprimierten Segmente und CIC-6105-Prüfsumme geprüft. Weiterhin 32 MiB. Sonstige Codeänderungen auf Textzeiger bzw. einzeln geprüfte ROM-Adreß-Relokationen beschränkt; Figuren, Räume, Animationen und normaler Spielstart erhalten.
- Sechs gezielte Produktions-ROM-Szenarien bei 4 MiB: beide Zimmerleute nachts im Gasthaus, Nachtwache, beide Ladenbesucher und Schloßtorwache nach drei Steinen. Gewöhnliche Textboxen mit A/Z geöffnet. Nur lokaler Testfortschritt, Tageszeit und Links Position vorbereitet; keine NPC-, Text- oder Timer-Manipulation. Frühere nicht passende Aufstellungs-/Zielerfassungsversuche sind nicht als erfolgreiche Prüfungen gezählt.
- BPS mit RomPatcher.js auf die validierte Vanilla-ROM angewandt; Ausgabe bytegleich zur geprüften Produktions-ROM.

Sechs ausgewählte unbearbeitete Aufnahmen mit Herkunft in previews/alltagsgags/Aufnahmen.json. Logs/Berichte in validation/alltagsgags. Kein kompletter Spieldurchlauf, nicht jeder Tageszeit-Zweig live gespielt und kein Hardwaretest. ROMs/Spielstände bleiben lokal und werden nicht veröffentlicht.

## Nachbauen

Auf der bestehenden Rekonstruktion build_story.py ausführen, anschließend build_habeck.py zum Wiederherstellen der sicheren Habeck-Fortsetzungen und build_text_speed.py. Normale PAL-1.0-Ziele bauen und komprimieren. `python tools/verify_alltagsgags.py OOT VORFASSUNG.z64` prüft gegen die oben genannte Hyrule-NPC-Fassung.
