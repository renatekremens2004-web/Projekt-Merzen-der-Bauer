# Wallace: lebhaftere Befreiung

Kumulativer Gesamtpatch für unveränderte Europa/PAL 1.0, Original-MD5 `e040de91a74b61e3201db0e2323f768a`. Ziel-SHA256 `85b2e36dea8fa9bd3fd33a4d012581c4ecfc5219fe4e0607dcebcba5b5a5e339`, weiterhin 40 MiB. Alle bisherigen Änderungen enthalten, insbesondere Wallaces Laufbewegung, der kleinere Weisen-Waluigi und die angepaßten Nahaufnahmen. Sämtliche Dialoge bleiben erhalten.

## Bewegung

Wallace gestikuliert mit Ober- und Unterarmen abwechselnd, nickt, neigt den Oberkörper leicht und wippt. Beim nativen Weggehen hebt er die Füße stärker an und federt mit. Zwei eigene Ellbogengruppen ergänzen die bisher zehn Gruppen. Bestehende Unterarmvertices werden nur neu zugeordnet; alle Positionen, Dreiecke, Normalen, UVs und Materialien bleiben unverändert. Weiterhin Höhe 90 und 2.269 Dreiecke. Unterarme erben die vollständige Schultertransformation, bevor sie sich am Ellbogen beugen. Keine Skalierung oder Scherung durch diese Pose.

Die Knie berücksichtigen das Wippen im Stand und die stärkere Bewegung beim Gehen. Die zweigliedrige inverse Kinematik hält den Standfuß am Boden und die Sohle waagerecht. Analytische Prüfung über 240 Gestenzeiten, 61 Fluchttimerwerte und beide Beine: erreichbare Fußziele ohne ideale Bodendurchdringung, maximale Rechenabweichung unter 1e-9 Modelleinheiten. Dies belegt die Sollgeometrie; tatsächliche N64-Matrizen verwenden die übliche begrenzte Genauigkeit.

Nur der Feuertempel-Gefangene erhält den Gestenparameter 1. Feuerweisenrolle, Finale und Credits verwenden 0: bisherige Posen und Schultersitz bleiben erhalten. Kind-Wallace unverändert.

## Ablauf und Speicher

Native Akteurssteuerung, Zelle, Bodenschalter, Weg, Geschwindigkeit, Zeiten, Kamera, Texte und Belohnung sind unverändert. Quellenvergleich: In EnGo2 und DemoDu ändert sich außerhalb der privaten Zeichnung ausschließlich das zusätzliche Aufrufargument. Laufzeitvergleich zum vorigen Patch: dieselben Zustandswechsel bei Frames 600, 1628, 1688 und 1689, gleiche Schalterbits und Akteurspositionen. Die Befreiung läuft über den echten Schalter und endet regulär.

Zwei zusätzliche 64-Byte-Matrizen pro Zeichnung, also 128 Bytes gegenüber der vorigen Laufkorrektur. Modellsegment und Feuertempelraum wachsen jeweils um 144 Bytes durch Matrix-/Vertexbefehle; die beiden Zeichenoverlays um jeweils 1.216 Bytes. Kein neuer Objekt-Slot, keine zusätzliche Geometrie, keine größere Akteursinstanz. Beide Szenen laufen mit tatsächlichen 4 MiB N64-RAM. Kein beobachteter Absturz, Objektpufferüberlauf oder ungültiger Grafikbefehl.

## Aufnahmen

| MP4 | Dauer | Bilder |
| --- | ---: | ---: |
| Wallace_Froehlich_Kurz.mp4 | 16,02 s | 267 |
| Wallace_Froehliche_Befreiung.mp4 | 69,00 s | 1150 |
| Wallace_Gesten_Weisen_Credits.mp4 | 38,82 s | 647 |

Echte fortlaufende Emulatorbilder aus demselben finalen Build: 640×480, H.264, PAL 50/3 Bilder/s, ohne Ton. Kurzclip ist ein zusammenhängender Ausschnitt aus den letzten 267 Bildern der vollständigen Befreiung. Vollclip enthält Gespräch und natives Weggehen. Credits zeigen erneut die gemeinsamen Weisen einschließlich Schultersitz und regulärem Szenenübergang. Lokale Ausgangsspielstände bereiten die Kapitel vor; anschließend Controller-Eingaben und native Spielsteuerung. Keine für die Aufnahme versetzten NPCs, umgeschalteten Fluchtzustände oder geänderten Kameras. Framefolge und MP4-Bildzahlen geprüft. PNGs verlustfrei aus denselben Quelldaten umgewandelt.

## Gesamtpatch

Alle 1.509 komprimierten Segmente und CIC-6105-Prüfsumme geprüft. Die drei Sprachsegmente sowie alle 1.013 eigenen Nachrichten bytegleich zur vorigen Fassung. Alle anderen Modelle und Kameras unverändert. Native Kern-/Questfunktionen trotz geänderter Linkadressen erhalten; vollständiger Bericht unter `validation/wallace-cheer/`. RomPatcher.js erzeugt mit eingeschalteter Quellprüfung aus Vanilla und BPS bytegenau die oben genannte Produktions-ROM.

Ein vollständiger normaler Durchlauf und echte N64-Hardware wurden in diesem Schritt nicht geprüft. Keine ROMs, Spielstände, Savestates, RAM-Abzüge oder ausführbaren Dateien veröffentlicht.

## Neubau

Am Ende der bestehenden Buildfolge `build_character_sizes.py`, dann `build_walk_followup.py`, dann **`build_wallace_cheer.py`** mit dem Decomp-Verzeichnis ausführen; anschließend normal bauen/komprimieren. Der letzte Schritt installiert die zwölfteilige Zeichnung und den zusätzlichen Gestenparameter. Vorbereitete Modelldaten und die unveränderten Sitzanimationen sind im Quellenpaket enthalten. `verify_wallace_cheer.py` benötigt die vorige Produktions-ROM mit Map/Modell-/Actorquellenschnappschüssen als lokale Vergleichsdaten. ROM-Vergleichsdaten werden nicht veröffentlicht.
