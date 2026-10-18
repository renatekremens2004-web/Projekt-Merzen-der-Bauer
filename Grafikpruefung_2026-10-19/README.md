# Schwarze Flächen: Originalvergleich vom 19.10.2026

Die fehlenden Wandflächen beim Wundererbsen-Händler und in der Halle kamen im geprüften Cloud-Aufbau von abgeschaltetem GLideN64-Software-Clipping. Mit **EnableClipping=True** werden sie bei gleicher Kamera gezeichnet. Die frühere Empfehlung zum Abschalten war falsch. **Der BPS-Patch bleibt unverändert.** Nach Umstellen den Emulator neu starten; automatische Spielprofile waren für die Vergleiche ausgeschaltet.

| Stelle | Original / Kontrolle | Aktueller Patch |
| --- | --- | --- |
| Händler | [Clipping aus](Haendler_Original_Clipping_aus.png), [Clipping an](Haendler_Original_Clipping_an.png) | [Wand korrekt gezeichnet](Haendler_Patch_Clipping_an.png) |
| Halle | [Original](Halle_Original_Clipping_an.png), [Patch mit Clipping aus](Halle_Patch_Clipping_aus.png) | [Clipping an](Halle_Patch_Clipping_an.png) |
| Bowling | [Original](Bowling_Original.png) | [Patch](Bowling_Patch.png) – schwarzer Leuchttafel-Hintergrund auch im Original |
| Wiegenlied | [Original](Wiegenlied_Original.png), [Original-Hofrand](Wiegenlied_Original_Hofrand.png) | [Bean](Wiegenlied_Patch.png), [Noten](Wiegenlied_Patch_Noten.png), [Hofrand](Wiegenlied_Patch_Hofrand.png) |
| Navi | [Original](Navi_Original.png) | [Patch](Navi_Patch.png) – native Abdunklung während der Hinweise |

15 unveränderte Emulator-PNGs. Herkunft, Frame und Prüfsummen: [Aufnahmen.json](Aufnahmen.json). Die Texte können sich beim Aufnehmen noch aufbauen. Der Händler bleibt diesmal am normalen Standort. Original und Patch wurden mit 4 MB geprüft; sechs Kamera-Vergleiche sind zahlenmäßig abgeglichen. Das Wiegenlied wurde in beiden Fassungen einschließlich Noteneingabe und Übergang nach Hyrule-Feld abgeschlossen. Offene Hofränder gibt es auch im Original.

Ausführliche Methode und Grenzen: [Prüfbericht](Pruefbericht.md). Kein vollständiger Spieldurchlauf und kein N64-Hardware-Test. Teststart und Fortschrittsdaten wurden nur im Emulator-RAM vorbereitet; die ROM-Dateien wurden nicht verändert.
