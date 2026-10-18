# Grafikprüfung vom 19.10.2026

Die großen fehlenden Wandflächen beim Wundererbsen-Händler und in der Halle der Weisen entstehen im untersuchten GLideN64-/Mesa-Aufbau bei abgeschaltetem Software-Clipping. Mit `EnableClipping=True` werden sie bei denselben Kamerakoordinaten gezeichnet. Die frühere pauschale Empfehlung, Clipping abzuschalten, war falsch und wird durch diese Prüfung ersetzt.

ROM und veröffentlichter Zora-/Jabu-BPS-Patch sind unverändert. Korrigiert wurden Aufnahme-Konfiguration, Dokumentation und aktuelles Händler-Beispielbild. Eine Grafik-Plugin-Einstellung wird nicht im BPS gespeichert.

## Ergebnisse

| Fundstelle | Vergleich und Befund |
| --- | --- |
| Wundererbsen-Händler | Die unveränderte Original-ROM zeigt bei ausgeschaltetem Clipping dieselben fehlenden Wanddreiecke. Eingeschaltet erscheint die Wand. Original und Patch haben dieselbe Kamera. Der Händler bleibt in den neuen Vergleichen an seinem nativen Standort; der frühere Versetzungsversuch erklärt den Fehler nicht allein. |
| Halle der Weisen | Aktueller Patch mit Clipping aus/an geprüft. Bei gleicher Kamera verschwinden die großen schwarzen Aussparungen mit eingeschaltetem Clipping. Das Original mit aktivem Clipping dient als weitere Gegenprobe. |
| Krabbelminen-Bowling | Der schwarze Hintergrund hinter der linken Leuchttafel ist auch im Original bei aktivem Clipping vorhanden. Original und Patch verwenden dieselbe Nahaufnahme. Hier ist keine zusätzliche fehlende Wand durch den Patch nachgewiesen. |
| Wiegenlied | Original und Patch durchlaufen Gespräch, vorgespielte Melodie, Eingabe der richtigen Noten und Wechsel nach Hyrule-Feld. Die bereits vorhandene Kameraanpassung für Bean bleibt bestehen. Offene Hofränder und abschließender Übergang sind auch im Original sichtbar; die abschließende Hofaufnahme wurde bei identischen Kamerakoordinaten verglichen. |
| Navi | Die Umgebung wird während der Hinweis-Nahaufnahme im Original und im Patch dunkel. Die unveränderte Navi-Logik ruft `Environment_AdjustLights` auf und verändert Nebel und Beleuchtung. Dies bleibt erhalten. Die Texte sind unterschiedlich lang; ihre Nahaufnahmen sind kein pixelgleicher Kamera-A/B-Test. |

Sechs zahlenmäßige Kamera-Gegenprüfungen stehen in `validation/grafik/runtime-vergleich.json`. Insgesamt wurden zwölf gültige Szenarien mit tatsächlich 4 MB emuliertem RAM ausgewertet. Fünfzehn unveränderte PNGs einschließlich Herkunft und Prüfsummen stehen unter `previews/grafik/`.

## Aufnahme-Konfiguration

```ini
[Video-GLideN64]
EnableClipping = True
EnableCustomSettings = False
```

Nach einer Änderung den Emulator neu starten. Andere Plugins können die Option anders benennen. Dies belegt den verwendeten GLideN64-/Mesa-Aufbau, nicht sämtliche Emulatoren oder echte N64-Hardware.

## Methode und Grenzen

Original-PAL-1.0-ROM und veröffentlichter Produktionsbuild werden direkt geladen. Der Helfer setzt einen vorbereiteten Fortschrittsstand im Emulator-RAM und startet die Szene über native Szenen-/Gamestate-Logik. Die ROM-Dateien bleiben unverändert. Beim Händler wird ein Wiedereinstiegspunkt auf seiner normalen Plattform verwendet. Die Bowling-Nahaufnahme setzt Link vor die Theke. Der frische Wiegenlied-Test startet ohne versetzte Figuren und benutzt reguläre Controller-Tasten einschließlich Liednoten. Navis Test setzt ihre Hinweis-Verfügbarkeit; die Produktions-ROM behält ihre normalen Abklingzeiten.

Die Raumdaten von Fluß, Quelle, Bowling, Halle und Hof sind bytegleich mit dem Original; siehe `validation/grafik/static-vergleich.json`. Das allein hätte keinen Darstellungsfehler ausgeschlossen, weshalb zusätzlich Laufzeitvergleiche durchgeführt wurden.

Unbrauchbare Vorversuche zählen nicht als bestandene Prüfungen: eine Bowling-Aufnahme mit erwachsenem Link, ein bereits fortgeschrittener Wiegenlied-Teststand, zwei fehlerhafte Navi-Teststarts über den laufenden Titelübergang und eine schwarze Screenshot-Rückleseprobe mit Glide64mk2. Die Szenen wurden anschließend mit passenden Testständen beziehungsweise direktem nativem Gamestate-Start erfolgreich erneut aufgenommen. Kein vollständiger Spieldurchlauf und kein Hardware-Test.

Produktions-ROM SHA256: `e211e8e908a2573578d93ce6e47f01ba82c4bc25729694dc72d74d6afc978ec1`.

Unveränderter BPS SHA256: `3f66f32317d089f98893616840000a973014b890da339a0c264d43729e86c09a`.
