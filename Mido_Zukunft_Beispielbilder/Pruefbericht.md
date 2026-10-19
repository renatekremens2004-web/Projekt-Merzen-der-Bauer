# Mido: sieben Jahre später

Drei deutsche Zukunftsnachrichten ergänzt, insgesamt jetzt 698 eigene Nachrichten. Die gesamte vorherige Wald-Auftakt-Fassung einschließlich Uga-Paluga-Boris, Shieks Hinweisen und Okto am Wasser bleibt enthalten.

- 1060: Mido findet den Spieler selbst nach sieben Jahren noch scheiße. Spielername dynamisch. Native Fortsetzung zu 1061 unverändert.
- 1061: Wiederholbarer Spruch plus Verabredung mit König Zora für eine mögliche Siegesfeier, falls Friedrich Merz besiegt wird. „Du rettest Hyrule, ich gehe feiern. Jeder leistet seinen Beitrag.“
- 1068: Nach Salias Lied dieselbe Haltung und derselbe Plan. Mido läßt den Weg weiterhin durch die native Liedprüfung frei.

## Prüfung

Produktions-ROM SHA256 8e88134c0d58e947d6a22d7c67dc3f6f5c5b0d779181124abc2c911f8445095d. Vergleich gegen veröffentlichte Wald-Auftakt-Fassung 3b1e1808f52f6484b3a76cd8aaa90feccc0bbbf825cd779f5a9e8031efe766ce. Exakt 1060/1061/1068 geändert; alle anderen deutschen Nachrichten bytegleich. Andere Sprachdaten, Szenen, Modelle und sämtliche Actor-Overlays einschließlich En_Md bytegleich. Kerncode nur deutsche Textzeiger verändert. Normale Startdaten, Quest-/Liedprüfung, Wegfreigabe, Preise und Belohnungen unverändert.

32 MiB, CIC-Prüfsumme und 1509 komprimierte Segmente geprüft. Alle 698 eigenen Nachrichten innerhalb von Textbreiten und nativen Puffern; Funktionssteuerungen und Fortsetzung 1060→1061 erhalten. Keine festen Lesezeiten geändert. Native 4-MiB-Probe: erster Spruch, Fortsetzung und Siegesfeiertext im echten Gespräch mit Mido. Lokal vorbereiteter erwachsener Spielstand in seinem tatsächlichen Raum, normale A-Eingaben; keine NPC-/Text-/Timer-Manipulation. Text 1068 statisch geprüft, kein erneuter vollständiger Lied-/Dungeon-Durchlauf oder Hardwaretest.

BPS mit RomPatcher.js auf die unveränderte Original-ROM angewandt, bytegleich zur Produktions-ROM. Zwei echte unbearbeitete Aufnahmen mit Herkunft in previews/mido-zukunft. Rohlogs/Prüfberichte in validation/mido-zukunft. Keine ROMs, Spielstände oder Emulator-Binaries veröffentlicht.

Nachbauen: auf bestehender Mod-Rekonstruktion build_story.py OOT und danach build_habeck.py OOT für sichere Fortsetzungsketten ausführen. Normales PAL-1.0-Ziel bauen/komprimieren. tools/verify_mido_future.py OOT VORFASSUNG.z64 benötigt die oben genannte Wald-Auftakt-ROM und ihre baseline.map daneben (Map als validation/mido-zukunft/baseline.map.txt mitgeliefert).
