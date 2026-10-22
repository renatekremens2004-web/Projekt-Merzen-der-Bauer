# Credits V37 – Goronen räumen die CDU-Bombe weg

Die erste Todesberg-Kamerafahrt im Abspann zeigt acht zusätzliche Goronen am Eingang von Goronia:

- Vier Goronen mit den gelieferten Soldatenhelmen tragen die bestehende CDU-Bombe waagerecht in gemeinsamer Formation. Ihre Beine verwenden die native Goronen-Laufanimation; die Armposen gleichen die unterschiedlichen Bodenhöhen aus. Die Bombe bewegt sich im selben Takt.
- Ein fünfter Gorone mit Soldatenhelm steht seitlich vor dem Transport und gibt große, wiederholte Rangierzeichen mit beiden Armen.
- Drei weitere Goronen tragen gelbe Bauhelme. Sie stehen im Hintergrund und nähern sich zeitversetzt, bevor sie wieder stehen bleiben.

Verwendet wird der PS2-Soldatenhelm mit 176 Dreiecken statt der Alternative mit 328. Der Bauhelm hat 60 Dreiecke und wurde gelb eingefärbt. Alle acht Goronen teilen sich das unveränderte Originalmodell. Helme und bestehende Bombe liegen in einer gemeinsamen zusätzlichen Objektbank. Die Helme folgen der tatsächlichen Kopfanimation. Es gibt keine neue Explosionsfunktion, keine neuen Dialoge oder Auswirkungen auf normale Goronen.

Die Szene wird ausschließlich im ersten Todesberg-Credits-Header geladen (Scene-Layer 7). Originalkamera, Texte, Abspannmusik, Dauer und Übergang nach Goronia bleiben erhalten. Die spätere Todesberg-Szene mit den Weisen und alle bisherigen Änderungen bleiben enthalten.

## Prüfung

Normal und DEBUG wurden mit 4 MiB RAM durch die vollständige Einstellung und den anschließenden Übergang nach Goronia geprüft. Alle acht Goronen werden dargestellt, ihre Positionen liegen auf dem tatsächlichen Boden, die sieben Laufanimationen schreiten fort und die originale Staff-1-Musik ist aktiv. Keine GBI-/Vertexfehler oder Objektbank-Überläufe. Die Einstellung nutzt 19 Objektplätze; die Objektbank hat noch 126.704 Bytes frei.

Anhand der tatsächlichen Gelenkstellungen im Testbild bei Cutscene-Frame 153 wurden die acht Handflächen der vier Träger nachgerechnet. Ihre Höhen unterscheiden sich um rund 0,073 Spieleinheiten. Dies kontrolliert den Ausgleich der unterschiedlichen Bodenhöhen.

Zusätzlich wurde die DEBUG-Fassung über L+R+Z geöffnet und „Credits starten“ mit A ausgewählt. Der natürliche Ablauf vom Gerudo-Tal über Festung und Kakariko zu unserer neuen Todesberg-Szene und weiter nach Goronia funktioniert. Danach wurde über das Debug-Menü ins Hyrule-Feld zurückgekehrt; normale Spielgeräusche waren wieder eingeschaltet.

Binär geprüft: Alle bisherigen Modell- und Dialogbanken sowie andere Räume bleiben bytegleich. Die beiden Todesberg-Credits-Cutscenes bleiben bytegleich; im zugehörigen Scene-Segment unterscheiden sich nur die notwendigen Raum-VROM-Adressen. Beide BPS-Patches ergeben nach dem Anwenden auf die saubere Basis exakt die getesteten Dateien. Die normale Fassung wurde zuletzt wiederhergestellt und neu gebaut. Geprüft wurde der beschriebene Credits-Abschnitt, kein neuer vollständiger Spieldurchlauf.

Credits_Goronen_Bombe_V37.mp4 zeigt 21,08 Sekunden der echten Kamerafahrt samt Übergang und originaler Abspannmusik aus der getesteten Normal-Fassung. Zwei PNGs zeigen Tragegruppe und Bauhelme. Es wurde keine Musik nachträglich unterlegt.

## Anwenden

Genau einen Patch auf eine saubere Ocarina of Time Europe PAL 1.0 .z64 anwenden (Basis-MD5 e040de91a74b61e3201db0e2323f768a). Nicht auf eine ältere gepatchte Version anwenden. Normal und DEBUG sind getrennte Alternativen und enthalten alle bisherigen Änderungen.

DEBUG: L+R gedrückt halten und Z drücken, ganz oben „Credits starten“ auswählen und A drücken. Der Abspann startet am Anfang der Landschaftsmontage.

Kumulatives Quellenpaket ohne ROM. Letzter Builder: tools/build_credits_v37.py nach build_credits_v36.py. Für DEBUG anschließend tools/build_debug_version.py ausführen; --restore stellt die normalen Quellen wieder her. Quellen der zusätzlichen Helme sind als reduzierte Modell-JSONs und Texturen enthalten. Reproduktionsskripte und Prüflogs unter validation/credits-v37.
