# Mehr Gespräche in Hyrule-Stadt

27 bislang originale Nachrichten von Stadtbewohnern und Seitengassen ersetzt; zusätzlich den bestehenden Farm-Folgedialog 7017 um den ausdrücklich gewünschten Gesichts-Gag erweitert. Insgesamt 28 geänderte Nachrichten gegenüber der Texttempo-Fassung und 626 bearbeitete deutsche Nachrichten im Gesamtprojekt. Nachrichten sind nicht mit verschiedenen NPCs gleichzusetzen: Erst-/Wiederholungs-, Gegenstands- und Storyzustände teilen sich Figuren.

## Belegung und Erreichbarkeit

| Figur | Nachrichten | Verhalten |
| --- | --- | --- |
| Frau 3 bei den Geschäften, En_Hy Typ 1 | 7017, 7045 | Gesichts-Gag im Farm-Folgedialog vor der Flucht; danach auch im ersten Nach-Flucht-Text. Vorheriger Farmhinweis erhalten. |
| Jogger, En_Hy Typ 3 | 7001 | Neues normales Gespräch vor und nach der Flucht. |
| Bettler, En_Hy Typ 5 | 700C, 70ED, 70EF, 70F0–70F3 | Neue Texte für Flaschenzustände. Der Mr.-Bean-Satz gehört zu 700C, das nativ bei vorhandenem Fisch/Käfer/Blauem Feuer ohne Übergabe gewählt wird. Ohne diese Inhalte erscheint 70ED. [C]-Hinweis und native Ankaufspreise 150/100/50/25 erhalten. |
| Feilschende Gruppen, En_Mu | 703E, 703F, 7041–7043 | Fünf neue Aussagen im bestehenden zufälligen Gesprächspool; keine neue Zufallslogik. |
| Hühner-Mädchen | 7000, 70EA | Normal- und Nach-Flucht-Reaktion ersetzt, Maskenreaktionen unverändert. |
| Paar auf dem Marktplatz, En_Tg | 7025, 7026 | Je vier/fünf native, manuell weitergeschaltete Seiten erhalten. |
| Seitengassen-Bewohner | 700E, 7055, 708A | Weitere Überraschungsdialoge, Hinweis auf die Feenquelle bleibt enthalten. |
| Hundefrau | 709B–709F, 70A0 | Stadt-/Nacht-/Rückgabezustände neu, weißer Richard, Suchauftrag und Belohnung bleiben verständlich. |

Die Frau ist die native grün-blaue En_Hy-Typ-1-Figur bei (480, 0, -202). Die feste Marktplatzkamera hält die Ansicht auf Abstand. Es gibt keine neue Unsichtbarkeitszone, kein verändertes Culling und keine versetzten NPCs. Ihr vorheriges Nutzer-Thema Farm/Klimawandel bleibt erhalten; bei 7017 steht der Metasatz vor dem bisherigen Wegweiser. Alle anderen 598 bereits bearbeiteten Nachrichten sind bytegleich zur vorherigen Veröffentlichung.

## Prüfung

- Vorfassung SHA256: 67c879ed33a4fc9c1f0817396afc407a01df47076120d9512ccd1564ecee0363.
- Produktions-SHA256: 299b3ee6ad2f0f785b45445f61e006fca9bb98734f5a76a20b025b8cfd9d8d56.
- Genau die 28 angekündigten deutschen ROM-Nachrichteneinträge geändert; die übrigen 2087 unverändert. Englisch und Französisch unverändert.
- Alle 626 Kontrollsequenzen, erforderlichen Namenszeichen, PAL-Zeilenbreiten, manuellen Seiten und Textpuffer geprüft. Alte Rechtschreibung. Feste Zeitvorgaben und Auswahlsteuerungen unverändert.
- Sämtliche 1509 gepackten Segmente geprüft, CIC-6105-Prüfsumme korrekt, weiterhin 32 MiB. Modelle/Räume unverändert. Das längere deutsche Textsegment verschiebt nachfolgende ROM-Segmente an der Ausrichtungsgrenze. Veränderte Adreßwörter im Code und in Overlays sind einzeln als Linker-Relokationen geprüft; sonst ist der ausführbare Code einschließlich des schnelleren Schreibtempos erhalten.
- Spielstandinitialisierung identisch zur normalen Texttempo-Fassung. Kein Sonderstart eingebaut.
- Sieben gezielte Produktions-ROM-Szenarien bei 4 MiB: Frau vor/nach Flucht, Jogger, Bettler ohne/mit Fisch, alle fünf Aussagen des nativen Gruppenpools, englische Frau als Gegenprobe. Reguläre Dialoge über A geöffnet/weitergeschaltet. Nur Testfortschritt, Inventar, Sprache und Spielerposition vorbereitet, keine Nachrichtenzustände oder NPCs manipuliert.
- RomPatcher.js validiert den BPS gegen die unveränderte Original-ROM; Ausgabe bytegleich zum geprüften Build.

Vier ausgewählte, unbearbeitete Ingame-Bilder in `previews/stadt-nachschlag/`; genaue Herkunft in Aufnahmen.json. Protokolle in `validation/stadt-nachschlag/`. Kein vollständiger Spieldurchlauf, nicht jeder neue Neben-Zweig live gespielt und kein Hardwaretest.

## Nachbauen

Auf der bisherigen Mod-Rekonstruktion `python tools/build_story.py OOT`, anschließend `python tools/build_habeck.py OOT` für die bestehenden sicheren Habeck-Fortsetzungen ausführen. `python tools/build_text_speed.py OOT` bewahrt/ergänzt das schnellere Texttempo. Danach normaler PAL-1.0-Build und Kompression. Prüfung mit `python tools/verify_stadt_nachschlag.py OOT TEXTTEMPO-VORFASSUNG.z64`.
