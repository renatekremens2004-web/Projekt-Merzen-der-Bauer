# V54: Train Chase bei der Flucht und beleuchteter Starwalker

Die hochgeladene „The Wrong Trousers – Train Chase“-MIDI von Julian Nott ersetzt die Musik bei der Flucht aus Friedrichs einstürzendem Schloss mit Zelda. Es ist eine native N64-Sequenz, keine eingespielte Audiodatei. Melodie, Tonartwechsel, Tempo von 111 BPM und die vollständige Passage von ungefähr 1:56 bleiben erhalten; danach wiederholt sich das Stück.

Für die Instrumentierung wurden die vielen gedoppelten Stimmen der MIDI zu einem Ensemble aus Bläsern, Streichern, hohen Holzbläsern, Bass, Trommeln und Pauken verdichtet. Die vorhandenen Spielinstrumente werden wiederverwendet. Es kommen keine neuen Samples oder Instrumentenbänke hinzu. Die Sequenz belegt 12.064 Byte innerhalb des vorhandenen 16.384-Byte-Sequenzpuffers. Maximal 16 gleichzeitig geschriebene Musikstimmen werden verwendet. Für Musik, Ausklänge und Spielgeräusche bleibt die bestehende Grenze von 24 Synthesestimmen unverändert. Zelda, Fluchttimer und das Starten/Weiterlaufen/Beenden der Musik verwenden die originale Spiellogik.

Starwalker reagiert in allen elf Dungeons und in seinem Credits-Auftritt auf die Beleuchtung der Umgebung. Geometrie, Textur, Größe und Knochen bleiben erhalten. In den Credits steht er weiter hinten am Rand der Feier, bei `(80, 0, -560)`, auf dem Ranchboden. Die ursprüngliche Kamerafahrt bleibt erhalten.

Die Plätze und Animationen der vier Madagascar-Pinguine und von Pingu wurden in V54 nicht verändert. Die Pinguin-Bilder aus V53 waren lediglich vergrößerte Kontrollansichten: freie Testkamera, kurz angehaltener Shot und ausgeblendete Beschriftung. Diese Kameraeinstellungen wurden nicht in die Spiel-Credits übernommen. Die in V53 korrigierte Trennung von Flügeln und Hüften bleibt enthalten.

Alle bisherigen Inhalte und Dialoge sind enthalten. Die Dialogliste nach dem Feuer- bis Ende des Wassertempels mit dem Dateinamen V52 bleibt aktuell, weil V53 und V54 diese Texte nicht ändern.

**Anwenden:** Genau einen der beiden BPS-Patches auf eine saubere europäische PAL-1.0-ROM anwenden. Nicht auf V53 oder eine andere bereits gepatchte ROM anwenden. Basis-MD5: `e040de91a74b61e3201db0e2323f768a`. Der normale Patch ist zum Spielen, DEBUG enthält weiterhin Ortswahl, alle Items, Credits-Start und Gewandoptionen. Ein vorhandener Spielstand kann weiterverwendet werden; für den neuen Stand die ROM neu starten und den normalen Spielstand laden, statt einen alten Emulator-Zustand fortzusetzen.

**Kontrollen:** Beide ROM-Ausgaben gebaut, Prüfsummen geprüft und BPS-Patches unabhängig zurückangewendet. Native Tests mit 4 MiB: Musik startet mit der echten Flucht-Zelda, vollständiger Musikdurchlauf mit Wiederholung, Weiterlaufen über einen echten Außen-/Innen-Szenenwechsel, DEBUG-Musikstart, vier beleuchtete Starwalker-Auftritte und sein Credits-Schwenk bis zum Übergang zum Todesberg. Andere Musiksequenzen, Instrumenten- und Samplebänke, bestehende Dialoge und Cutscene-Skripte wurden binär verglichen. Das ist kein vollständiger Durchspieltest der gesamten Schlossflucht.

Die MP4 enthält tatsächlich im Emulator erzeugte Musik und Spielgeräusche. Die Eingaben für die kurze Hörprobe werden automatisch gesteuert. Die Starwalker-Dungeonbilder verwenden eine freie Kontrollkamera; das Credits-Bild verwendet die originale Spielkamera.

**Quellen:** Nach V53 `python3 tools/build_train_chase_v54.py /pfad/zur/oot-decomp` ausführen, anschließend normal bauen. DEBUG bleibt ein optionaler letzter Schritt. Die MIDI, das Arrangement, der erzeugte Sequenztext und die Konvertierungsskripte liegen unter `audio/train-chase-v54` beziehungsweise `validation/train-chase-v54`. Die fertige Sequenz lässt sich ohne erneute MIDI-Konvertierung bauen. Nur die erneute Konvertierung benötigt Python `mido`.
