# Eulenstimme und leichter erreichbare Tagesgags

Weiterhin 681 bearbeitete deutsche Nachrichten. Gegen die veröffentlichte NPC-Stimmen-Fassung sind genau 45 Einträge neu geschrieben: 33 Euleneinträge, neun Zustände für Tagesbewohner/Nachtwache/Flaschenkäufer und drei Merz-Texte mit „Herr Bohne“.

## Eule

Der native En_Owl-Actor verweist einschließlich TEXTID-Fortsetzungen auf 34 Nachrichteneinträge: 10C0–10C7, 2064–2072, 3062–3063, 4002–4004, 4017, 4031 und 6079–607C. Alle hatten bereits eigene Texte; der Eindruck verbliebener Originale wurde durch eine allgemeine Ausdrucksweise begünstigt. 33 Texte sind deutlicher in der gewünschten Stimme gefaßt: Abwägungen, Selbstkorrekturen, Umsetzungsfragen, Energie/Wirtschaft und umständliche Einordnung. Die bereits eigene kurze Auswahlfrage 2066 bleibt. Keine Nennung Habecks, Raurus oder der Geistereulen-Erklärung in diesen Texten. Die Enthüllung in der Halle der Weisen bleibt unverändert.

Alle normalen Auftritte, Varianten nach Lied-/Questfortschritt, Wiederholungen, Ja-/Nein-Reihenfolgen, Wegangaben und Flugangebote berücksichtigt. Automatische BOX_BREAK_DELAYED(40), TEXTID, EVENT und sonstige Steuersequenzen erhalten. Keine Lese-/Cutscene-Zeiten oder Actor-Logik geändert.

## Merz nennt Bean „Herr Bohne“

In Merz’ Flucht-/Suchdialogen 2019/201E und seiner Masterschwert-Rede 700A heißt Bean konsequent „Herr Bohne“. Die übrigen Figuren behalten „Mr. Bean“. Nur diese drei Texte wurden nach der Eulen-/Tagesprüfung zusätzlich geändert; alle anderen Nachrichtentexte und sämtliche Actor-Overlays sind zwischen beiden Builds bytegleich (bohne-scope-verification.json).

## Tagesgespräche

| Rolle am nativen Standort | Vor Zeldas Flucht | Danach | Zugang |
| --- | --- | --- | --- |
| Ältere Frau auf dem Marktplatz, EnHy Typ 6 | 7021 zuerst, 7022 bei Wiederholung | 704A | Zitteraal-Gag tagsüber; ohne Flasche/Handel. |
| Mann im schwarzen Oberteil nahe den Geschäften, EnHy Typ 4 | 7023 zuerst, 7024 bei Wiederholung | 704B | Bean als Rettungssanitäter tagsüber; ohne Flasche/Handel. |
| Hyrules Marktplatz-Nachtwachen | 7003 | 7003 | Stolz auf den Dienst ausdrücklich bei Nacht; kein Zitteraal mehr. |
| Flaschenkäufer, EnHy Typ 5 | 700C / 70ED | native Bedingungen | Kerngag wegverlegt; klare Aufforderung zum Zeigen mit C. Preise/Belohnungen unverändert. |

Der Flaschenkäufer wählt 700C tatsächlich erst, wenn ein passender Inhalt mitgeführt wird; ohne passenden Fisch/Käfer/blaues Feuer verwendet er normalerweise 70ED. Der neue Tages-Erzähler hat diesen Zweig nicht. Zwei spätere Haar-Kommentare (704A/B) weichen den Gags. Die übrigen entsprechenden Sprüche bleiben. Die Tagesfiguren brauchen nach den bestehenden nativen Regeln keinerlei Item, Minispiel oder Nebenquest. Maskenreaktionen behalten ihre eigenen Pfade.

## Prüfung

- Vorfassung SHA256 9d486686e7cd4a38e782eaa6b484c14f486d994b3741be05b444bfe9369664f0.
- Produktions-SHA256 81bfa6f9aa1c339c48012327c4dd02c19371acf44b0fe48bc6967eabd9e24858. 32 MiB, gültige CIC-6105-Prüfsumme.
- Genau 45 deutsche Texte geändert, alle anderen 2070 deutschen Einträge bytegleich. 681 bearbeitete Einträge insgesamt. Englische/französische Texte, bisherige Kapitel und Modelle erhalten.
- Alle 681 funktionalen Steuersequenzen, PAL-Breiten und Puffer geprüft. Eigene Texte an allen 34 erfaßten Eulenplätzen und keine vorgezogene Identitätsenthüllung nachgewiesen.
- 1509 komprimierte Segmente gegen unkomprimierte Ausgabe geprüft. Zusätzliche Änderungen ausschließlich in German-Textdaten/-Zeigern, Prüfsumme, Segmenttabelle und einzeln geprüften Linker-Relokationen. Native En_Owl-, En_Hy- und Nachtwachen-Quellen unverändert; bisheriger normaler Start und schnelleres Schreibtempo erhalten.
- Neun native Emulator-Szenarien bei 4 MiB: beide Tagesfiguren vor und nach Zeldas Flucht, Nachtwache sowie Eule vor dem Kokiri-Wald, am Schloß und am Zora-Fluß sowie die native Masterschwert-/Merz-Szene mit „Herr Bohne“. Die acht Eulen-/Tagesfälle verwenden die vor dem Namensnachtrag gebaute, ansonsten text- und actoridentische Zwischenfassung; Merz wird mit der endgültigen ROM geprüft. Protokolle/Bilder nennen ihren jeweiligen Hash. Erst- und Wiederholungsgespräche tagsüber mit leeren Flaschenplätzen; bei den ersten beiden Eulenketten Wiederholung und anschließendes Verlassen über normale Controller-Eingaben geprüft.
- BPS mit RomPatcher.js auf die validierte Vanilla-ROM angewandt; Ausgabe bytegleich zur Produktions-ROM.

Sieben unbearbeitete Ingame-Beispiele mit Herkunft in previews/eule-tagesdialoge/Aufnahmen.json. Berichte/Logs in validation/eule-tagesdialoge. Lokale Testspielstände bereiten nur Fortschritt, Tageszeit und Links Position vor. Keine NPCs versetzt, keine Text-/Timer-Manipulation. Nicht jeder Eulenauftritt live gespielt, kein voller Spieldurchlauf und kein Hardwaretest. ROMs/Spielstände werden nicht veröffentlicht.

## Nachbauen

Nach der bestehenden Modellrekonstruktion `build_story.py OOT`, `build_habeck.py OOT`, `build_npc_stimmen.py OOT` und `build_text_speed.py OOT`, dann normale PAL-1.0-Ziele bauen und komprimieren. `python tools/verify_eule_tagesgags.py OOT VORFASSUNG.z64`; die oben genannte Vorfassungs-Linker-Map muß als baseline.map danebenliegen (mitgeliefert unter validation/eule-tagesdialoge/baseline.map.txt). Runtime-Skripte benötigen den genannten lokalen Emulator und private Testspielstände.
