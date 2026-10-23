# DEBUG V45: Standard-, Sonnen- und Schattengewand auswählen

Der Gewand-Schalter im DEBUG-Ortsmenü bietet jetzt drei eindeutige Stufen. Alle übrigen Änderungen aus V44 bleiben erhalten. Die normale V44 wurde nicht verändert.

## Bedienung

**L + R halten und Z drücken**, um das Ortsmenü zu öffnen. Mit **C-rechts** durch die Gewänder schalten:

| Auswahl | Farbe | Gewöhnlicher Schaden |
| --- | --- | --- |
| Standard | Grün | Voller Schaden |
| Sonnengewand | Gelb | Halber Schaden |
| Schattengewand | Schwarz | Ein Viertel Schaden |

Nach dem Schattengewand geht die Auswahl wieder auf Standard zurück. Anschließend mit **A oder Start** den gewählten Ort laden; dabei wird das gewählte Gewand angelegt. Die Auswahl gilt für Kind und Erwachsen.

**C-links: Alle Items** bleibt eine unabhängige Aktion. Sie füllt Ausrüstung, Munition, Magie und die übrigen bereits in V44 beschriebenen Gegenstände auf, verändert aber nicht mehr die Gewandstufe. Damit ist auch die Kombination **Alle Items + grünes Standardgewand** möglich.

Wird die Gewandwahl nicht betätigt, bleibt die bisherige Stufe erhalten. Standard setzt gezielt beide Gewand-Upgrades zurück; Sonnengewand aktiviert Gelb und entfernt das Schatten-Upgrade; Schattengewand aktiviert Schwarz. Andere Story- und Navi-Markierungen bleiben erhalten.

Das orange Wallace-Gewand und das hellblaue Zora-Gewand halbieren weiterhin den Schaden. Ein bereits separat erworbener nativer Doppelverteidigungsbonus wird durch die Gewandwahl nicht entfernt. Die Boni werden weiterhin nicht miteinander multipliziert.

## Geprüft

- Zehn native Ladedurchläufe mit **4 MiB RAM**, einschließlich aller drei Gewänder bei Kind und Erwachsen.
- Alle Items zusammen mit Standard, Sonne und Schatten; vorhandene Flaschenpost, Tauschgegenstände und andere Fortschrittsmarkierungen bleiben erhalten.
- „Credits starten“ und die Rückkehr ins Spiel funktionieren weiter.
- Alle Modellbanken, Räume, Text- und Textursegmente sowie die neun geprüften Credits-Kamerafahrten sind gegenüber DEBUG V44 unverändert.
- Die wiederhergestellte normale ROM ist byteidentisch zur normalen V44.
- Der neue BPS-Patch wurde mit Quellprüfung angewendet und das Ergebnis bytegenau mit dem Build verglichen. Kein vollständiger Spieldurchlauf.

## Installation

Den DEBUG-V45-Patch auf die **saubere europäische PAL 1.0 (.z64)** anwenden, nicht auf eine ältere gepatchte ROM. MD5 der Quell-ROM: `e040de91a74b61e3201db0e2323f768a`.

Das kumulative Quellenarchiv enthält den neuen DEBUG-V45-Patch und den unveränderten normalen Sonnengewand-V44-Patch. Es enthält keine ROM.
