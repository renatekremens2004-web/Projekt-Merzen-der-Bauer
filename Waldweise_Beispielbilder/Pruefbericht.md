# Krabbelminen-Frau als Waldweise

Die Frau wird erst nach dem Waldtempel als Waldweise enthüllt. Die junge Salia, ihr Lied, Kontakt, Geschichte und Brückenauftritt bleiben erhalten. Nach dem Waldamulett reagiert Salia am Okarinentelephon auf die neue Weise. Siegel-/Prüfungsrollen und Credits zeigen dieselbe Frau. In den Credits sitzt sie mit eigenen Beinen auf Darunias Schultern und blickt mit den nativen Cue-Wechseln nach unten und wieder hoch.

514 Quelldatenpunkte und 986 Dreiecke vollständig erhalten. Eigenes Skelett mit 15 Gelenken, 7 Animationen, ausschließlich gleichmäßige Skalierung, 62 Spieleinheiten hoch. Die Figur behält in Halle und Credits dieselbe Körpergröße. Normale Szenenbeleuchtung, Normalen, Nebel und transparente Ausblendung. Kameras der Enthüllung und einer Credits-Einstellung berücksichtigen die größere Figur. Alle Cutscene-Cues, Textzeiten, Übergänge, Belohnungen und Fade-Zeiten bleiben erhalten. Quellen und Urheberhinweise: models/bowling_sage/CREDITS.md.

Acht deutsche Nachrichten neu (106A/108F/1090/106B/003E/016B/016C/016D), insgesamt **706** eigene Nachrichten. Alle vorherigen Änderungen einschließlich Mido, Boris, Thaddäus im Tauchspiel und Okto bleiben enthalten. Thaddäus ersetzt die erwachsene Ruto noch nicht. Naboorus Ersatz ist vorgemerkt, Figur und Modell noch offen.

## Prüfung und Grenzen

Produktions-ROM SHA256: 3ca9c4c0054ae075a5db8f5ae18db7f38072d63d11cd3adbaf779afce1a2efe9. Gegenüber der veröffentlichten Mido-Fassung 8e88134c0d58e947d6a22d7c67dc3f6f5c5b0d779181124abc2c911f8445095d: ausschließlich die acht genannten deutschen Nachrichten, object_sa, Demo_Sa und der gezielte Modellbank-Bedarf in Object_InitContext geändert; weitere Binärunterschiede sind geprüfte Linker-Relokationen. Der ursprüngliche 86576-Byte-Teil von object_sa ist bytegleich erhalten. Andere Sprachdaten und sämtliche Raumsegmente bleiben erhalten. Native En_Sa- und Brückenroutinen unverändert.

Modellbank: doppelte Vertexdaten ohne Geometrieverlust zusammengefaßt. Die beiden späteren Halle-der-Weisen-Einstellungen laden zusätzlich Habeck und alle anderen Figuren; nur für diese Cutscene-Layer ist die Modellbank von 1050 auf 1226 KiB vergrößert (jeweils abzüglich nativer 4-KiB-Reserve). Kein Expansion Pak erforderlich. Alle Szenenlisten mit object_sa konservativ gegen die ROM-Objektgrößen geprüft. Aktuelle Credits-Modellbank hat lediglich 1472 Bytes Reserve. Künftige Ersatzmodelle erfordern eine neue Budgetprüfung und gegebenenfalls Optimierung; die jetzige Prüfung ist keine Garantie für spätere Modelle.

Sieben tatsächliche Emulatorproben mit 4 MiB abgeschlossen:
- Waldamulett-Enthüllung, normale A-Seiten, Segen, Amulett und native Rückkehr in den Wald.
- Echte Credits auf dem Todesberg: Sitzen auf Darunias Schultern, Blick runter/hoch, native Creditseinblendungen und Szenenwechsel.
- Junge Salia in ihrem Haus: unverändertes Skelett und normales Gespräch 1003.
- Englische Waldamulett-Szene: ursprüngliches Salia-Skelett und englische Texte.
- Erste Rauru-/Habeck-Szene ohne vorgezogene Waldweise.
- Spätere Triforce-/Weisen-Szene mit allen geladenen Figuren.
- Siegel-Szene mit eigener Segensanimation der Waldweisen und nativen Übergängen.

Lokal vorbereitete Spielstände zum gezielten Aufrufen der nativen Szenen. Keine NPC-Verschiebungen und keine Text-/Timer-Schreibzugriffe in diesen Szenarien. Bilder sind unbearbeitete Emulatoraufnahmen der veröffentlichten Produktions-ROM, keine Illustrationen. Herkunft: previews/waldweise/Aufnahmen.json. Der Test läuft mit GLideN64 und aktiviertem Software-Clipping. Erwartete Cloud-Meldungen zu Kamera, fehlendem Font und VSync sind keine Spielabstürze.

32 MiB, CIC-Prüfsumme, 1509 komprimierte Segmente, alle 706 Text-Steuersequenzen und Textpuffer geprüft. Die ursprünglichen festen Textzeiten sind erhalten. BPS mit RomPatcher.js und Quellvalidierung auf Vanilla angewandt: Ergebnis bytegleich zur Produktions-ROM. Kein vollständiger Spieldurchlauf, kein echter Hardwaretest und keine umfassende Leistungsmessung.

## Nachbauen

Bestehende Mod-Rekonstruktion vorausgesetzt. build_story.py OOT, danach build_habeck.py OOT für die bereits vorhandenen sicheren Textketten, dann build_bowling_sage.py OOT ausführen. Normales PAL-1.0-Ziel bauen/komprimieren. Der Generator benötigt Python und Pillow, keinen Blender zur normalen Wiederholung. Eigene Skelett-/Animationsdaten stehen in tools/bowling_sage_source.json, originale DAE und Texturen unter models/bowling_sage. Die mitgelieferten Importhelfer dokumentieren den einmaligen Quellimport, ihre Arbeitsdateipfade sind keine universelle Setup-Anleitung.

verify_bowling_sage.py OOT VORFASSUNG.z64 benötigt die oben genannte Mido-ROM und baseline.map daneben (validation/waldweise/baseline.map.txt). Nur BPS, Modell-/Werkzeugquellen, Dokumentation und Bilder veröffentlicht; keine ROMs, Spielstände oder Emulator-Binaries.
