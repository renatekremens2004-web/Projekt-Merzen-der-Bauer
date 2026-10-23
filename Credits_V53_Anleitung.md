# V53: engeres Deltarune-Trio und Credits-Auftritte

Beide BPS-Patches sind kumulativ und enthalten sämtliche bisherigen Änderungen. Genau einen auf eine saubere europäische PAL-1.0-ROM anwenden (MD5 `e040de91a74b61e3201db0e2323f768a`), nicht auf eine schon gepatchte ROM.

## Deltarune-Trio

Kris, Susie und Ralsei stehen nun als kleine, eng zusammenstehende Gruppe an derselben sicheren Seite des Donnerblumen-/Treppenraums von Dodongos Höhle. Ihre Abstände sind auf ungefähr 51, 51 und 101 Welteinheiten verkürzt. Größen, Modelle, leichte Bewegungen und die drei eigenen Gespräche bleiben erhalten. Das Trio erscheint weiterhin ausschließlich als Kind. Die Treppe und der normale Weg bleiben frei.

## Flügel der vier Madagascar-Pinguine

Bei Skipper, Kowalski, Private und Rico waren zuvor auch Körper-/Hüftpunkte den bewegten Flügelgruppen zugeordnet. Ihre Credits-Modelle haben jetzt separate, starre Flügelteile. An den Ansätzen sind die beiden getrennten Oberflächen geschlossen. Kein Dreieck verbindet Punkte aus unterschiedlichen Bewegungsgruppen: dadurch kann die Flügelanimation keine Hüften mehr langziehen. Der kräftige Tanz bleibt erhalten. Insgesamt kommen bei den vier kleinen Modellen nur 52 Dreiecke hinzu. Ihre normalen Schloss-Auftritte werden nicht geändert.

Pingus Modell und seine gesamte Tanzanimation bleiben unverändert.

## Neue Credits-Gäste

- Moseby steht auf dem Gras der Insel im Hylia-See, vor dem Baum und möglichst frei von der Credits-Schrift. Er bewegt Kopf und Arme leicht. Der normale erwachsene Moseby am See bleibt erhalten.
- Original Starwalker steht im letzten Schwenk auf der Feier, nachdem Mido und König Zora die Lichter bemerkt haben, vor dem Schnitt zum Todesberg. Er wird nur während dieses Bildausschnitts gezeichnet (Frames 317–472).

Beide Gäste haben in den Credits keine Gespräche, Zielerfassung oder Kollision. Ihre Auftritte benutzen Raumdaten und benötigen keine weiteren Objektbank-Plätze. Die ursprünglichen Kamerafahrten, Schwenks, Laufzeiten und Schnitte bleiben unverändert.

## Bilder und Dialogliste

Die Bildersammlung enthält vier ausgewählte Starwalker-Auftritte aus Deku-Baum, Waldtempel, Wassertempel und Eishöhle sowie die neuen Credits-Gäste und das engere Trio. Die Dungeon-Bilder sind Emulator-Kontrollansichten mit freier Kamera und ausgeblendeter Link-Darstellung, damit Starwalker unverdeckt zu erkennen ist. Die Bilder der beiden Credits-Gäste verwenden die ursprüngliche Spielkamera. Die vergrößerten Pinguin-Kontrollansichten halten den Shot an und blenden die Beschriftung aus; das ist nur eine Emulator-Prüfung.

Die aktuelle Dialogliste von nach dem Feuertempel bis zum Ende des Wassertempels enthält 120 Text-IDs einschließlich Nebenhandlungen und Varianten. Sie wurde aus dem deutschen Spieltext gelesen, mit IDs und echten Textbox-Seiten. Ihr Textstand V52 gilt auch für V53: diese Ausgabe ändert keine Dialoge.

## Geprüft

Mit 4 MiB im Emulator: alle drei Trio-Gespräche, das Fehlen des Trios als Erwachsener, die ganze Folge der Ranch-Feierszenen bis zum Todesberg, beide neuen Credits-Gäste und ihre anschließende Entfernung sowie vier ausgewählte Dungeon-Auftritte von Starwalker. Modellgruppierung und geschlossene Flügelansätze werden außerdem an den konvertierten Geometriedaten geprüft. Die unveränderten Modellbanken, übrigen Räume, Sprachdateien und Cutscene-Skripte werden mit V52 verglichen. Beide Patches werden unabhängig erneut angewendet und gegen die gebauten ROMs geprüft.

Ein kompletter Spieldurchlauf wurde nicht durchgeführt. Alte Emulator-Savestates enthalten den früheren RAM-Zustand; für neue Platzierungen den Raum nach Laden der neuen ROM frisch betreten.

## Quellen bauen

Nach der vorhandenen Baufolge bis V52:

```
python3 tools/build_credits_refinement_v53.py /pfad/zu/oot
```

Danach normal mit `VERSION=pal-1.0 COMPARE=0` bauen. Für DEBUG zuletzt `build_debug_version.py` anwenden; `--restore` stellt die normalen Quellen wieder her. DEBUG bleibt wie bisher auf L+R halten, dann Z drücken. Die vorhandenen Optionen für alle Items, Standard-/Licht-/Schattengewand und Credits bleiben enthalten.

Die Modelldaten, der Konverter für die getrennten Flügel, native Testprogramme und Prüfprotokolle liegen im Quellenarchiv. Es werden keine ROMs mitgeliefert.
