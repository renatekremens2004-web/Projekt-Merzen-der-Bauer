# Wald-Dialoge, Navi bis Feuertempel und Salias Reise

748 eigene Story-Nachrichten plus 15 reine Namensänderungen, insgesamt 763 bearbeitete deutsche Nachrichten. Dieser Gesamtpatch enthält sämtliche bisherigen Modell- und Dialogänderungen. 28 Nachrichten unterscheiden sich von der veröffentlichten Wasser-/Geisterweisen-Fassung.

Sheiks Menuett-Szene enthält das Gedicht über Mr. Bean und Merz. Salia kündigt vor dem Waldamulett ihre Untersuchung im Waldtempel von Philipp Amthor an (016A). Beim Anruf nach dem Waldamulett sagt sie (016B): „Jaa, keine Sorge, (Spielername), mir geht's prächtig. Ich bin auf ne coole Reise gegangen, weil Hyrule mir zu konservativ wurde.“ Die drei vorhandenen manuellen Seiten und EVENT bleiben erhalten. Der native Fortschritt bestimmt die spätere Ablösung dieses Anruftextes.

Sieben Kokiri-Typen haben die gewünschten Sprüche erhalten; mehrere native Erst-/Wiederholungs-/Nach-Tempel-Texte gehören jeweils zur gleichen Figur. Midos eigene Texte bleiben erhalten. Der Laborforscher spricht nur als Erwachsener und auf Deutsch über den Papphai (0199); Kind-, englischer, Tauchbelohnungs- und Tauschquestzweig bleiben erhalten. Sein interner Gesprächszustand ist weiterhin 4018.

Navi: 01A3, 01A5, 01A7, 01A9 und 0152 enthalten die Nutzerfassungen. 0105 mit den Minecraft-Blöcken wird sowohl im Wald- als auch im Feuertempel benutzt. 0151 und 0120 bleiben erhalten. Die vollständige Übersicht mit Auslösern steht unter planning/NAVI_NACH_WALDTEMPEL_BIS_FEUER_AKTUELL.md.

## Prüfung

Finale ROM-SHA256: `0fbfcd1d49f9196be409e7d91c8384b35cc7b35d168865392892bc0a0b8a40f8`. 1509 komprimierte Segmente geprüft, davon 1228 bytegleich zur Vergleichsfassung. Alle anderen Unterschiede sind auf die dokumentierten deutschen Texte, die beiden Erwachsenen-/Sprachbedingungen des Laborforschers und überprüfte Linker-Relokationen begrenzt. Modelle und Szenendaten bleiben erhalten. Alle 763 Textpuffer, native Steuerbefehle, Textketten und feste Zeiten geprüft. RomPatcher.js prüft die Original-ROM und erzeugt bytegleich den finalen Build.

Der finale Emulatorlauf ruft Salia über das tatsächlich gespielte Lied nach dem Waldamulett an; alle drei Seiten von 016B und Wiederansprache sind protokolliert. Frühere gezielte Läufe prüfen Sheiks komplettes Menuett-Ereignis einschließlich Liedlernen, Salias Anruf vor Abschluß, ausgewählte Kokiri, Laborintro für Erwachsener/Kind/Englisch sowie alle sechs Seiten von Navis Statuerede und alle vier Seiten nach dem Feueramulett. Diese früheren Aufnahmen stammen aus dem unmittelbar vorherigen Build c31317a3bb9a6123c9b84546f812487813ad441ce584b6c2c19de5064e33e290; seitdem wurde ausschließlich der Inhalt von 016B geändert. Die Herkunft ist pro Bild dokumentiert.

Mupen64Plus mit GLideN64 und tatsächlichen 4 MiB. Vorbereiteter Fortschritt, Ausrüstung und Spielerposition; keine NPCs für Bilder verschoben und keine Textboxen per Debugfunktion geöffnet. Der lokale Statuenhinweis wurde durch einen kurzen Fall des vorbereiteten Spielers in sein natives Auslösevolumen erreicht. Unveränderte Emulator-PNGs. Kein kompletter Spieldurchlauf und kein Hardwaretest. Frühere verworfene Teststände mit falschen Song-/Fortschrittsbits sind keine bestandenen Nachweise.

## Neubau

Vollständigen README-Ablauf verwenden. build_wald_dialoge.py nach den vorhandenen Modellbauern anwenden, build_sage_names.py abschließend. Bei erneutem build_story.py anschließend build_habeck.py für die sicheren TEXTID-Ketten und build_sage_names.py erneut anwenden. verify_wald_nachschlag.py erwartet die lokale Wasser-/Geisterweisen-Vergleichs-ROM samt baseline.map. Keine vollständigen ROMs, Saves oder ELF-Dateien im Paket.
