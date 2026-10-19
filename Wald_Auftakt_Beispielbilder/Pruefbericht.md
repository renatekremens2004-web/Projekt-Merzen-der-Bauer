# Wald-Auftakt: Kokiri, Shiek und Rennsport-Boris

15 deutsche Nachrichten neu bearbeitet, davon zwei bereits eigene Boris-Texte ersetzt und 13 bisher native Einträge ergänzt. Insgesamt jetzt 695 eigene Nachrichten. Alle bisherigen Änderungen, Modelle, schnelleres Schreibtempo und Okto am Wasser enthalten.

## Belegung

| Figur / Situation | IDs | Inhalt |
|---|---|---|
| Entspannter Kokiri als Erwachsener, vor Waldamulett, in Midos Haus | 105F | Schock über den seit sieben Jahren toten Deku-Baum; derselbe Typ CHILD_4 wie Kindheitsdialog 100A. |
| Derselbe Kokiri nach Waldamulett, wieder draußen | 1076 | Wald erholt sich, aber die versprochenen hundert Baumjahre fehlen weiterhin. |
| Boris als Geist, vor Rennstart | 5041 | Große Vergänglichkeitsrede, Treppensturz vorgestern, angeblich schon immer Rennsportler, „Uga Paluga“ als angeblich alte Catchphrase, Testament und ausdrücklicher Waldtempel-Hinweis. Zehn manuelle Seiten. |
| Boris nach erstem Rennen | 502D | Testament eingelöst; Enterhaken/Fanghaken, Waldtempel und gefährliche Windmühlentreppe. Fünf manuelle Seiten. |
| Boris nach Wiederholungsrennen | 502E | Geschenk und angebliches Rennsport-Markenzeichen. |
| Shieks erstes Gespräch in der Zitadelle | 7056/7057/7077–707A | Merz hat Hyrule verwüstet, fünf Tempel, alte Freundin ohne Namensnennung, Kakariko/Haken. |
| Shieks Hinweise bei erneutem Ansprechen | 700F/7010 | Fehlender/vorhandener Haken; zweideutige alte Freundin. |
| Shiek beim Menuett des Waldes | 106C/106D | Arbeit, Dinge ins Rollen bringen, Glück/Geschick, alte Bekanntschaft. |

Nicht rückwirkend beim Kind-Boris oder Friedhofsjungen Rennsport oder Catchphrase hinzufügen: Gerade die unbelegte Behauptung ist der Gag.

## Spätere Modelle / Enthüllung

Krabbelminen-Bowling-Frau soll Salia als Waldweise ersetzen. Noch kein Modell geliefert, deshalb aktuell ausschließlich zweideutige Shiek-Hinweise aktiv. Enthüllungsentwurf, zu prüfende Folgeauftritte und Abgrenzung zu junger Salia in planning/WALDKAPITEL.md. Salia-Modell und Enthüllung im aktuellen Patch noch nativ.

Phantom-Ganon wird später Philipp Amthor mit dem noch zu liefernden Smithers-Modell. Nutzerkorrektur zu Smithers festgehalten. Noch kein Modell- oder Bossdialogtausch.

## Prüfung

- ROM SHA256 3b1e1808f52f6484b3a76cd8aaa90feccc0bbbf825cd779f5a9e8031efe766ce. Vergleich gegen die veröffentlichte Okto-Wasser-Fassung SHA256 508a8bf66f5775e4f88151723089abe713ce7d1b490a6964fed01640411bb168.
- 32 MiB, korrekte CIC-Prüfsumme, 1509 komprimierte Segmente gegen unkomprimierte Ausgabe geprüft. Alle Modelle, Szenen und Actor-Overlays bytegleich; abweichend nur deutsche Texte, deutsche Nachrichtentabelle und notwendige ROM-Metadaten.
- Exakt die 15 beabsichtigten deutschen Nachrichten geändert. Alle übrigen deutschen Texte und andere Sprachdaten erhalten. Kerncode außerhalb der deutschen Zeigertabelle geprüft; unveränderte Quest-, Renn- und Belohnungslogik. Rennen-Zeitnachricht 502F samt RACE_TIME unangetastet.
- Alle 695 Nachrichten auf Funktionssteuerungen und Textpuffer geprüft. Boris 5041: 930 Rohbytes von 1280; größtes dekodiertes Seitenbudget 105 von 200. Alle Seiten innerhalb der nativen Textbreiten. Keine festen Lese-/Ausblend-/Cutscene-Zeiten geändert.
- Fünf gezielte native 4-MiB-Emulatorfälle: Kokiri vor/nach Waldamulett, vollständige zehnseitige Boris-Einleitung, Shieks erste Zitadellen-Szene und wiederholbarer Kakariko-Hinweis. Testspielstände lokal vorbereitet, nur Link zur Gesprächsprobe positioniert; keine NPC-/Text-/Timer-Manipulation. Kein vollständiger Renn-/Waldtempel-Durchlauf oder Hardwaretest. Belohnungsseiten statisch mit nativen Steuerungen geprüft.
- Gesamtpatch mit RomPatcher.js auf die unveränderte Original-ROM angewandt, Ergebnis bytegleich zur Produktions-ROM.

Vier echte, unbearbeitete Emulatorbilder in previews/wald-auftakt, Herkunft in Aufnahmen.json. Rohlogs und Berichte in validation/wald-auftakt. Keine ROMs oder Spielstände im Quellenpaket.

## Nachbauen

Auf bestehender Mod-Rekonstruktion build_story.py OOT, build_habeck.py OOT (TEXTID-Fortsetzungen), build_npc_stimmen.py OOT und build_text_speed.py OOT ausführen. Normale PAL-1.0-Ziele bauen und komprimieren. tools/verify_forest_opening.py OOT VORFASSUNG.z64 benötigt die obige Okto-Wasser-ROM und ihre baseline.map neben der Datei (Map im Quellenpaket als validation/wald-auftakt/baseline.map.txt). Native Tests erfordern den lokalen Emulator und private Spielstände.
