# Pingu, Crazy Frog und Terri – V25

Terri (Beedle) ohne Helm ersetzt den Basarhändler: als Kind in Hyrule-Stadt, als Erwachsener in Kakariko. Nur dessen Zeichenfunktion verwendet das neue Modell. Shop-Inventar, Preise, Dialoge, Auswahlcursor, Kaufablauf und der übrige Händlercode bleiben erhalten. Der Helm ist ein eigener Material-/Modellteil und vollständig entfernt (138 Dreiecke). Der verbleibende Körper mit Gesicht hat 321 Dreiecke und eine einzige 64 × 64 Textur; vier starre Modellteile ermöglichen leichte Kopf-, Arm- und Körperbewegungen. Höhe 88 Spieleinheiten. Kein neuer Actor und keine zusätzliche Objektbank für Terri. Die übliche deutsche Spielsprache ist Voraussetzung für die Ersetzung.

Pingu steht als Erwachsener in Raum 2 der Eishöhle, seitlich im Gang vor dem großen Klingenraum. 607 Dreiecke, Höhe 46, vier bewegliche starre Teile. Leichte Kopfbewegungen und Flügelschläge, im Gespräch etwas stärker. Sein Text 71DE enthält genau den gewünschten NOOT-NOOT-Satz und das Zitat auf zwei Seiten. Native Wege, Krüge, Übergänge und Rätsel bleiben bestehen.

Crazy Frog steht als Kind am Ufer direkt beim ursprünglichen Froschstamm im Zora-Fluß. Er hat 382 Dreiecke, Höhe 42 und leichte Arm-/Kopfbewegungen. Sein Gespräch 71DF besteht ausschließlich aus geschriebenen Crazy-Frog-Geräuschen. Die sechs ursprünglichen Frosch-Actors, das Okarina-Minispiel und seine Belohnungen bleiben erhalten. Keine zusätzlichen Sprachaufnahmen. Als Erwachsener erscheint Crazy Frog nicht.

Alle Modelle werden nur aus ihrem jeweiligen Raum geladen. Keine neuen DMA-Einträge oder zusätzlichen Objektbank-Slots. Die Modelle stammen aus den vom Nutzer hochgeladenen Vorlagen; daraus folgt keine zusätzliche Lizenz für die Vorlagen.

## Prüfung

Normal- und DEBUG-Build erstellt, N64-Prüfsummen geprüft, beide BPS auf die unveränderte PAL-1.0-Ausgangs-ROM angewendet und das Ergebnis bytegenau mit den Builds verglichen. Alle bisherigen Nachrichten in Deutsch, Englisch und Französisch sind bytegleich zu V24; nur zwei private neue Nachrichten sind hinzugefügt. Neue Texte passen in die vorhandenen Textpuffer. Alle ROM-Segmente gegen V24 verglichen; außerhalb der vorgesehenen Änderungen nur nachgewiesene Linker-Adressen. Der Maschinencode im zentralen Code-Textabschnitt hat nur solche Adressanpassungen. Der Basar-Quelltext ist außerhalb des reinen Modell-Renderers unverändert.

Vier gezielte Laufzeittests mit tatsächlichen 4 MiB RAM: Pingu und Crazy Frog angesprochen, beide Textseiten gelesen, Gespräch geschlossen und anschließend weiterlaufen lassen. Terri als Kind und Erwachsener kontrolliert: regulär ansprechen, Schild auswählen, kaufen, Erhalt abwarten und Einkauf beenden. Eigentumsbit wechselt, 99 Rubine werden zu 19, der Laden läuft weiter. Dabei verbleiben mindestens 103712 Bytes im nativen Objektbereich. Pingu-/Crazy-Frog-Tests erfolgten vor der ausschließlich visuellen Terri-Blickrichtungskorrektur; beide Basartests wurden mit der fertigen korrigierten ROM wiederholt. Gezielt geprüfte Szenen, kein vollständiger Spieldurchlauf.

## Anwendung

Alle bisherigen Änderungen einschließlich Triangle Guy V24 und Goronia-Bombe V23 enthalten. Normal ODER DEBUG auf eine unveränderte europäische PAL-1.0-ROM anwenden (MD5 e040de91a74b61e3201db0e2323f768a), nicht auf eine bereits gepatchte ROM. DEBUG-Menü wie bisher L+R halten und Z drücken. Spielstände vor einem Versionswechsel regulär im Spiel sichern und neu laden.

## Reproduzieren

Nach build_triangle_v24.py nacheinander:

1. python3 tools/build_pingu_v25.py /workspace/oot-burns-pal
2. python3 tools/build_crazy_frog_v25.py /workspace/oot-burns-pal
3. python3 tools/build_beedle_v25.py /workspace/oot-burns-pal

Dann PAL-1.0 mit COMPARE=0 bauen. DEBUG optional anschließend separat bauen. Nach dem DEBUG-Bau sind die normalen Quellen und der normale Build wiederhergestellt. Ausgangs-OBJ/DAE und PNGs liegen in models/pingu, models/crazy_frog und models/beedle. Exportskripte, fertige JSON-Modelldaten, eingebundene Actor-Helfer und Originaldateien befinden sich in tools. Prüfskripte und Berichte in validation/pingu-v25. Keine ROMs, Spielstände oder ausführbaren Testprogramme enthalten.
