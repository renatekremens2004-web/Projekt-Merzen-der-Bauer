# V62: Drei Goronen, genauere Ziele und eigene Aufnahmen

Die drei Soldaten der Kakariko-Szene verfolgen den Schatten nun mit deutlich genauer ausgerichteten Gewehren. Jeder hat einen eigenen nativen Sound aus den hochgeladenen WAV-Dateien:

| Rolle | Aufnahme | Neue Sound-ID |
| --- | --- | --- |
| Erster Gorone | Gorone 1.wav | 28F8 |
| Zweiter Gorone | Gorone 2.wav | 28F9 |
| Dritter Gorone | Gorone 3.wav | 28FA |

Die Aufnahmen werden beim Abfeuern ausgelöst. Eine eigene Wartezeit je Rolle läßt den jeweiligen Clip ausspielen, bevor er erneut beginnt. Die unterschiedlichen Längen bleiben erhalten. Das Video `Kakariko_Sounds_V62.mp4` enthält den tatsächlich im Emulator erzeugten Ton, einschließlich Regen und Musik; die WAVs wurden nicht nachträglich auf das Video gelegt.

## Zielverfolgung

Der Schatten bewegt sich über die Texturen zweier statischer Szenenmodelle; seine Actor-Position allein bildet diese Bewegung nicht ab. Die neue Zieltabelle berücksichtigt deshalb Modellgeometrie, Texturkoordinaten, Texturbewegung und Sichtbarkeit in den unveränderten Originalkameras. Die Soldaten verfolgen die sichtbare Schattenbahn zum Brunnen und später über die Eingangsfläche.

31 vorberechnete Haltungen decken -70 bis +80 Grad ab. Beide Arme, Ellbogen und Handgelenke folgen der Zielhöhe. Der seitliche Abstand der rechten Schulter zur Körpermitte wird beim Zielen ausgeglichen. Im Emulator gemessene Mündung und Laufachse stimmen mit den Schüssen überein: größte Zielabweichung 0,472 Grad bei 23 überprüften Schüssen. Die aufwendige Berechnung der Armhaltungen erfolgt beim Export; im Spiel werden Tabellen interpoliert.

Der bisherige Ablauf bleibt erhalten: zunächst unsichtbar, nach Sheiks Sturz von hinten ins Bild und zur Treppe laufen, am Brunnen feuern, zur Eingangsfläche verfolgen und dort weiterfeuern. Die erste Salve beginnt nun erst, wenn die Schattenbahn im Brunnen-Shot aktiv ist.

## Audio und Speicher

Die bearbeiteten Dateien sind Mono mit 16 kHz und werden im nativen N64-ADPCM-Format eingebunden. Die drei neuen codierten Samples benötigen zusammen ungefähr 43 KiB im ROM. Originale WAVs und die vorbereiteten Dateien sind im Quellenpaket enthalten. Überflüssige Stille am Ende wurde gekürzt; kurze Ausblendungen vermeiden Knackser.

Drei neue Einträge werden an die vorhandene Umgebungssound-Tabelle angehängt. Die permanente Soundfont 0 und ihre Samplebank erhalten drei zusätzliche Instrumente beziehungsweise Samples; vorhandene Einträge werden nicht umgewidmet. Die SFX-Sequenz bekommt drei zusätzliche Handler. Die Wartezeiten betragen je Rolle 26, 18 und 44 Spielbilder.

Es werden keine zusätzlichen Projektile als Actors angelegt. Der feste Grafikpool bleibt auf sechs gleichzeitige Leuchtspuren begrenzt. Die Spuren verursachen keinen Schaden.

## Prüfungen

- Normale und DEBUG-Ausgabe mit 4 MiB RAM: gesamte Sequenz, Sheik-Gespräch, Nocturne erfolgreich nachgespielt und Rückkehr ins steuerbare Dorf.
- Beide Durchläufe: 23 Schüsse, höchstens fünf gleichzeitig, alle drei neuen Sound-IDs im nativen Audioplayer aktiv; Links Gesundheit bleibt unverändert.
- Alle drei hochgeladenen Stimmen wurden zusätzlich durch Wellenformvergleich im aufgenommenen Spielton nachgewiesen.
- Die erste Objektbank bleibt bei 14 Slots mit 3.808 freien Bytes; der zweite Teil bei elf Slots mit 140.800 freien Bytes. Die neue Audioeinbindung hat beide nativen Durchläufe bestanden.
- Bisherige Modellbanken, Räume, Szenen, Texte und Sprachen bleiben gegenüber V61 erhalten. Andere Actor-Overlays wurden nach Berücksichtigung der Linker-Adressen verglichen. Hauptprogramm-Instruktionen und Registeroperanden bleiben gleich; geänderte Adressoperanden wurden geprüft.
- Sämtliche Musiksequenzen außer der erweiterten SFX-Sequenz 0, sämtliche Soundfonts außer Font 0 und sämtliche Samplebanken außer Bank 0 bleiben bytegleich. Die bisherigen Samples der Bank 0 bleiben erhalten.
- Beide BPS wurden mit einem unabhängigen Patcher auf die saubere Basis angewendet und bytegenau mit den getesteten Ausgaben verglichen. Kein vollständiger neuer Spieldurchlauf.

## Anwendung

Genau einen V62-BPS-Patch auf eine **saubere europäische PAL-1.0-ROM** anwenden. Basis-MD5: `e040de91a74b61e3201db0e2323f768a`. Alle bisherigen Änderungen sind enthalten. Die ROM neu starten; alte Emulator-Savestates enthalten weiterhin alten Code und RAM-Zustände.

Ein Spielstand, in dem die Nocturne-Sequenz bereits erledigt ist, löst sie beim Betreten Kakarikos nicht erneut aus. Die mitgelieferte MP4 zeigt den vollständigen Verteidigungsabschnitt mit echtem Spielton.

## Quellen

Auf dem kumulativen V61-Stand `python3 tools/build_defender_audio_v62.py /pfad/oot` ausführen, danach wie bisher mit `VERSION=pal-1.0 COMPARE=0` bauen und komprimieren. Für DEBUG anschließend `build_debug_version.py` verwenden und erneut bauen. Mit `--restore` die normalen Quellen wiederherstellen und erneut bauen.

Die fertigen Ziel- und Haltungstabellen sind enthalten. Nur beim Neuberechnen der Armhaltungen benötigt `export_defender_poses_v62.py` NumPy und SciPy. `export_shadow_target_v62.py` verwendet die originale Schattengeometrie und die beigefügten Kamera-Prüfdaten. Vollständige Symbol-Dumps werden aus Platzgründen weiterhin nicht mitgeliefert; sie lassen sich aus dem jeweiligen Build erzeugen. Keine ROM im Paket.
