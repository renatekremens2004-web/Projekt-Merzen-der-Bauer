# V41 – Wawa-Brüder am mittleren Festungsausgang

Kumulativ auf V40: alle bisherigen Änderungen sind enthalten. Beide BPS-Dateien auf eine saubere europäische PAL-1.0-ROM (.z64) anwenden, MD5 `e040de91a74b61e3201db0e2323f768a`.

Wawario steht links direkt vor dem tatsächlichen mittleren Ein-/Ausgang der Gerudo-Festung, als hätte er sie gerade verlassen. Wawaluigi steht rechts daneben auf derselben Dachterrasse; beide schauen einander an. Die kleine Größe bleibt erhalten. Ihre Füße stehen auf dem vorhandenen Boden bei Y=733. Der bisherige Platz an der Ecke hinter dem Vordergrundzaun entfällt. Die komplette originale Kamerafahrt bleibt bytegleich mit V40.

In Mauzis Credits-Einstellung stehen jetzt vier verlassene Panzer in der Ferne. Drei zusätzliche Exemplare sind mit unterschiedlichen Ausrichtungen und Abständen über das gegenüberliegende Plateau verteilt. Alle teilen sich das vorhandene Modell mit 282 Dreiecken und 14.672 Bytes. Die Objektbank belegt deshalb weiterhin 982.384 Bytes; 37.520 Bytes bleiben frei. Die Platzierungen der Panzer und Soldaten im normalen Spiel bleiben unverändert.

Das MP4 zeigt beide Einstellungen im Spiel mit der originalen Credits-Musik und den Spielgeräuschen.

Geprüft: normale Credits-Sequenz mit 4 MiB RAM inklusive Übergang ins nächste Gebiet; DEBUG-Start über „Credits starten“ und Rückkehr ins normale Spiel mit wieder aktivem Ton. Beide BPS-Dateien wurden erneut auf die saubere Basis angewendet und bytegenau mit den geprüften Builds verglichen. ROM-Prüfsummen stimmen. Sämtliche Dialoge, Objektbanken, Kameras sowie die normalen Kinder-/Erwachsenen-Actorlisten sind unverändert. Durch die zusätzlichen Credits-Einträge verschiebt sich lediglich eine bestehende Modelladresse; die zugehörige Referenz wurde geprüft.

DEBUG-Menü: L+R halten und Z drücken. Letzter normaler Builder: `tools/build_credits_v41.py` nach dem vollständigen V40-Stand. DEBUG anschließend separat mit `tools/build_debug_version.py` erzeugen.
