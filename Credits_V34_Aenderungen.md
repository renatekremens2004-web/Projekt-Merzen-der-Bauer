# Credits V34 – Gespräch und Pinguin-Tänze

Alle früheren Spiel-, Dialog- und Modelländerungen sind enthalten.

- Pepsiman und Crocker schauen einander an. Beide bleiben an ihren zuletzt gewählten Plätzen und gestikulieren abwechselnd wie in einem Gespräch. Crockers Pepsi-Dose folgt weiterhin seiner rechten Hand.
- Skipper, Kowalski, Private und Rico tanzen mit schnellen, großen Flossenbewegungen wie Pingu. Ihre individuellen Grundwinkel berücksichtigen die bereits nach unten modellierten Flossen, damit die Bewegung außerhalb des Bauchs bleibt. Versetzte Phasen geben ihnen unterschiedliche Bewegungen.
- Drei Pinguin-Standorte sind für den größeren Bewegungsraum versetzt. Die Bewegungsbereiche aller vier Modelle wurden über den vollständigen gemeinsamen Zyklus geprüft; sie überschneiden sich gegenseitig nicht und die Flossen schneiden nicht durch den Boden. Zusätzlich wurden die Nachbarfiguren im echten Rendering über mehrere Bewegungsphasen kontrolliert. Die Abschätzung der Abstände zu Originalfiguren anhand großzügiger Körperradien ist getrennt von dieser Sichtprüfung dokumentiert.
- Terri hat entspannte, überwiegend abgesenkte Arme hinter seiner Kiste statt ausgestreckter T-Pose-Arme. Kleine Bewegungen bleiben erhalten; seine Beine bleiben wie gewünscht verdeckt.

Der von Dir bestätigte Pingu-Auftritt, die Gesprächsgesten von Shaggy/Fred sowie alle Kamerafahrten bleiben unverändert. Keine neuen Modelle, Actor- oder Objektplätze. Alle Modellbanken bleiben bytegleich zu V33.

## Videos und Prüfung

Credits_Feinschliff_V34.mp4 zeigt die neuen Tänze, Terri und das Gespräch. Credits_Gaeste_V34.mp4 enthält die komplette Ranch-Sequenz bis zur Bergszene. Beide verwenden die originale Abspannmusik und Spielgeräusche direkt aus der Emulation. Musik in kurzen Ausschnitten springt entsprechend den Bildschnitten; die komplette Aufnahme läuft durchgehend.

Normal und DEBUG wurden mit 4 MiB RAM durch alle sechs Ranch-Teile und die anschließende Bergszene geführt. Der letzte Hof wurde einschließlich des nativen Bewegungsstopps geprüft. Keine GBI-/Vertexfehler oder Objektbank-Überläufe. Bodenkontakte der Zusatzfiguren sind geprüft; Terris ausdrücklich gewünschter verdeckter Höhenversatz ist separat berücksichtigt.

Dialogbanken, Ladenlogik, alle Modelle und sämtliche Credits-Kameradaten bleiben unverändert. Beide BPS-Patches wurden auf die saubere Basis angewendet und ergeben bytegenau die getesteten Dateien. Das ist eine gezielte Szenenprüfung, kein vollständiger Spieldurchlauf.

## Installation und Quellen

Genau einen Patch auf eine saubere Ocarina of Time Europe PAL 1.0 ROM im .z64-Format anwenden (Basis-MD5 e040de91a74b61e3201db0e2323f768a). Keine ältere gepatchte ROM als Basis verwenden. Normal und DEBUG sind separate Alternativen.

Das Quellenpaket ist kumulativ. Neuer letzter Builder: tools/build_credits_v34.py nach build_credits_v33.py. Reproduktionsskripte, Laufzeitlogs, Abstands- und Musikprüfung liegen unter validation/credits-v34. Keine ROM enthalten.
