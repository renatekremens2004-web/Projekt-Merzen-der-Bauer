# Credits V35 – Deku-Händler in der Mitte

Der bestehende tanzende Deku-Händler steht nun in der Kameransicht zwischen Pepsiman und der Frau, die mit Hühnern jongliert. Er steht etwas weiter hinten in der Lücke und verdeckt weder die Gesprächspartner noch die Hühner. Alle anderen Positionen, Tänze, Modelle und Dialoge bleiben unverändert.

Normal und DEBUG wurden in dieser Credits-Einstellung mit 4 MiB RAM bis Cutscene-Frame 135 geprüft, einschließlich mehrerer Bewegungsphasen, Bodenkontakt, aktiver Animation und nativer Abspannmusik. Keine GBI-/Vertexfehler oder Objektbank-Überläufe; weiterhin 12 Objektplätze und 43.968 Bytes freie Objektbank in dieser Einstellung. Die vollständigen Credits-Prüfungen aus V34 bleiben im kumulativen Quellenpaket enthalten.

Der binäre Vergleich mit V34 bestätigt: Nur der bestehende Actor-Eintrag im Ranch-Raum unterscheidet sich (zusätzlich zur ROM-Verwaltung beim Packen). Sämtlicher ausführbarer Code, alle Modelle, Dialoge und Kameradaten bleiben bytegleich. Beide BPS-Patches ergeben nach dem Anwenden auf die saubere Basis genau die getesteten Dateien.

Credits_Deku_Mitte_V35.mp4 zeigt die Einstellung mit originaler Abspannmusik und Spielgeräuschen direkt aus der Emulation; Credits_Deku_Mitte_V35.png zeigt die neue Position.

Genau einen Patch auf eine saubere Ocarina of Time Europe PAL 1.0 .z64 anwenden (Basis-MD5 e040de91a74b61e3201db0e2323f768a). Normal und DEBUG sind separate Alternativen. Keine ältere gepatchte ROM als Basis verwenden.

Kumulatives Quellenpaket ohne ROM. Letzter Builder: tools/build_credits_v35.py nach build_credits_v34.py. Reproduktionsskripte und Prüflogs unter validation/credits-v35.
