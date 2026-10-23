# V49: Merz und König gegenüber auf dem blauen Teppich

Merz und König Harkinian sind jetzt auf derselben Mittellinie des blauen Teppichs ausgerichtet und schauen einander an. Sie stehen auf gegenüberliegenden Seiten der Teppichmitte. Der König steht mit den Füßen auf dem Boden. Merz geht weiterhin auf ihn zu und kniet wie bisher nieder.

Die in V48 verkleinerte Größe beider Figuren bleibt erhalten. Kamera, Kamerafahrt, Dialoge, Gesten, Zeitablauf und zurückgelegte Gehstrecke bleiben unverändert. Es werden keine zusätzlichen Figuren oder Modelle geladen.

Diese Version enthält alle Änderungen bis V48, einschließlich Lichtgewand, Frosch-Übergabe und Navis Erklärung in der Zitadelle.

## Anwendung

Einen der beiden kumulativen BPS-Patches auf eine saubere europäische Ocarina-of-Time-PAL-1.0-ROM anwenden, nicht auf einen vorherigen Patchstand. Quell-ROM-MD5: `e040de91a74b61e3201db0e2323f768a`. Das Quellen-ZIP enthält keine ROM.

DEBUG-Steuerung unverändert: L+R halten und Z drücken; C-links: alle Items; C-rechts: Standard → Lichtgewand → Schattengewand; A: Ort laden.

## Prüfung

- Fensterszene mit der ursprünglichen weiten und nahen Kamera im nativen Emulator mit 4 MiB getestet.
- Positionen, Blickrichtungen und unveränderte verkleinerte Größen im laufenden Spiel geprüft.
- Normal- und DEBUG-Build mit V48 verglichen: Geändert sind ausschließlich die Positionen/Blickrichtung der beiden Figuren sowie Merz' entsprechende Wegpunkte. Alle anderen Szenendaten einschließlich Kameras, die gesamte Programmlogik, Modelle und Texte bleiben bytegleich.
- Beide BPS-Patches mit einem unabhängigen Patchprogramm angewendet und bytegleich mit den jeweiligen Builds verglichen.

Kein vollständiger neuer Spieldurchlauf. Die Änderungen betreffen nur die Fensterszene.

## Wiederaufbau

Nach dem V48-Builder `python3 tools/build_window_carpet_v49.py /pfad/zum/oot-burns-pal` ausführen. Für DEBUG wie bisher `build_debug_version.py` zuletzt ausführen und anschließend mit `--restore` wieder die normale Ausgabe herstellen. Die V48-Ausgangsdateien für diesen Schritt liegen unter `tools/originals/window-carpet-v49`.
