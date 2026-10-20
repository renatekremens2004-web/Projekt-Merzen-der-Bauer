# Wallace läuft; Weisen-Waluigi paßt zur ursprünglichen Größe

Kumulativer Gesamtpatch für die unveränderte Europa/PAL-1.0-ROM. Vanilla-MD5 `e040de91a74b61e3201db0e2323f768a`, Ziel-SHA256 `3789ff2805ff2c5b5e53c2f7bd44935c4c2cf01dca425a7610c61890f210e1f9`. Weiterhin 40 MiB. Alle bisherigen Änderungen enthalten, einschließlich kleinerem blauen Wawaluigi, Punk-Armen und Triangle Guys ursprünglicher Begrüßung plus Triforce-Zusatz. Keine Dialoge in diesem Schritt geändert; die bereits vorab gelieferte Brunnen-/Schattentempel-Liste bleibt aktuell.

## Wallace

Der vorherige Ersatz hatte lediglich Körper, Kopf und zwei Arme. Seine Beine waren Teil des starren Körpers, während der native Goronen-Akteur bereits auf dem Fluchtweg bewegt wurde. Jetzt hat das gleiche Modell zehn starre Matrixgruppen: Körper, Kopf, beide Arme, beide Oberschenkel, beide Unterschenkel und beide Füße. Höhe weiterhin 90 Spieleinheiten, 2.269 Dreiecke. Alle Modellpositionen, Dreiecke, Normalen, UVs und Texturen erhalten. Nur die Zuordnung der bestehenden unteren Körpervertices zu den neuen Beinteilen ändert sich.

Eine sechzehn Frames lange Gehbewegung ist auf den nativen Fluchtablauf abgestimmt. Zweigliedrige inverse Kinematik läßt das Standbein am Boden stehen und hebt den anderen Fuß an; die Fußmatrix hält die Sohle waagerecht. Sanfter Beginn und Ausklang. Die Bewegung ist ausschließlich im vorhandenen Fluchtzustand 2 bei positiver Geschwindigkeit aktiv. Weisen- und Credits-Auftritte behalten ruhige Beine. Keine Änderung an AI, Bodenschalter, Zelltür, Gespräch, Fluchtweg, Geschwindigkeit, Zustandszeiten oder Belohnung. Die bereits angepaßte Fluchtkamera bleibt erhalten. Sechs weitere 64-Byte-Matrizen pro Zeichnung (384 Bytes); keine zusätzlichen Dreiecke oder Objekt-Slots. Objekt-/Raumdaten wachsen durch zusätzliche Matrixbefehle um je 672 Bytes, bleiben in den vorhandenen Puffern.

## Waluigi

Gemeint ist Waluigi als Ersatz für Naboru, nicht der blaue Wawaluigi am Gerudo-Zelt. Vergleich bei gleicher Standanimation und Akteursskalierung 0,01: Naboru etwa 65,47 Spieleinheiten, bisheriger Waluigi 97,51, neuer Waluigi 73,13. Gleichmäßiger Faktor 0,75 auf sämtliche Modellachsen, eigenen Knochenabstände und Animationswurzelpositionen. So bleibt er etwa 12 Prozent größer als Naboru, statt rund 49 Prozent. Eigene Proportionen bleiben erhalten. 420 Dreiecke, 14 eigene Knochen, Texturen, Normalen, UVs und alle 22 Naboru-Animationen plus die Iron-Knuckle-Enthüllung mit identischen Rotationen und Framezahlen. Das Objekt bleibt exakt 60.144 Bytes groß.

Der kleinere Waluigi gilt bei der Begegnung als Kind, der Entführung, der erwachsenen Enthüllung, dem Weisen-Auftritt, Finale und Credits. Nur die zuvor für das größere Modell korrigierten Nahaufnahmen werden passend neu gerahmt. Geändert sind ausschließlich Augen-/Zielkoordinaten: Halle (Gruppen 263/363/433), Enthüllung (65/85/140/222), spätere Siegelszene (110), Credits-Nahaufnahme (246). Alle Kamera-Zeiten, FOVs, Cutscene-Cues, Texte, Bewegungs- und Questbefehle bytegleich. Andere Kameragruppen bleiben erhalten. Blaue Wawaluigi-Figur, orange Wawario-Figur und normaler Wario unverändert.

## MP4-Nachweise

| Datei | Dauer | Bilder |
| --- | ---: | ---: |
| Waluigi_01_Begegnung_Kind.mp4 | 168.30 s | 2805 |
| Waluigi_02_Entfuehrung.mp4 | 77.82 s | 1297 |
| Waluigi_03_Eisenprinz_Enthuellung.mp4 | 75.30 s | 1255 |
| Waluigi_04_Halle_der_Weisen.mp4 | 185.58 s | 3093 |
| Wallace_Laufanimation_Befreiung.mp4 | 69.00 s | 1150 |
| Wallace_Waluigi_Weisen_Credits.mp4 | 38.82 s | 647 |

Alle sechs Videos sind fortlaufende echte Emulatoraufnahmen desselben oben angegebenen finalen Builds mit tatsächlichen 4 MiB N64-RAM. 640×480, H.264, PAL 50/3 Bilder pro Sekunde, ohne Ton. Keine ersetzten oder für die Vorschau versetzten NPCs/Kameras. Die Kamerakorrekturen sind Teil des spielbaren Patches. Lokale Ausgangsspielstände setzen die jeweiligen Kapitel voraus; danach normale Controller-Eingaben und native Szenen. Keine Akteurspositionen, Schalter, Belohnungen oder Animationszustände für diese Aufnahmen verändert. Beginn/Ende, vollständige gerenderte Framezahl, Reihenfolge und MP4-Framezahl geprüft. Lange Clips lesen jeden gerenderten Frame per nativer READ_SCREEN-API; keine 1.000-Screenshot-Grenze. Standbilder werden unverändert aus diesen Quelldaten in PNG umgewandelt. Kein Ton aufgenommen.

Die Kinderbegegnung enthält alle Gesprächsseiten bis zur Zusage und Waluigis anschließenden nativen Bewegung. Die Entführung endet nach dem regulären Szenenende, die Enthüllung nach der Konfrontation mit den Hexen, die Halle nach dem Amulett und der nativen Rückkehr. Wallace wird über den echten Bodenschalter befreit, liest seine Gesprächsseiten und läuft selbständig aus der Zelle. Die gemeinsamen Weisen-Credits enthalten auch die unverändert auf dem kleineren Wallace sitzende Krabbelminenfrau und den regulären Szenenübergang.

## Prüfung und Grenzen

Alle 1.509 komprimierten Segmente gegen den unkomprimierten Neubau und CIC-6105-Prüfsumme geprüft. Sämtliche deutschen, englischen und französischen Texte unverändert, einschließlich aller 1.013 eigenen Nachrichten. Native Kernfunktionen erhalten: 2955; Goronenfunktionen 98; Feuerweisenfunktionen 94; Naboru-Funktionen 124; Iron-Knuckle-Funktionen 71; Waldweisenfunktionen 74. Private Zeichnung ist erweitert; ursprüngliche Spielsteuerung bleibt erhalten. Geprüfte ideale Stand-/Schwungfuß-Geometrie ohne Bodendurchdringung, einschließlich der Überblendung. Vollständige Protokolle und Größenvergleich im Quellenpaket.

Kein beobachteter Absturz, Objektpufferüberlauf oder ungültiger Grafikbefehl in diesen Proben. Ein vollständiger normaler Durchlauf und echte N64-Hardware sind damit noch nicht geprüft. RomPatcher.js mit eingeschalteter Quellvalidierung erzeugt aus Vanilla und dem BPS bytegenau diese Produktions-ROM. Keine ROMs, Spielstände, Savestates, RAM-Abzüge oder ausführbaren Dateien veröffentlicht. MP4s liegen getrennt vom Quellenarchiv und zusätzlich gemeinsam im Video-ZIP.

Für weitere Builds `build_walk_followup.py` nach `build_character_sizes.py` ausführen. Die vorbereiteten eigenen Modelle und Kameradaten sind enthalten. Blender weiterhin mit `--python-exit-code 1` starten.
