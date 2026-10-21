# Finale Burns V5

## Aufteilung nach Zeitlinie und Gestalt

In der gesamten normalen Kinder-Zeitlinie bleibt der vollständige Burns mit seinem Anzug erhalten: Intro, Schloßhof und Flucht-/Reitszenen benutzen weiterhin das unveränderte Objekt OBJECT_GNDD. Die Phantom-Ganon-/Amthor-Köpfe bleiben ebenfalls unverändert.

Für die erwachsenen Ganondorf-Auftritte im Schloß und Finale verwendet OBJECT_GANON wieder Ganondorfs originalen Körper, Hände, Skelett und Bewegungen, ergänzt um den bereits bewährten Burns-Kopf. Nur Kopf und Hals, keine Burns-Schultern oder Jackenreste. Der native Umhang wird nur am zugehörigen erwachsenen Boß-/Endauftritt wieder gezeichnet. Die Kindheitsvarianten behalten ihr bisheriges Aussehen.

Ganon besitzt nach der Verwandlung seinen originalen Bestienkörper mit einem gleichmäßig auf das 2,2fache vergrößerten Burns-Kopf. Alte Schweineschnauze, Zähne, Augen, Haarketten und Hörner sind vollständig ausgeblendet. Die leeren Displaylisten bleiben an ihren ursprünglichen Knochenslots, damit Matrixindizes, Angriffspunkte, Schwertbewegungen, Schwanz und Kollisionen erhalten bleiben. Der Kopf bewegt sich als ein starrer Teil am vorhandenen Kopfknochen; keine neue Gesichts-/Lippensynchronanimation.

## Speicher und Beleuchtung

Pro Kopf 1779 Dreiecke wie die bewährte Vorlage, ohne zusätzliche Polygone. Die eigentlichen Körper kommen aus dem Originalspiel. Beide Köpfe verwenden ihre eigenen unverzerrten Proportionen und folgen den nativen Animationen. Die Farbpalette und Normalen dienen weiterhin der echten Spielbeleuchtung; kein unbeleuchtetes Ersatzbild. Nach der Koordinatendrehung werden Normalenwerte auf den gültigen positiven/negativen Bereich begrenzt, damit keine Komponente beim 8-Bit-Packvorgang das Vorzeichen wechselt.

Die statischen Eckpunktdaten sind global dedupliziert: je Kopf 1080 eindeutige Vtx-Einträge. Dreiecksreihenfolge für den 32er-Vertexcache optimiert; bei Bedarf getrennte Vertex-Ladevorgänge mit unveränderten Cacheplätzen. Eine Rekonstruktion der Displaylisten prüft sämtliche Eckpunkte, UVs und Normalen gegen die Vorlage. Keine neuen Objektslots, keine vergrößerten Speicherpools. In der abschließenden 4-MiB-Endkampfprobe blieben 19520 Bytes im bestehenden Objektpuffer frei. Alle vier betroffenen Objektlisten statisch einschließlich Keep-/Spielerobjekten geprüft: Orgelraum 44832, Ganon-Endkampf 19520, Schloß-Endraum 93184 und die betreffende Schlußszene mindestens 251984 Bytes Reserve.

## Prüfung

Beide normalen/Debug-PAL-Builds mit gültiger N64-Prüfsumme. Objekt- und Quellvergleich zur V4-Fassung: Nur OBJECT_GANON, OBJECT_GANON2 und die native Umhang-Zeichenfunktion sind inhaltlich geändert. Alle übrigen Binäränderungen einzeln als Linker-Relokationen geprüft. Insbesondere bleiben OBJECT_GNDD (vollständiger Burns als Kind), OBJECT_GND (Phantom-Köpfe), Textdatei und kompilierte deutsche Texte bytegleich. Boß-KI, Angriffs-/Kollisionslogik, Kameras, Animationsdaten, Musik und Zeitabläufe bleiben erhalten.

Laufzeitproben der endgültigen normalen ROM mit echten 4 MiB, aktiver Grafik-Clipping-Option und höchstens zwei gleichzeitigen Emulatoren: vollständiger nativer Orgel-Intro-Ablauf bis Zustand 16 einschließlich Aufstehen/Wenden, sowie die Verwandlung und 180 weitere freie Spielbilder im eigentlichen Ganon-Kampf. Nur Spieler-/Fortschritts-Testdateien für den Einstieg vorbereitet; keine Modelle für Aufnahmen versetzt, keine Boßaktionen oder Animationszustände injiziert. Die nativen Controller-Eingaben bestätigen Dialogseiten. Keine Grafikkommando-/Vertexfehler, Objektpufferüberläufe oder Abstürze in diesen Proben. Gesicht, Körperanschluß und vollständiges Entfernen der Schweine-/Haar-/Hornreste anhand der echten Aufnahmen kontrolliert. Das sind gezielte Proben, kein vollständiger Spieldurchlauf bis zum letzten Treffer und kein Hardwaretest.

Zwei MP4-Dateien zeigen jeweils 600 fortlaufende Spielbilder, 36 Sekunden bei PAL 50/3 Bildern pro Sekunde, ohne Ton: Merz_Ganondorf_Koerper.mp4 und Ganon_Burns_Verwandlung.mp4. Die zweite zeigt die native Verwandlung; die zusätzliche Probe im freien Kampf ist im Testprotokoll dokumentiert.

Beide BPS mit RomPatcher.js und aktiver Quellvalidierung auf Vanilla angewandt und byteweise mit den gebauten Ziel-ROMs verglichen. Alle bisherigen Änderungen bis V4 enthalten, auch Triangle Guy, Running Man und Dialogtrennungen. Die bereitgestellten Kapitel-1/2-Texte gelten unverändert weiter.

## Anwendung und Quellen

Je einen BPS-Gesamtpatch auf die unveränderte Europe/PAL-1.0-ROM anwenden, nicht auf eine bereits gepatchte Datei. Original-MD5 e040de91a74b61e3201db0e2323f768a. Deutsch wählen. Normal und DEBUG enthalten dieselben Spielinhalte; Debugsteuerung unverändert.

Letzter normaler Builder: tools/build_finale_burns.py nach build_character_life.py, vor optional build_debug_version.py. Grundlage des Kopfes: die bereits enthaltene CC-BY-4.0-Burns-Adaption (chicosantossaraiva), tools/phantom_burns_source.json und models/phantom-amthor. tools/ganon_finale_rig.json enthält die aus der nativen Ruheanimation ermittelte Kopf-Basis. Quellenarchiv einschließlich Builder und Prüfungen, ohne ROM, ELF, Save, SRAM, Savestate oder ausführbare Programme.

normal Ziel-SHA256: 752dbf11612d29982b3f51d5ba13e6e17c8073536116318f36b4421877bbc37c

debug Ziel-SHA256: bb96f05cd1b5a4f2f5da8dc258dd23dfeb4deeb28e968b4c46fbec4c0f25e53f
