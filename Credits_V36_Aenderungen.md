# Credits V36 – Debug-Start und Pepsi für den Deku-Händler

In der DEBUG-Fassung steht ganz oben im Ortsmenü **Credits starten**. L und R auf Controller 1 gedrückt halten und Z drücken, dann den Eintrag mit A auswählen. Er startet den Abspann am Anfang der Landschaftsmontage im Gerudo-Tal, mit der originalen Abspannmusik und den normalen Szenenwechseln. Alter und Stage-Auswahl im Menü werden dafür passend gesetzt; ein zuvor abgeschlossener Spielstand ist nicht nötig. Mit derselben Tastenkombination lässt sich das Menü wieder öffnen. Beim anschließenden Laden eines normalen Gebiets werden auch die normalen Spielgeräusche wieder eingeschaltet.

Der tanzende Deku-Händler in der Ranch-Feier hält jetzt eine Pepsi-Dose in der rechten Hand. Sie folgt seiner bestehenden Handanimation. Verwendet wird das bereits geladene Dosenmodell: kein zusätzlicher Actor, kein zusätzlicher Objektplatz oder Modellbank; eine zusätzliche 64-Byte-Grafikmatrix pro dargestelltem Frame. Die Position zwischen Pepsiman und Hühnerfrau bleibt erhalten. Normale Deku-Verkäufer erhalten keine Dose.

Geprüft mit 4 MiB RAM: tatsächliches Öffnen des Menüs per Controller und Credits-Start per A, automatische Szenenwechsel vom Gerudo-Tal zur Festung und nach Kakariko, aktive Originalmusik, anschließend Rückkehr über das Debug-Menü ins Hyrule-Feld mit normalen Spielgeräuschen. Die Ranch-Einstellung wurde in Normal und DEBUG durch mehrere Tanzphasen bis Cutscene-Frame 135 geprüft. Weiterhin 12 Objektplätze und 43.968 Bytes freie Objektbank; keine GBI-/Vertexfehler oder Objektbank-Überläufe. Alle Modelle, Dialogdaten und Raumplatzierungen sind gegenüber V35 bytegleich. Kein neuer vollständiger Spieldurchlauf; frühere Credits-Prüfungen bleiben im kumulativen Quellenpaket enthalten.

Credits_Deku_Pepsi_V36.mp4 zeigt die Feier mit originaler Abspannmusik und Spielgeräuschen aus der getesteten Normal-Fassung. Credits_Debug_Menu_V36.png zeigt den neuen Menüeintrag.

Genau einen BPS-Patch auf eine saubere Ocarina of Time Europe PAL 1.0 .z64 anwenden (Basis-MD5 e040de91a74b61e3201db0e2323f768a). Nicht auf eine ältere gepatchte Version anwenden. Alle bisherigen Änderungen enthalten. Der neue Menüeintrag existiert ausschließlich in der DEBUG-Fassung.

Kumulatives Quellenpaket ohne ROM. Letzter normaler Builder: tools/build_credits_v36.py nach build_credits_v35.py. Für DEBUG anschließend tools/build_debug_version.py ausführen; --restore stellt die normalen Quellen wieder her. Reproduktionsskripte und Prüflogs unter validation/credits-v36.
