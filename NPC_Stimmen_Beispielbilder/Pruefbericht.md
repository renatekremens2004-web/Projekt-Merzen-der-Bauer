# Eigene NPC- und Händlerstimmen

46 zusätzliche deutsche Nachrichtenzustände, insgesamt 681 bearbeitete Nachrichten. Der Kokiri-Nachtrag ersetzt einen bisherigen eigenen Text; die anderen 634 bleiben bytegleich. Alte Rechtschreibung, bestehendes schnelleres Schreibtempo und normaler Spielstart erhalten.

| Figur | Einträge | Umsetzung |
| --- | --- | --- |
| Basar, beide Orte | 0127 | Eigene deutsche Begrüßung, Qualität/fake. |
| Tränkehändler, Hyrule und Kakariko | 012C | Eigene Begrüßung zur Inflation. |
| Krabbelminenhändler | 012D | Eigene Warnung. |
| Schießbudenbetreiber, beide Orte | 012E | Wortspiel, anschließend originale 20-Rubine-Auswahl. |
| Schatzkistenspiel | 006D, 704C | Auge der Wahrheit; Schlüssel/10 Rubine erhalten. |
| Hexe im hinteren Elixierladen | 500C–500E, 5048–504D, 504F | Schleimhexe, Tauschaufgabe und 100-Rubine-Kauf. |
| Alter Mann in Erwachsenen-Kakariko | 5087 | Deku-Ball-Empörung; Brunnen/Auge-Hinweis bleibt. |
| Mann mit rotem Schnurrbart | 507F–5082 | Bartwachs in seinen Dorf-/Gasthauszuständen. |
| Wache am Todesberg-Tor | 200A/C/E/F, 2010/15/16, 2020 | Zuständigkeit und Befehle; Brief, Schild, Maskenhandel erhalten. |
| Irrlichtsammler | 70F4–70F8 | Frühere Krugraum-Wache; Rückblick nach sieben Jahren, Handel und dynamischer Punktestand. |
| Kind bei Salias Garten | 100A | Wald-Idyll nur vor dem Kokiri-Smaragd; spätere Story-Zweige erhalten. |
| Familie im Skulltula-Haus | 001F–0029, 00FE | Spinnenfluch, Zwischenbelohnungen und Vater bei 100; echte Symbolzähler. |

Die Händler teilten zuvor Begrüßungen mit anderen Läden. Zwei eng begrenzte Actor-Anpassungen wählen ausschließlich auf Deutsch private Textplätze. Andere Sprachen, Maskenladen, Tauchspiel, Preise, Auswahlreihenfolgen und Spielregeln behalten ihre Pfade. Rücknahme genau dieser Einfügungen ergibt die nativen Händler-/Schießbuden-Quellen. Die übrigen NPCs nutzen ihre ursprünglichen Text-IDs und Standorte.

## Prüfung

- Vorfassung SHA256 691db63c5c1ce03ee84436dbda05a524076e17c76f7bfb82b3df27135204f723.
- Produktions-SHA256 9d486686e7cd4a38e782eaa6b484c14f486d994b3741be05b444bfe9369664f0. 32 MiB, gültige CIC-6105-Prüfsumme.
- Genau 47 geänderte deutsche Nachrichteneinträge (46 zusätzliche Bearbeitungen, ein bisheriger Kokiri-Text neu); übrige 2068 Einträge bytegleich. Englisch/französische Daten unverändert. Sämtliche 681 funktionalen Steuersequenzen, Breiten und Puffer geprüft; Namens-, Skulltula- und Irrlichtzähler erhalten.
- Zusätzliche Seiten bei Kokiri, Wache, Hexe und Schießbude werden manuell weitergeschaltet; keine festen Lese-, Minispiel- oder Cutscene-Zeiten verändert. Sichere Habeck-Fortsetzungen unverändert.
- 1509 komprimierte Segmente gegen unkomprimierte Ausgabe geprüft. Modelle, Räume, Animationen und normales Startverhalten erhalten. Veränderungen außerhalb der deutschen Texte und zwei beabsichtigten Actor-Segmente einzeln als Linker-Relokationen geprüft; geänderte Zeiger in den Overlay-Tabellen haben unveränderte Addenden.
- 16 gezielte native 4-MiB-Szenarien einschließlich englischer Basar-Begrüßung und Kokiri vor/nach dem Smaragd. Elf erfolgreiche Händler-/NPC-Szenarien stammen aus der zuerst gebauten Fassung; fünf Gespräche wurden mit der endgültigen ROM geprüft. Der zusätzliche Kokiri-Nachtrag ändert allein Nachricht 100A, alle Actor-Segmente und übrigen Nachrichtentexte sind zwischen beiden Builds bytegleich (kokiri-scope-verification.json). Protokolle und Bilder nennen ihren jeweiligen ROM-Hash. Neue Gespräche über A/Z geöffnet, echte NPCs nicht versetzt. Lokaler Testfortschritt, Tageszeit und Links Position vorbereitet. Keine Textbox-/Timer-Manipulation.
- Native Funktionsprüfungen: Schatzkistenspiel zieht 10 Rubine ab und gibt den Schlüssel; Schießbude zieht 20 Rubine ab und startet; Schleimhexe füllt nach 100 Rubinen die Flasche mit blauem Trank; erste Skulltula-Belohnung erweitert die Geldbörse.
- BPS mit RomPatcher.js auf die validierte Vanilla-ROM angewandt; Ausgabe bytegleich zur geprüften Produktions-ROM.

Neun ausgewählte unbearbeitete Ingame-Aufnahmen mit Herkunft in previews/npc-stimmen/Aufnahmen.json. Logs/Berichte in validation/npc-stimmen. Kein kompletter Spieldurchlauf, nicht jeder Alters-/Tageszeit-/Belohnungszustand live gespielt und kein Hardwaretest. Keine ROMs/Spielstände veröffentlicht.

## Nachbauen

Auf der bestehenden PAL-1.0-Rekonstruktion nach den bisherigen Modellgeneratoren `build_story.py OOT`, dann `build_habeck.py OOT`, `build_npc_stimmen.py OOT` und `build_text_speed.py OOT` ausführen. Normales PAL-1.0-Ziel bauen und komprimieren. `python tools/verify_npc_stimmen.py OOT VORFASSUNG.z64` prüft gegen die oben genannte Vorfassung. Dazu deren Linker-Map als `baseline.map` neben der lokalen Vorfassungs-ROM bereitstellen (Kopie: validation/npc-stimmen/baseline.map.txt). Native Runtime-Tests erfordern den in den Skripten genannten lokalen Emulator und private Testspielstände; diese werden nicht mitgeliefert.
