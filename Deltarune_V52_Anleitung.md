# V52: Deltarune-Gäste und zwei geparkte Panzer

Diese Ausgabe enthält alle bisherigen Änderungen bis V49 sowie die folgenden Ergänzungen. Die normale und die DEBUG-Ausgabe sind jeweils kumulative BPS-Patches für eine unveränderte europäische PAL-1.0-ROM (MD5 `e040de91a74b61e3201db0e2323f768a`). Genau einen Patch auf die saubere Basis anwenden, nicht auf eine bereits gepatchte ROM.

## Deltarune-Trio

Kris, Susie und Ralsei stehen zusammen im Donnerblumen-/Treppenraum von Dodongos Höhle (Raum 2), seitlich neben dem Treppenbereich. Sie erscheinen ausschließlich als Kind. Der Zugang, Donnerblumen und das Treppenrätsel bleiben erhalten. Verwendet werden die kleine gerüstete Susie aus dem Referenzbild und die kleinere Ralsei-Variante. Kris' Arme sind aus der T-Pose abgesenkt; die drei bewegen Kopf und Arme leicht, beim Reden etwas stärker. Sie behalten ihre eigenen Körperproportionen.

- Kris: „...“
- Susie: „VERFICKTE SCHEISSE, KRIS! WARUM ZUM FICK SIND WIR IN ZELDA: OCARINA OF TIME?!“
- Ralsei: „Willkommen, Fremder! Ich mag dein Gewand. Hast du zufällig einen Dunklen Brunnen gesehen?“

Die Gespräche sind unabhängig und benutzen neue Textnummern; vorhandene Dialoge werden nicht überschrieben.

## Original Starwalker

Die zweite hochgeladene Version ersetzt die erste Auswahl vollständig. Sie hat nach der Reduktion 565 Dreiecke und behält ihre sieben Knochen. Je ein ansprechbarer Starwalker steht im Deku-Baum, in Dodongos Höhle, Jabu-Jabu, Wald-, Feuer-, Wasser-, Schatten- und Geistertempel, Friedrichs Schloss, Brunnen und Eishöhle. Die Sprüche entsprechen der gewünschten englischen Fassung. Vor „Starwalker“ gibt es eine Pause über die normale Textsteuerung des Spiels.

Die Figuren sind in den jeweiligen Raum eingebettet und benötigen keine zusätzlichen Objektbank-Plätze. Der schwarze Konturrand des gelieferten Modells verwendet die passende Rückseiten-Ausblendung, damit er den gelben Körper nicht verdeckt.

## Kakariko

Als Erwachsener stehen nur noch zwei Panzer seitlich am Rasenrand, parallel zueinander und mit freiem Durchgang. Der vordere steht entsprechend der Bodenneigung. Die bestehenden festen Kollisionshüllen bleiben erhalten. Die Kinderversion sowie die eigenen Schauspielerlisten für Bongo-Bongo/Sheik und die Credits erhalten diese geparkten Panzer nicht.

## Prüfungen

Die neuen Gespräche und die Abwesenheit des Trios als Erwachsener werden im Emulator mit 4 MiB geprüft. Die vorherige V50-Prüfung umfasst außerdem Tag/Nacht, einen normalen Lauf durch Kakariko, feste Panzerkollision und die vollständige Bongo-Bongo-/Sheik-Sequenz mit dem Erlernen des Liedes. Die Prüfprotokolle und Skripte liegen im Quellenarchiv.

Die 405 bestehenden Modellbanken, unveränderte Räume, vorhandene Texte und die ursprünglichen Cutscene-Daten einschließlich der neun Credits-Skripte werden mit V50 verglichen. Beide BPS-Dateien werden mit einem unabhängigen Patcher gegen die gebauten ROMs geprüft. Ein vollständiger Spieldurchlauf wurde nicht durchgeführt.

## DEBUG bedienen

L+R halten, dann Z drücken. Alter, Tageszeit und Ort auswählen, mit A laden. C-links gibt alle Items. C-rechts wechselt Standard/Lichtgewand/Schattengewand. Die vorhandene Credits-Option bleibt enthalten. Bei alten Emulator-Savestates empfiehlt sich für neue Figuren ein frischer Raumwechsel; ein Savestate enthält noch den früheren RAM-Zustand.

## Quellen wieder bauen

Die vorhandene Baufolge bis V49 bleibt erhalten. Danach:

```
python3 tools/build_kakariko_parking_v50.py /pfad/zu/oot
python3 tools/build_starwalker_v51.py /pfad/zu/oot
python3 tools/build_deltarune_trio_v52.py /pfad/zu/oot
```

Die fertigen Modell-Includes und konvertierten Quelldaten sind enthalten. Für die normale Ausgabe anschließend wie bisher mit `VERSION=pal-1.0 COMPARE=0` bauen. Für DEBUG zuletzt `build_debug_version.py` anwenden; `--restore` stellt die normale Ausgabe wieder her. Die Blender-Konverter unter `validation/` dokumentieren die Auswahl, Größen, Armpositionen und Texturvorbereitung.

Kris-Modell: LumpySpirit, mit Dank an Spikey-Valentine und Senjen für die zugrunde liegenden Rips, gemäß der mitgelieferten README. Die übrigen Modelle stammen aus den vom Nutzer bereitgestellten Archiven; es wurden keine zusätzlichen Urheberangaben erfunden. Original Starwalker sowie Kris, Susie und Ralsei sind Figuren aus Deltarune.
