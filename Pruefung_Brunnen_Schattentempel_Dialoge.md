# Prüfung: Brunnen-/Schattentempel-Dialoge

Gesamtpatch für unveränderte Europa/PAL 1.0. Original-MD5 `e040de91a74b61e3201db0e2323f768a`. Ziel-SHA256 `8d52174b6d576c16f24a94e5621479d89b0acd247c91ce6a47d8f25640268030`, 40 MiB. Alle bisherigen Änderungen enthalten, einschließlich Wallaces neuer Arm-/Laufbewegung, kleinerem Waluigi und Schultersitz in den Credits.

19 deutsche Textkörper geändert, jetzt insgesamt 1.024 eigene Nachrichten. 0191 bleibt ausdrücklich unverändert. Alle sonstigen deutschen Nachrichten, sämtliche anderen Sprachen und alle Textboxkopf-/Positionseigenschaften exakt wie in der vorigen Veröffentlichung. Echte Spielernamen und funktionale Steuerzeichen einschließlich EVENT, TEXTID, Liedabläufen, Auswahlfeldern und festen Verzögerungen erhalten. Zusätzliche Seiten verwenden nur normales BOX_BREAK; keine festen Lesezeiten angepaßt.

Die verrutschten Nummern sind in der neuen Dialogliste zugeordnet; Oben-/Tiefe-Witze auf die beiden Mauern 0129/012A verteilt. Guru-Gurus erste Erwachsenenrede ist 5034. Alte Rechtschreibung, einschließlich daß, muß, Schloß, Haß, unfaßbar und wißt.

## Prüfung des Neubaus

- Layout aller eigenen Nachrichten mit den echten PAL-Schriftbreiten geprüft, höchstens vier Zeilen pro Seite. Spielernamen werden konservativ mit acht breiten Buchstaben berechnet.
- Alle 1.024 kompilierten eigenen Nachrichten unter 1.280 Rohbytes und unter 200 decodierten Zeichen pro Seite. Größte Nachricht unverändert 1.146 Bytes. Sheiks neue 5031: 944 Bytes, neun manuell weitergeklickte Seiten, höchstens 137 decodierte Zeichen pro Seite.
- Alle 1.509 komprimierten Segmente gegen den unkomprimierten Neubau geprüft; CIC-6105-Prüfsumme gültig.
- Nur deutsche Textdaten sowie notwendige Text-/Dateiadressen, ROM-Header und DMA-Daten ändern sich. Alle anderen Segmente sind bytegleich oder enthalten ausschließlich geprüfte Linker-Adreßanpassungen. Modelle, Animationen, native Akteurslogik, Cutscenes, Kameras, Quests und Navis Auslöser erhalten.
- RomPatcher.js mit Quellvalidierung erzeugt aus Vanilla und BPS bytegenau den oben genannten Neubau.

Dies ist ein Textschritt. Keine erneute Emulatoraufnahme oder vollständiger Durchlauf in diesem Schritt; vorige Modell-/Credits-Aufnahmen gehören weiterhin zu ihrem damaligen Build. Keine neue Performance- oder RAM-Zusage aus diesem Test abgeleitet. Keine ROMs, Spielstände, Savestates, RAM-Abzüge oder ausführbaren Dateien veröffentlicht.

## Quellen / Neubau

Neue Einträge: `story/schatten_brunnen_de.json`; bisherige Einträge mit denselben IDs aus `goronen_kakariko_de.json` und `bean_impa_de.json` dorthin verschoben, damit es keine doppelten IDs gibt. `build_shadow_dialogue.py <oot>` als letzten Textschritt nach der bestehenden Modell-/Kapitelfolge ausführen; anschließend normal bauen und komprimieren. Es ersetzt ausschließlich die 19 deutschen Textkörper im vorhandenen fertigen Tabellenstand. Alle anderen Kopf-/Sprach-/Fortsetzungsdaten bleiben erhalten, insbesondere Habecks TEXTID-Kette und private NPC-Textboxeinstellungen. Ein erneuter allgemeiner `build_story.py`-Lauf danach erfordert wie bisher die nachgelagerten Kapitel-Builder.

Der Vergleichsprüfer benötigt die vorige Produktions-ROM, deren Map, Texttabellenquelle und Navi-Hinweisquelle lokal; diese ROM-Vergleichsdaten sind nicht im Quellenpaket. Vollständiger Ergebnisbericht in `validation/shadow-dialogs/`.
