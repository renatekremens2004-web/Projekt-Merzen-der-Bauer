# Triangle Guy V24

Triangle Guy steht jetzt auf Zeldas Seite des Kampfplatzes, aber mit Link INNERHALB des Feuerrings. Zelda bleibt draußen. Position (440, 1086, -340), Entfernung zum Ringmittelpunkt 655,13 Spieleinheiten, unveränderte Feuer-Schadensgrenze 784. Auch seine gesamte ursprüngliche Modellbreite bleibt innerhalb dieser Grenze. Sein Standort und Links Ansprechposition haben echten Boden auf Höhe 1086. Triangle Guy ist regulär zu Fuß erreichbar, ohne durch das Feuer zu gehen.

Die groben Augen sind durch symmetrische weiße Augenwölbungen, grüne Iriden, schwarze Pupillen und kleine Lichtpunkte ersetzt. Körper, Mund, Arme, Hände und Füße behalten ihre bisherige Geometrie. Alle einfarbigen CI4-Materialflächen verwenden korrekt ausgerichtete 16 × 16 Texturzeilen. Eine nur für diesen Actor gesetzte Grundbeleuchtung hält ihn auch während der dunklen Kampfphasen sichtbar. Der native Lichtzustand der übrigen Szene wird nicht geändert.

Er winkt abwechselnd, bewegt beim Reden die Arme stärker und dreht sich in der Nähe zu Link. Es bleiben dieselben drei starren Modellteile und dieselben drei Zeichenmatrizen. 1178 statt bisher 1102 Dreiecke. Keine neue Objektbank, keine zusätzlichen Actor-Instanzen, keine geänderte Kollision oder Boss-KI. Die bisherige Gesprächssperre während Zwischensequenzen bleibt erhalten.

Sein vollständiger Text 608A ist unverändert: ursprüngliche verspätete Ankunft PLUS Triforce-des-Mutes-Zusatz. Sämtliche Nachrichten in allen Sprachen sind gegenüber V23 bytegleich. Die V23-Bombe, Donnerblumen und Musikänderung bleiben enthalten.

## Prüfung

Normal und DEBUG gebaut, N64-Prüfsummen geprüft. Alle ROM-Segmente gegenüber V23 verglichen: gezielt nur Elf_Msg2 und der finale Raum verändert; sonstige Unterschiede auf geprüfte Linker-Adressen beschränkt. Boss-, Zelda- und Feuerlogik unverändert. Alle nicht zu den Augen gehörenden Dreiecke einschließlich Positionen, Normalen und UVs gegen das bisherige Modell verglichen.

Im Emulator mit tatsächlichen 4 MiB RAM den nativen Ganon-Auftritt per Controller durchlaufen, zu Triangle Guy gelaufen, alle vier Dialogseiten geöffnet und das Gespräch geschlossen. Danach läuft das Spiel weiter. Im Test mindestens 19520 Bytes Reserve im nativen Objektbereich. Keine veränderten NPC-Positionen, Bossphasen oder Zeichenfunktionen im Test-RAM. Die neuen Positionen stammen aus der fertigen ROM. Kontrollierter Szenentest, kein vollständiger Spieldurchlauf.

Das knapp 20 Sekunden lange MP4 zeigt den Auftritt mit echtem, direkt aus N64-AI-DMA aufgezeichnetem Spielton. Nur der Anfang der Aufnahme mit Navis großer Gesprächskamera wurde abgeschnitten. Keine nachträgliche Tempo- oder Tonhöhenänderung.

## Anwendung und Quellen

Alle bisherigen Änderungen einschließlich V23 enthalten. Normal ODER DEBUG auf die unveränderte europäische PAL-1.0-ROM anwenden (MD5 e040de91a74b61e3201db0e2323f768a). Nicht auf die bereits gepatchte ROM anwenden. DEBUG-Menü wie bisher: L+R halten und Z drücken.

Letzter normaler Builder: `python3 tools/build_triangle_v24.py /workspace/oot-burns-pal`, nach `build_goron_bomb_v23.py`. Optional danach `build_debug_version.py`. Nach dem separaten DEBUG-Bau sind die Normalquellen und der normale Build wiederhergestellt. Modellgenerierung in validation/triangle-v24/prepare_model.py; Ausgangsmodell vom Nutzer, bisheriger Export tools/triangle_source.json. Neue Daten tools/triangle_v24_source.json, Bewegungen tools/triangle_v24_actor.inc.c. Kein Anspruch auf eine zusätzliche Lizenz der hochgeladenen Vorlage.
