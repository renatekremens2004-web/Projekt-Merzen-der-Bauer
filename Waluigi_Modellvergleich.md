# Waluigi für Nabooru: Vorprüfung, noch kein Einbau

Nutzerentscheidung: Nabooru wird später Waluigi. Jetzt ausschließlich Modelle vergleichen und reservieren; weder Nabooru noch erwachsene Ruto in dieser Prüfung ersetzt. Produktions-ROM unverändert: `3ca9c4c0054ae075a5db8f5ae18db7f38072d63d11cd3adbaf779afce1a2efe9`.

| Kriterium | Mario Party 3 | Mario Tennis 64 Ver. 2 |
|---|---:|---:|
| Dreiecke im gelieferten OBJ | 420 | 471 |
| Geometriepositionen im OBJ | 330 | 1411 |
| Davon unterschiedliche Koordinaten | 281 | 292 |
| Verwendete Materialien | 3 | 6 |
| Skelett im Paket | 39 Knoten, starre Einzelgewichte | keines im OBJ |
| Materialzuordnung | MTL und Texturen vorhanden | referenzierte MTL fehlt |

**Mario Party 3 ist die empfohlene Grundlage.** Rund 11 % weniger Dreiecke, vorhandene Gelenke und drei einfach nutzbare Texturen. Die drei Basistexturen haben 64×64, 32×64 und 64×64 Pixel mit jeweils höchstens 16 RGBA-Farben. Im N64-CI4-Format samt drei RGBA16-Paletten benötigen sie zusammen **5216 Bytes (5,09 KiB)**. Die weiteren elf PNGs im Quellpaket sind optionale Varianten und müssen nicht alle ständig geladen werden.

Die ZIP-Dateigröße sagt nichts Verläßliches über den Laufzeitspeicher aus. Beim Tennis-OBJ sind zahlreiche Positionen mehrfach exportiert; die 1411 Datensätze sind deshalb kein direkter Faktor für den N64-Bedarf. Die fünf PNGs und das JPEG haben ohne MTL keine sichere Zuordnung zu den sechs Materialien. Mehrere enthalten über 256 Farben und erfordern bei kompakten N64-Texturformaten eine Farbverringerung. Eine faire Gesamtgröße nach Rigging läßt sich dafür noch nicht angeben. Die Party-Dateien enthalten eine gebundene Grundpose, keine fertigen Bewegungssequenzen. Auch dort müssen Naboorus Bewegungen später angepaßt bzw. neu erzeugt und getestet werden.

Die native Nabooru verwendet 650 Dreiecke in ihren Displaylisten; ihr komplettes Objekt mit Animationen und Texturen belegt **98784 Bytes (96,47 KiB)**. Waluigi ist also eine plausible Möglichkeit zur Entlastung. Die tatsächliche Ersparnis steht erst nach seiner fertigen Konvertierung fest. Eigenes Skelett und ursprüngliche Waluigi-Proportionen erhalten; keine erzwungene Streckung auf Naboorus Gelenkabstände.

## Erwachsene Ruto durch Thaddäus

Der Gedanke stimmt: Unsere ausgewählte SuperSponge-Figur hat **254 Dreiecke**, die originale erwachsene Ruto **484** in ihren Displaylisten. Rutos komplettes Objekt `object_ru2` benötigt **63696 Bytes (62,20 KiB)**. Der schon konvertierte Thaddäus fügt dem gewöhnlichen Zora-Objekt derzeit **21696 Bytes (21,19 KiB)** hinzu, einschließlich seines Skeletts, seiner Texturen und der beiden bisherigen Animationen.

Ein wirklich vollständiger Austausch könnte damit überschlägig **42000 Bytes (41,02 KiB)** vor zusätzlichen Weisen-/Schwimm-/Schlußanimationen freigeben. Das ist eine Vergleichsrechnung, kein gemessener fertiger Wasserweisen-Einbau. Die nötigen weiteren Animationen und Verweise müssen erst übertragen werden.

Wichtig für die Umsetzung: Das aktuelle `object_zo` enthält auch die normalen Zora-Daten und ist zusammen mit Thaddäus **70912 Bytes** groß. Würde man einfach dieses ganze Paket statt Rutos Objekt in die Weisen-Szene laden, wären es sogar **7216 Bytes mehr**. Es muß ein schlankes Thaddäus-Objekt an die Stelle der nicht mehr benötigten Erwachsenen-Ruto-Daten treten. Die junge Ruto hat ihr eigenes `object_ru1` und bleibt erhalten. Alte Erwachsenen-Ruto-Daten dürfen erst entfallen, wenn sämtliche erwachsenen Auftritte samt Animationen umgestellt sind.

Ergebnis: beide späteren Ersetzungen als vollständigen Austausch planen; pro gleichzeitig besetzter Szene neu messen. Kein neuer Spielpatch für diese reine Vorprüfung.
