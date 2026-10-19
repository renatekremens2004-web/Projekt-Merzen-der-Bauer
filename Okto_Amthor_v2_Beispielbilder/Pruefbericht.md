# Okto im Wassertempel und Phantom-Köpfe v2

Alle bisherigen Änderungen enthalten. Zwei deutsche Nachrichten geändert (00F8 und 209C), insgesamt 963 eigene Nachrichten. 00F9 ist unverändert. Der aktuelle Dialog steht in planning/OKTO_WASSERTEMPEL_DIALOGE_AKTUELL.md.

## Okto

Im festen Eingangsbecken von Wassertempel-Raum 0, nur als erwachsener Link in deutscher Sprache. Position −195/765/810 nach nativer Wasserabfrage; Boden darunter 620. Link kann ihn vom trockenen Rand −195/780/725 ansprechen. Wasserbox 0 bleibt bei allen drei Hauptpegeln auf 765; das veränderliche Hauptbecken wurde mit −15, 445 und 765 geprüft. Die originale Wassersteuerung wurde nicht geändert. Ein zusätzlicher Actor und OBJECT_OKUTA, Listen von 28 auf 29 und 12 auf 13 erweitert; vorhandene Grafik, Kollision und Wege erhalten.

Okto bleibt ein freundlicher NPC mit nativer Schwimmanimation, Beleuchtung und Wassereffekten. Kein Angriff, keine Trefferannahme, kein Projektil. Wiederholt ansprechbar und auch in bereits gesäubertem Raum vorhanden. Der Ehren-Oktorok ist ein Dialoggag ohne Inventargegenstand. Jabu-Okto bleibt an seinem bisherigen Platz; seine vier Seiten enthalten jetzt Hola, Amigo, Muchacho, Ay caramba und Compadre. Normale Gegner bleiben unverändert.

## Köpfe und Video

Burns verwendet wieder das etablierte klassische Merz-Modell, ausschließlich Kopf und Hals ohne eigene Jacke, Schultern oder Kragen. Die ursprüngliche neutrale Gesichtsgeometrie bleibt erhalten. 1779 Dreiecke. Smithers behält die vollständige Gesichts-/Brillengeometrie mit grauen Haaren, 783 Dreiecke. Beide Köpfe gleichmäßig skaliert. Originale Phantom-Rüstung, Pferd, Skelett, Animationen, Kampf, Kamera und Begrüßung bleiben erhalten. Drei eigene CI4-Texturen; originaler Todesmaskeneffekt berücksichtigt sie weiterhin. Im Bossraum verbleiben 83.008 Bytes des nativen Objektpuffers.

Die MP4 zeigt den tatsächlichen nativen Übergang aus der finalen ROM: 670 aufeinanderfolgende gerenderte Frames, 40,2 Sekunden, 640×480, PAL 50/3 Bilder/s. Ohne Ton; keine Montage oder ersetzten Modellbilder. Die PNGs sind unveränderte Emulatoraufnahmen. Urheber- und Lizenzangaben in models/phantom-amthor/ATTRIBUTION.md und CREDITS.md.

## Prüfung

Finale ROM-SHA256: `54945b5aaec82f7f7094a0653c11a730455d2b04bcf3462960e3f5b48acebaf2`. 32 MiB, CIC-6105. Alle 1509 komprimierten Segmente mit dem Neubau verglichen. 3667 erhaltene Codefunktionen, 195 native Phantom-Assets, 34 Kampffunktionen und 115 Assets des Eingangsraums geprüft. Alle anderen Modelle und Szenengeometrien erhalten; notwendige Linker-Adressen über Relokationen geprüft. Englisch/Französisch unverändert; alle 963 Textpuffer innerhalb ihrer Grenzen.

Sechs gezielte abgeschlossene Emulatorproben auf dieser finalen ROM: niedriger/mittlerer/hoher Wasserstand, gesäuberter Wassertempel-Raum, Jabu-Gespräch und englische Negativprobe. Mupen64Plus/GLideN64 mit tatsächlichen 4 MiB. Keine direkt gestarteten Textboxen und keine versetzten NPCs. Die gesonderte native Reveal-Aufnahme prüft die neuen Köpfe in Bewegung. Kein kompletter Spieldurchlauf oder N64-Hardwaretest.

RomPatcher.js wendet den BPS mit Quellprüfung auf Original-MD5 e040de91a74b61e3201db0e2323f768a an und erzeugt bytegleich den geprüften Neubau. Direkt auf die entpackte unveränderte Europa/PAL-1.0-ROM anwenden. Normale Spielstände verwenden, keine alten Emulator-Save-States. Original-ROM, Speicherabbilder, ausführbare Programme und Spielstände sind nicht im Quellenpaket enthalten.
