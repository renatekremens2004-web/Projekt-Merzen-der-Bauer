# V46: Panzer-Stellplätze, Wald-Soldat und Geister-Boris

Die Panzer behalten ihre feste Kollision. Es gibt keine Ausnahme für Cutscenes und kein Durchlaufen der Panzerhüllen.

- Der Panzer im schmalen Todesberg-Weg Richtung Kakariko steht jetzt seitlich am breiteren Vorplatz beim Zugang zu Goronia. Link kann den unteren Weg und den Zugang zu Goronia passieren.
- Kakarikos drei Panzer stehen tagsüber und nachts auf der großen Grünfläche am Dorfeingang. Ihre Neigung folgt dem Boden. Die Wege durch das Dorf sowie die Bewegungsabläufe von Bongo Bongo, Link und Sheik bleiben frei.
- Der Soldaten-Gorone in den Verlorenen Wäldern schaut in den offenen Raum statt zur Wand.
- Geister-Boris schwebt in der Kakariko-Kamerafahrt der Credits durch das Bild. Er benutzt seine originale Schwebeanimation, ohne Wettrennen, Belohnung oder Speichermarkierungen auszulösen. Die ursprünglichen Kamerafahrten bleiben erhalten.

## Videos

`Sonnengewand_Erhalt_V46.mp4` zeigt die zusätzliche Sonnengewand-Übergabe in der originalen Halle-der-Weisen-Zeremonie, einschließlich gelber Kleidung und neuem Erhalt-Text. Das Licht-Amulett gehört weiterhin zur Zeremonie. Die Aufnahme enthält Spielmusik und Soundeffekte.

`Boris_Kakariko_Credits_V46.mp4` zeigt Boris während der unveränderten Kakariko-Kamerafahrt, ebenfalls mit Spielmusik.

## Anwenden

Einen der beiden BPS-Patches auf eine **saubere europäische Ocarina-of-Time-PAL-1.0-ROM** anwenden, nicht auf eine bereits gepatchte Version. Beide Patches enthalten alle bisherigen Änderungen. Die saubere Ausgangs-ROM hat MD5 `e040de91a74b61e3201db0e2323f768a`.

- Normal: `Mr_Burns_Mr_Bean_DE_PAL10_Panzer_Boris_V46.bps`
- Mit Debug-Menü: `Mr_Burns_Mr_Bean_DE_PAL10_DEBUG_Panzer_Boris_V46.bps`

DEBUG wie bisher mit **L+R halten, dann Z** öffnen. **C-links** gibt alle Items. **C-rechts** wechselt Standard → Sonnengewand → Schattengewand. **A** lädt den gewählten Ort. Der Credits-Eintrag bleibt verfügbar.

Sonnengewand, oranges Wallace-Gewand und hellblaues Wassergewand halbieren Schaden. Das schwarze Schattengewand bleibt mit einem Viertel Schaden am stärksten. Die Standard-Stufe ist grün, ohne zusätzlichen Schutz.

## Prüfung

Gezielte Tests im nativen Emulator mit 4 MiB: Durchlaufen der betroffenen Wege, feste Panzerkollision, beide Teile der Bongo-Bongo-/Sheik-Szene einschließlich Lernen der Nocturne und Rückkehr ins Dorf, Kind-Zeitlinie ohne Panzer, Blickrichtung des Wald-Soldaten, Boris in den Credits samt anschließendem Szenenwechsel, Sonnengewand-Übergabe und DEBUG-Credits-Einstieg samt Rückkehr.

Alle bisherigen Dialoge und Modellbanken sowie die ursprünglichen Credits-Kamerafahrten sind gegenüber V44 normal / V45 DEBUG erhalten. Beide BPS-Dateien wurden mit einem unabhängigen Patchprogramm erneut angewendet und bytegenau gegen die gebauten Versionen verglichen. Ein vollständiger Spieldurchlauf ist damit noch nicht geprüft.

Die Quellen-ZIP ist kumulativ. Nach `build_sun_tunic_v44.py` folgt `build_placements_v46.py`; `build_debug_version.py` bleibt optional der letzte Schritt für die separate DEBUG-Ausgabe.
