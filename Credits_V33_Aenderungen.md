# Credits V33 – große Gesten und gezielte Bildkomposition

Alle früheren Spiel-, Dialog- und Modelländerungen sind enthalten.

- Pingu steht in der Mario-/Luigi-Nahaufnahme rechts und etwas hinter Mario. Seine Flossen bewegen sich schnell und weit auf und ab, mit zusätzlicher Vor-/Rückbewegung. Der Kopf bewegt sich mit. Die Anpassung betrifft nur seinen Credits-Auftritt.
- Terri steht wie hinter einem Verkaufstresen: Unterkörper und Beine sind absichtlich in der Kiste verdeckt; der Oberkörper schaut darüber. Sein fester Höhenversatz gilt nur für diese Credits-Figur. Die sichtbare Haltung wurde aus der tatsächlichen Kamera geprüft.
- Crocker steht aus Sicht der Kamera links von Pepsiman, abseits des zentralen Credits-Texts. Er hält eine Pepsi-Dose in der rechten Hand. Die Dose benutzt exakt die Handtransformation und folgt seinem gesamten Tanz. Das bereits geladene Dosenmodell wird wiederverwendet, ohne neuen Actor, Objektplatz oder zusätzliche Modellkopie.
- Shaggy und Fred bekommen deutlich größere und schnellere, abwechselnde Gesprächsgesten. Beide stehen gemeinsam etwas weiter im Bild, damit Fred in der Nahaufnahme erkennbar bleibt. Die Schulterdrehpunkte wurden an die tatsächlichen Armansätze gesetzt. Acht Hals-Hautpunkte in Shaggys Credits-Kopie bleiben am Kopf, damit kräftige Armbewegungen nicht den Hals mitziehen.

Die Kamerafahrten bleiben gegenüber V32 unverändert; die nahe Viererreihe bleibt erhalten. Sitzender Wario, Franky, Marty/Doc, Weisen und alle Spielauftritte der Figuren bleiben unverändert.

## Videos und Bilder

Credits_Gaeste_V33.mp4 enthält die komplette Ranch-Sequenz bis zur Bergszene. Credits_Feinschliff_V33.mp4 zeigt die geänderten Einstellungen als kurzen Zusammenschnitt. Beide verwenden die originale Abspannmusik und Spielgeräusche direkt aus der Emulation. Die Musik wurde nicht nachträglich unterlegt. Kurze Ausschnitte springen musikalisch entsprechend ihren Schnitten; das vollständige Ranch-Video läuft durchgehend.

## Prüfung und Installation

Normal- und DEBUG-Fassung wurden mit 4 MiB RAM durch alle sechs Ranch-Teile und die anschließende Bergszene geführt. Der letzte Hof wurde ebenfalls einschließlich des nativen Bewegungsstopps geprüft. Keine GBI-/Vertexfehler oder Objektbank-Überläufe; keine zusätzlichen Actor- oder Objektplätze. Bodenkontakte aller anderen Zusatzfiguren bleiben geprüft; Terris ausdrücklich gewünschter verdeckter Höhenversatz ist separat berücksichtigt. Mehrere Bewegungsphasen wurden im tatsächlichen Rendering kontrolliert.

Alle bisherigen Objektbanken außer Shaggys gezielt angepasster Credits-Bank bleiben bytegleich. Die anderen fünf Modelle in dieser Bank bleiben in der Quelle unverändert. Dialogbanken, Ladenlogik und sämtliche Credits-Kameradaten bleiben unverändert. Beide BPS-Patches wurden auf die saubere Basis angewendet und ergeben bytegenau die getesteten Dateien. Das ist eine gezielte Szenenprüfung, kein vollständiger Spieldurchlauf.

Genau einen Patch auf eine saubere Ocarina of Time Europe PAL 1.0 ROM im .z64-Format anwenden (Basis-MD5 e040de91a74b61e3201db0e2323f768a). Keine ältere gepatchte ROM als Basis verwenden. Normal und DEBUG sind separate Alternativen.

Das Quellenpaket ist kumulativ. Neuer letzter Builder: tools/build_credits_v33.py nach build_credits_v32.py. Reproduktionsskripte, native Laufzeitlogs und Bank-/Musikprüfung liegen unter validation/credits-v33. Keine ROM enthalten.
