# V47: Lichtgewand mit eigener zweiter Übergabe

Habeck übergibt zuerst das Licht-Amulett in der ursprünglichen Zeremonie. Link trägt dabei noch seine bisherige Kleidung. Danach sagt Habeck:

> Ach ja, das ist noch nicht alles.
>
> SPIELT DIE ANIMATION NOCH MAL AB!

Die Erhalt-Animation samt Kamerafahrt und Fanfare läuft erneut. Diesmal hält Link ein gelbes 3D-Lichtgewand hoch, legt es automatisch an und erhält den zugehörigen Erhalt-Text. Das Gewand bleibt während dieses Texts sichtbar.

Der Name **Lichtgewand** ersetzt Sonnengewand in den Spieltexten, im Ausrüstungsmenü und im DEBUG-Ortsmenü. Das gelbe Symbol bleibt erhalten. Lichtgewand, oranges Wallace-Gewand und hellblaues Wassergewand halbieren den Schaden; das schwarze Schattengewand bleibt mit einem Viertel Schaden am stärksten. Die Wirkung gilt weiterhin für Kind und Erwachsenen.

## Dateien und Anwenden

- Normaler Patch: `Mr_Burns_Mr_Bean_DE_PAL10_Lichtgewand_V47.bps`
- DEBUG-Patch: `Mr_Burns_Mr_Bean_DE_PAL10_DEBUG_Lichtgewand_V47.bps`
- Video mit Spielmusik und Soundeffekten: `Lichtgewand_Zweite_Uebergabe_V47.mp4`
- Kumulative Quellen und beide Patches: `Merzen_Lichtgewand_V47_Quellen_Patch.zip`

Einen der BPS-Patches auf eine **saubere europäische Ocarina-of-Time-PAL-1.0-ROM** anwenden, nicht auf eine zuvor gepatchte Version. Die Ausgangs-ROM hat MD5 `e040de91a74b61e3201db0e2323f768a`. Alle bisherigen Änderungen bis V46 sind enthalten, einschließlich Panzer-Stellplätzen und Geister-Boris.

DEBUG öffnen: **L+R halten, dann Z**. **C-links:** alle Items. **C-rechts:** Standard → Lichtgewand → Schattengewand. **A:** Ort laden.

## Umsetzung und Tests

Eine eigene deutsche Cutscene wiederholt den originalen Erhalt-Abschnitt. Das originale Cutscene-Skript bleibt für die anderen Sprachen erhalten. Die zweite Übergabe verwendet das kleine, vorhandene Gewandmodell mit eigenen gelben Materialien. Die anderen Gewand- und Amulettmodelle sind unverändert. Der zusätzliche Objektbank-Eintrag wird nur in der ersten Halle-der-Weisen-Szene geladen.

Mit 4 MiB im nativen Emulator geprüft: erstes Ziehen des Master-Schwerts, Licht-Amulett vor der Ansage, Lichtgewand erst danach, gelbes Modell während der zweiten Übergabe und des Erhalt-Texts, automatische Ausrüstung und Rückkehr zur Zitadelle der Zeit. Zusätzlich wurden der exakte Name und das gelbe Symbol im Ausrüstungsmenü sowie die drei DEBUG-Gewandstufen und die getrennte Alle-Items-Funktion geprüft.

Alle ursprünglichen Cutscene-Skripte, darunter die neun Credits-Kamerafahrten, bleiben bytegleich erhalten. Vorherige Dialoge bleiben mit Ausnahme der verschobenen Übergabeverknüpfungen und der beiden neuen Gewandtexte erhalten. Beide BPS-Dateien wurden mit einem unabhängigen Patchprogramm erneut angewendet und bytegenau mit den gebauten Versionen verglichen. Ein vollständiger Spieldurchlauf ist damit noch nicht geprüft.

Build-Reihenfolge nach V46: `python3 tools/build_lichtgewand_v47.py /pfad/oot`. Für DEBUG abschließend optional `build_debug_version.py` ausführen. Mit dessen `--restore` wird wieder der normale Produktionsstand hergestellt.
