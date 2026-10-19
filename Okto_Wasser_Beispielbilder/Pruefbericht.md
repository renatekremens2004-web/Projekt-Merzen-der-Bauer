# Okto am Wasser – Platzkorrektur

Der vorherige Platz auf den Bildern war die tatsächliche Ingame-Position auf trockenem Boden. Diese Fassung ersetzt ihn durch (140, -330, 0) am Rand der nativen Wasserfläche im Eingangsraum von Jabu-Jabu. Link kann vom trockenen Ufer aus mit A sprechen, ohne schwimmen zu müssen. Okto bleibt wiederholt ansprechbar, auch nach geräumtem Raum.

Die Initialisierung ermittelt den nativen Wasserpegel und prüft, daß der Boden darunter liegt. Keine frei erfundene Höhe: Wasseroberfläche -330, Boden an Oktos Position ungefähr -333,7. Okto verwendet die vorhandene Float-Animation, Modellbeleuchtung und die native Wasserring-Routine. Keine Angriffe, Trefferkollision oder Projektile; NPC-Kategorie 4, AT=0/AC=0. Normale Oktoroks bleiben Gegner. Die bereits vorhandene, ausschließlich auf diesen NPC begrenzte Raum-Clear-Ausnahme ist unverändert.

## Prüfung

- Produktions-ROM SHA256: 508a8bf66f5775e4f88151723089abe713ce7d1b490a6964fed01640411bb168. Vergleichsbasis: vorher veröffentlichte trockene Okto-Fassung SHA256 e09953490120959b4bd1ae215e64238c8d78fd47b71a47d898fb3a0be3d60fcd.
- Alle deutschen Nachrichteneinträge sind bytegleich zur Vorfassung, einschließlich sämtlicher 682 eigenen Nachrichten. Keine Text-, Lesezeit-, Quest-, Modell- oder Startänderungen.
- 32 MiB, CIC-Prüfsumme und sämtliche 1509 komprimierten Segmente geprüft. Der Kerncode einschließlich Actor_Spawn ist bytegleich zur Vorfassung; Quellnormalisierung bestätigt unveränderte native Gegnerzweige. Nur Oktos Platz, Wasserhöheninitialisierung und Wasserringe geändert.
- Zwei gezielte native Emulatorprüfungen mit 4 MiB: normaler Eingangsraum und bereits geräumter Raum. Beide zeigen vollständiges und wiederholtes Gespräch. Link bleibt während der ersten Gespräche am trockenen Ufer (kein WATER-Bit); Okto bleibt auf der nativen Wasseroberfläche mit AT=0/AC=0. Vorbereitete lokale Fortschritts-Spielstände und normale A-Eingaben; keine NPC-Versetzung oder Text-/Timer-Manipulation zur Laufzeit.
- BPS mit RomPatcher.js auf die unveränderte PAL-1.0-ROM angewandt: Ergebnis bytegleich zur Produktions-ROM.

Drei echte, unbearbeitete Emulatoraufnahmen samt Herkunft in previews/okto-wasser. Prüfberichte und Rohlogs in validation/okto-wasser. Kein vollständiger Spieldurchlauf oder Hardwaretest. Frühere breite Verhaltensprüfungen sind in TESTING_OKTO.md dokumentiert; diese Aktualisierung prüft die Platzkorrektur gezielt.

## Nachbauen

Bestehende PAL-1.0-Rekonstruktion verwenden, nach den bisherigen Generatoren tools/build_friendly_octorok.py OOT ausführen und normal bauen/komprimieren. tools/verify_okto_water.py OOT VORFASSUNG.z64 benötigt die oben genannte Okto-Vorfassung und deren baseline.map (mitgeliefert als validation/okto-wasser/baseline.map.txt). Runtime-Skripte benötigen den lokalen Emulator und private Testspielstände. ROMs und Spielstände werden nicht veröffentlicht.
