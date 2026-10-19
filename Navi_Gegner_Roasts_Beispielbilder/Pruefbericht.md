# Schärfere Navi-Gegnertexte

Alle 93 Textplätze 0600–065C wurden neu geschrieben. Konkrete Gegneraktionen und direktes Beschimpfen statt allgemeiner Vergleiche über die Persönlichkeit. Die normale Skulltula zeigt als achtbeiniger Vollidiot ihren Schwachpunkt; bei der Killermuschel droht Navi, sie in der Mitte durchzubrechen. Nicht jeder Text enthält einen Fluch. Alte Rechtschreibung bleibt erhalten, etwa unfaßbar, daß, muß, bißchen und verpiß.

599 bearbeitete deutsche Nachrichten insgesamt. Alle 93 bestehenden Seitenzahlen bleiben erhalten, einschließlich der zwei Seiten von 061A; keine festen Textzeiten verlängert. Alle funktionalen Kontrollen und alle 599 Textpuffer geprüft.

## Statische Grenzen des Eingriffs

Vergleich mit der veröffentlichten normalen LEGO-X-Wing-Fassung, SHA256 c78155650c054c3111d1e97119f63c8070f951cbcb04390324d681283de1c09b. Die deutschen ROM-Nachrichtentabellen wurden direkt aus beiden fertigen ROMs gelesen: genau 93 geänderte Nachrichten, IDs 0600–065C. Alle anderen deutschen Nachrichten bytegleich, ohne C-String-/Segment-Padding. Englisch und Französisch sowie die bisherigen Modelle und Räume bleiben unverändert.

Der gesamte Code-Abschnitt ist bytegleich bis auf die erforderlichen Zeiger in sGerMessageEntryTable. Somit keine Änderungen an Kampfverhalten, Z-Anvisieren, Navi-Auslösung, Beleuchtung oder Spielstandinitialisierung. Normale Fassung mit normalem Spielstart; der separate Nach-Jabu-Sonderpatch bleibt ein eigener Download. Alle 1509 komprimierten Segmente sowie CIC-6105-Prüfsumme und RomPatcher.js-Rundlauf geprüft.

## Laufzeit

Drei gezielte Szenarien auf derselben Produktions-ROM, tatsächlich 4 MB, Mupen64Plus/GLideN64, EnableClipping=True, EnableCustomSettings=False:

- Normale Skulltula im Dekubaum, Raum 8: natives Z-Ziel und C-oben öffnen 0604; wiederholt beobachtet.
- Native Killermuscheln im Wassertempel, Raum 18: natives Z-Ziel und C-oben öffnen 0627; wiederholt beobachtet.
- Englische Skulltula-Gegenprobe: ursprünglicher englischer Text statt des deutschen Roasts.

Teststarts setzen nur Links Raum, Position, Sprache und Inventar; Gegner bleiben an ihren normalen Orten und bewegen sich regulär. Für die Aufnahme hat der Testspielstand zwölf Herzen; im Wassertempel trägt Link die normale Zora-Rüstung und Eisenstiefel. Keine Heil-/Versetzungs-/Freeze-Logik in der Produktions-ROM. Unbearbeitete Spielbilder liegen unter previews/navi-roasts/, Protokolle und Helfer unter validation/navi-roasts/.

Die beiden gewünschten Gegner wurden im Spiel geprüft; kein kompletter Spieldurchlauf oder Live-Test aller 93 Zieltextplätze. Platzhalterplätze behalten allgemein formulierte Beleidigungen ohne erfundenen Gegnernamen. Kein Hardwaretest.

Original-ROM: Europa/PAL 1.0, MD5 e040de91a74b61e3201db0e2323f768a. Gesamtpatch direkt auf die unveränderte Original-ROM anwenden. Normale Spielstände statt alter Emulator-Save-States verwenden. Produktions-SHA256: e8a1ce46bf4ed445935d471427dafab2ed708ce1c3409af75a8f90c2df52b6d3.
