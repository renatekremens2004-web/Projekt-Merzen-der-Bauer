# Pinguine und Modellkorrekturen – V26

## Terri und Pingu korrigiert

Terris hochgeladene DS-Vorlage verwendet für beide Texturachsen MIRROR. Die bisherige Umsetzung benutzte normales WRAP. Seine UV-Koordinaten reichen bis über acht Texturkacheln hinaus; dadurch erschienen zuvor Teile der Hose und andere falsche Flächen auf Gesicht und Körper. Beide Achsen verwenden jetzt die vom Original verlangte gespiegelte Wiederholung. Die Modellgeometrie und die helmlose Auswahl bleiben erhalten. Das korrigierte Gesicht wurde im tatsächlichen Basar geprüft. Der reguläre Schildkauf funktioniert weiterhin: Eigentumsbit gesetzt, 99 auf 19 Rubine, Erhalt und Menüende.

Bei Pingu lagen Flügelansatz und großer Abwärtswinkel ungünstig zum schmalen Schulterbereich und breiteren Rumpf. Die Flügel wurden neu am oberen Rumpf verankert, leicht nach unten versetzt und nach außen gesetzt. Das Drehen erfolgt um diese Ansätze mit kleinerem Bewegungsbereich. Beide Flügel bleiben sichtbar außerhalb des Körpers und sind am Rumpf angesetzt. Keine zusätzlichen Dreiecke: weiterhin 607. Dialog und Standort sind unverändert. Neuer Szenentest mit beiden Dialogseiten und geschlossenem Gespräch.

## Madagascar-Pinguine in Friedrichs Schloß

Vier neue regulär ansprechbare NPCs, nur für erwachsenen Link und deutsche Spielsprache, jeweils in einem eigenen Raum:

- Skipper im Eingangskorridor, Raum 0, (-70, 240, 1520). Ein Dynamitbündel neben ihm.
- Kowalski in der Haupthalle, Raum 1, (-440, 150, 60). Ein Dynamitbündel neben ihm. Mr. Monopoly bleibt erhalten.
- Private im Vorraum der Lichtprüfung, Raum 9, (-2100, -240, -780). Eine einzelne Stange Dynamit ist seinem Flügel zugeordnet und bewegt sich mit ihm.
- Rico im ersten Raum der Waldprüfung, Raum 5, (1000, 110, 1000). Sechs einzelne rote Stangen liegen mit verschiedenen Ausrichtungen um ihn herum. Sie bleiben am Boden, wenn Rico sich zu Link dreht.

Leichte Körper-, Kopf- und Flügelbewegungen; etwas stärkere Gesten beim Reden. Ihre Größen unterscheiden sich passend zu den Figuren: Skipper 50, Kowalski 62, Private 46, Rico 54 Spieleinheiten. Originale DS-Geometrie und UVs bleiben erhalten. Die Texturen werden für den N64 als 64 × 64 CI4 mit je 16 Farben verwendet. Die eigentlichen Figuren haben 294, 295, 288 beziehungsweise 292 Dreiecke. Mit dem jeweiligen Dynamit zusammen: 416, 417, 392 und 916 Dreiecke. Für die Bündel wird die sparsame gelieferte Vorlage mit 122 Dreiecken verwendet, für die einzelnen Stangen die 104-Dreieck-Vorlage mit Zündschnur.

Das Dynamit ist ausschließlich sichtbare Kulisse, ohne Explosionslogik, Schaden oder Kollision. Wege, Türen, Originalgegner, Truhen, Prüfungen und Siegelabläufe werden nicht ersetzt. Pro Raum nur ein zusätzlicher NPC, keine einzelnen Actors für die Stangen. Keine neue Objektbank, keine neuen Objektbank-Slots oder DMA-Einträge. Benachbarte Räume können während eines Übergangs wie üblich gemeinsam geladen werden. Raumbezogene Zeichenadressen verwenden den jeweils zum Actor gehörenden Raum.

Skipper kündigt die Sprengaktion gegen Merz an, Private warnt vor der Aktion, Kowalski bringt eine absurde Cartoon-Rechnung, Rico ruft DYNAMIT/KABLAAAM/KA-BOOOM. Neue private Nachrichten 71E0 bis 71E3. Alle bisherigen Nachrichten sind bytegleich zu V25.

## Prüfung

Normal und DEBUG gebaut, N64-Prüfsummen geprüft. Beide BPS auf eine unveränderte PAL-1.0-Ausgangs-ROM angewendet; Ergebnisse bytegleich mit den Builds. Alle ROM-Segmente mit V25 verglichen; außerhalb der vorgesehenen Modell-, Actor-, Raum- und Nachrichtenergänzungen nur geprüfte Linker-Adressen. Der zentrale ausführbare Code hat ausschließlich solche Adreßanpassungen. Neue Texte passen in die Textpuffer.

Gezielte Laufzeittests mit tatsächlich 4 MiB RAM: alle vier Pinguine angesprochen, sämtliche Seiten gelesen, Gespräch geschlossen, Spiel läuft weiter. Mindestens 71488 Bytes Reserve im nativen Objektbereich in den geprüften Schloß-Räumen. Privates Zuordnung zu Raum 9 wurde im tatsächlichen geladenen Raum kontrolliert. Terri und Pingus letzte Korrekturen wurden mit der fertigen Normal-ROM erneut geprüft. Die vorherigen erfolgreichen Schloßtests wurden nach der ausschließlich Pingu betreffenden letzten Posenänderung nicht vollständig wiederholt. Keine Behauptung eines vollständigen Spieldurchlaufs.

## Anwendung und Quellen

Alle bisherigen Änderungen einschließlich V25, Triangle Guy und Goronia-Bombe enthalten. Normal ODER DEBUG auf eine unveränderte europäische PAL-1.0-ROM anwenden (MD5 e040de91a74b61e3201db0e2323f768a), nicht auf eine bereits gepatchte ROM. DEBUG-Menü: L+R halten und Z drücken.

Nach den drei V25-Buildern zuletzt build_penguins_v26.py und danach build_model_fixes_v26.py ausführen. Der Korrektur-Builder muß nach dem Pinguin-Builder laufen und korrigiert die aktuelle Pingu-Zeichenfunktion, ohne andere Gäste zu entfernen. Anschließend PAL-1.0 mit COMPARE=0 bauen. DEBUG optional danach separat. Die normalen Quellen und der normale Build sind abschließend wiederhergestellt.

OBJ-/DAE-Ausgangsdaten, Texturen, JSON-Modelle, Export- und Builder-Skripte enthalten. Prüfungen in validation/penguins-v26 und validation/model-fixes-v26. Keine ROMs, Spielstände oder ausführbaren Testprogramme enthalten. Die Vorlagen stammen aus den hochgeladenen Dateien; daraus folgt keine zusätzliche Lizenz an den Vorlagen.
