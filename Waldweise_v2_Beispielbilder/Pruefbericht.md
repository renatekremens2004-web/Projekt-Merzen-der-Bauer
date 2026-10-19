# Waldweise v2: Schulter-Sitz und Einsturzgeschichte

Die Krabbelminen-Frau sitzt in den Credits tiefer hinter Darunias Kopf am Hals-/Schulteransatz. Die bisherige Beckenposition auf Höhe seiner Haarspitze war falsch. Der eigene Animationsursprung ist von (0,8300,0) auf (-100,5800,-800) Modell-Einheiten verschoben. Die Oberschenkel und Unterschenkel liegen nach außen; der Oberkörper lehnt 15 Grad zurück. Gleiche Körpergröße, gleiche Knochenlängen, keine neue Skalierung. Blick runter/hoch und ihre nativen Bildzahlen bleiben erhalten. Der Seitenblick von hinten in der gemeinsamen Einstellung zeigt den Kontakt zum Schulter-/Rückenansatz; die anderen Credits-Einstellungen bleiben erhalten.

Die Schultergeometrie wurde aus Darunias originalen Credits-Posen ausgewertet: Schulteroberkante ungefähr 56, hinterer Hals-/Rückenansatz 58,8 und Haarspitze 85 Spieleinheiten über der Modellbasis. Die nativen Figuren stehen auf leicht unterschiedlichen Bodenhöhen; auch dieser Versatz ist beim Sitz berücksichtigt. Der finale Sitz und die Bewegungen wurden im Emulator geprüft. Die Auswertung im Werkzeug ist eine Referenzpose, kein Kollisionsbeweis für beliebige Animationsframes.

## Dialog

Vier deutsche Nachrichten geändert (106A,108F,1090,106B), weiterhin insgesamt **706** eigene Nachrichten. Der Laden ist unter Merz’ Kaputtsparpolitik zusammengebrochen, Hyrule ist voller Zombies aufgrund seiner Reformen, und die Decke hat ihren Schädel gecrusht. Sie bittet um eine Warnung in der Vergangenheit, um sich einen anderen Job zu suchen: „Ist eher ungeil, tot zu sein. Honestly.“ Anschließend gibt sie als Waldweise das Amulett. Der Satz ist Dialog und startet keine neue Zeitreise-Nebenquest.

Alle festen Zeiten unverändert, insbesondere BOX_BREAK_DELAYED(30) in 108F und FADE(80) in 106B. Die wichtige Warnung steht auf einer manuellen Seite; die kurze automatische Seite sagt nur „Rein theoretisch.“. Junge Salia, ihre Geschichte und das Lied bleiben erhalten. Waluigi/Nabooru und Thaddäus/Wasserweiser weiterhin nur geplant.

## Build und Prüfung

Produktions-ROM SHA256: `59b69171d06cf38da8301e8290423405e583d7f13ab15008393cd8bb4cbd15f1`. Baseline: veröffentlichte Waldweise v1 `3ca9c4c0054ae075a5db8f5ae18db7f38072d63d11cd3adbaf779afce1a2efe9`.

Unterschiede: exakt die vier oben genannten deutschen Nachrichten, die drei eigenen Sitzanimationen im angehängten object_sa und die Kamera der gemeinsamen Credits-Einstellung in Demo_Sa. Alle übrigen eigenen Modellkanäle, Körpergeometrie, Knochenlängen, Texturen, Beleuchtung und Stand-/Segen-/Siegelanimationen gleich. Der originale 86576-Byte-Salia-Bereich bleibt bytegleich. Native Cutscene-Cues, Textzeiten, Fades, Amulettübergabe und Rückkehr erhalten. Weitere Binärunterschiede sind geprüfte Linker-Relokationen. Unveränderter Startcode und native Spielstandsinitialisierung.

32-MiB-ROM, CIC-6105-Prüfsumme und alle 1509 komprimierten Segmente geprüft. Alle 706 Text-Steuersequenzen und Textpuffer geprüft. Alle Raumlisten mit object_sa bleiben im Modellbank-Budget; Credits-Reserve jetzt 1456 Bytes. Die beiden späteren Weisen-Hallen behalten die bereits in v1 geprüfte Bankgröße; diese Revision erhöht sie nicht.

Gezielte aktuelle 4-MiB-Emulatorläufe: Credits mit Blickbewegungen und Szenenwechsel, vollständiger Waldamulett-Textablauf bis zur nativen Rückkehr in den Wald, spätere Siegel-Szene. Zusätzlich regulärer Start der fertigen Produktions-ROM ohne vorbereiteten Spielstand bis Titel-/Sprachauswahl. Keine Actor-Verschiebungen, Text-/Timer-Eingriffe oder gestarteten Save-States in diesen Szenarien. Lokal vorbereitete Fortschrittsdaten nur für die gezielt angesprungenen Cutscenes.

Die vom Nutzer wegen Schwarzbild in Rosalie’s Mupen GUI 0.6.0 hochgeladene ROM ist bytegleich zu v1, korrekt 32 MiB groß und hat die richtige N64-Prüfsumme. Genau diese Datei startete im Mupen64Plus-Core regulär mit Cached Interpreter (tatsächlich 4 MiB) und Dynarec (tatsächlich 8 MiB) bis zur Sprachauswahl. Der Nutzer bestätigte zwischenzeitlich ebenfalls den erfolgreichen Start. Die Ursache des vorübergehenden Schwarzbilds ist damit nicht festgestellt; die konkrete GUI-Konfiguration wurde nicht reproduziert und kein Startcode auf Verdacht geändert.

BPS mit RomPatcher.js samt Quellvalidierung auf die unveränderte Original-ROM angewandt: bytegleich zur Produktions-ROM. Bilder unbearbeitete echte Emulatoraufnahmen, Herkunft in previews/waldweise-v2/Aufnahmen.json. Kein vollständiger Spieldurchlauf und kein N64-Hardwaretest. Keine ROMs oder Spielstände veröffentlicht.

Nachbauen: build_story.py OOT, build_habeck.py OOT, build_bowling_sage.py OOT; PAL-1.0-Ziel bauen/komprimieren. Kanonische Animationsdaten in tools/bowling_sage_source.json. Normales Wiederbauen benötigt keinen Blender; generate_bowling_sage_seat.py kann die Sitzposen bei Bedarf mit Blender erzeugen. verify_bowling_sage_revision.py OOT VORFASSUNG.z64 benötigt baseline.map und original_bowling_sage_source.json neben der V1-ROM; Referenzdateien in validation/waldweise-v2.
