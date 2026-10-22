# Credits V32 – Verteilung, Gesten und Musikaufnahme

Alle bisherigen Spiel-, Dialog- und Modelländerungen sind enthalten.

- Crocker, Pepsiman, Deku-Händler und Hühnerfrau stehen lockerer verteilt. Der Deku-Händler verdeckt Crocker nicht mehr; die Pepsi-Dosen liegen bei Pepsiman.
- Terri steht anstelle der entfernten ursprünglichen Krabbelminenfrau hinter der Kiste, mit kleinen Armbewegungen. Sein korrigiertes Modell nutzt dieselbe Objektbank wie Fanboy/Chum Chum, ohne zusätzlichen Objektplatz oder Ladenlogik.
- Die Viererreihe mit Mackey, Doofenshmirtz, Maskenhändler und Trankhändler bekommt die ursprüngliche relative Kameradistanz zurück: Die Fahrt wurde um denselben Versatz wie die Figuren verschoben. Brennweite, Tempo und restliche Kameras entsprechen dem Original.
- Shaggy und Fred sind zueinander ausgerichtet und bekommen abwechselnde kleine Gesprächsgesten. Füße und Standort bleiben fest.
- Die Pinguine stehen weiter außerhalb der tanzenden Zora-Flossen. Die Mario-/Luigi-Einstellung und verschiedene Phasen der Zora-Bewegung wurden im tatsächlichen Rendering kontrolliert.
- Franky, der sitzende Wario, Marty/Doc im letzten Hof und die Weisen bleiben unverändert. Die bisherigen starken Tänze für Fanboy/Crocker und Wawa-Arme bleiben enthalten.

## Videos mit originaler Musik

Credits_Gaeste_V32.mp4 zeigt die komplette Ranch-Sequenz bis zur Bergszene (117,70 Sekunden). Credits_Feinschliff_V32.mp4 zeigt die geänderten Einstellungen als kurzen Zusammenschnitt.

Beide enthalten den direkt im Emulator aufgenommenen Originalton mit Abspannmusik und Soundeffekten. Für den Einstieg mitten in die Credits setzt die Testdatei den übernommenen BGM-Status zurück; der native Szenenstart spielt dann NA_BGM_STAFF_2. Der letzte Hof wurde ebenfalls mit NA_BGM_STAFF_4 geprüft. Die Musik wurde nicht nachträglich unterlegt. Im Patch wurden weder Musikdaten noch Audiologik verändert. Kurze Ausschnitte springen musikalisch entsprechend ihren Schnitten; das vollständige Ranch-Video läuft durchgehend.

## Prüfung

Normal und DEBUG durchlaufen alle sechs Ranch-Teile mit nativen Übergängen, anschließend die Bergszene. Der letzte Hof wurde in beiden Fassungen einschließlich des abschließenden Bewegungsstopps geprüft. Jede Aufnahme läuft mit 4 MiB RAM; keine GBI-/Vertexfehler oder Objektbank-Überläufe. Terris Erweiterung belegt 12.896 zusätzliche Bytes in einer vorhandenen Bank. In seiner Einstellung verbleiben 33.728 Bytes freier Objektbank-Speicher; die Anzahl der Objektplätze bleibt gleich.

Geprüfte Bodenkontakte aller Zusatzfiguren, mehrere Gesten-/Kameraphasen, originaler Musikspieler während der Aufnahmen und synchroner Ton. Alle bisherigen Objektmodelle und Dialogbanken bleiben unverändert; vorhandene Fanboy-/Chum-Chum-Daten in der erweiterten Bank bleiben bytegleich. Die Laden- und Erbsenhändlerlogik ist unverändert. Beide BPS-Patches wurden auf die saubere Basis angewendet und ergeben bytegenau die getesteten Dateien. Das ist eine gezielte Szenenprüfung, kein vollständiger Spieldurchlauf.

## Installation und Quellen

Genau einen Patch auf eine saubere Ocarina of Time Europe PAL 1.0 ROM im .z64-Format anwenden (Basis-MD5 e040de91a74b61e3201db0e2323f768a). Keine ältere gepatchte ROM als Basis verwenden. Normal und DEBUG sind separate Alternativen.

Das Quellenpaket ist kumulativ. Neuer letzter Builder: tools/build_credits_v32.py nach build_credits_v31.py. Reproduktionsskripte, native Laufzeitlogs, Kamera-/Bank-/Musikprüfung und Prüfsummen liegen unter validation/credits-v32. Keine ROM enthalten.
