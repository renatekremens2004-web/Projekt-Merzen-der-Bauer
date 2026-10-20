# Prüfung: neuer Sahur, Comic im Wassertempel und Augen

Gesamtpatch für unveränderte Europa/PAL 1.0, Vanilla-MD5 `e040de91a74b61e3201db0e2323f768a`. Ziel-SHA256 `06d6ffb42399caf326d8d984abbc7d6d7ac6f5c1c9544d66ac9c734aa8a2350f`, weiterhin 40 MiB. Alle bisherigen Änderungen enthalten, einschließlich der 19 Brunnen-/Schattentempel-Texte und Wallaces lebhafterer Befreiung.

## Modelle und Auftritte

Tripple T verwendet die neue Shuffling-Vorlage: 35.818 auf 2.000 Dreiecke, 22 eigene Knochen, Höhe 60. Eigene Proportionen und gleichmäßige Skalierung; drei kleine CI4-Kacheln bewahren das Gesicht. Die Not-AI-Vorlage wurde ebenfalls untersucht; das große Roblox-Archiv war wegen der 32-MiB-Transfergrenze nicht zugänglich. Der vorhandene Tanz ist auf 108 eigene Rotationsposen einschließlich Übergang zum Schleifenanfang vorbereitet. Wurzel X/Z fest, keine Skalierung oder Scherung. Native Beleuchtung, Nebel und Tiefentest.

Im vollständigen nativen Ablauf bleibt seine Animation während der Cutscene auf der ruhigen Pose. Erst bei ruhendem Cutscene-Kontext und beendetem Auftauchen läuft die Tanzanimation. Protokolle zeigen wechselnde Animationsframes bei gleicher Akteursposition und Blickrichtung. Native Auftauchbewegung, Kameras, Cutscene-Daten, Medaillon-/Altersbedingungen und Dialoge bleiben erhalten. Der kurze Tanzclip zeigt ihn nach dem abgeschlossenen Waldkapitel ohne Eingaben und ohne Textbox; A bietet weiterhin das normale Gespräch an.

Fanboy: gleiche 1.463 Dreiecke, gleiche Größe 78, Originaltextur und unveränderter Waldtempel-Raum 3. Zusätzlich im Wassertempel-Raum 7 bei −3320/1060/−3970. Dieser feste Boden wird von keiner Wasserbox überdeckt. Chum Chum zusätzlich in Raum 19 bei 1730/780/180; die relevante höchste Wasseroberfläche liegt bei 765. Andere unabhängige Becken, etwa bei Schattenlink, sind für diese Positionen nicht maßgeblich. Räume 7/19 sind kein direkt verbundenes Raumpaar. Native Türen, Truhen, Gegner, Schalter und Wege bleiben erhalten. Normale OC-Körperkollision, keine Angriffs-/Trefferkollision oder Questflag-Änderung. Keine zusätzlichen Objekt-Slots.

Chums Augenkorrektur gilt in beiden Tempeln: 408 ursprüngliche Augen-/Pupillendreiecke erhalten, Pupillen etwa 0,205 Spieleinheiten vorgezogen, damit sie nicht in den vereinfachten Augapfelflächen verschwinden. Jetzt 1.573 statt 1.287 Dreiecke, weiterhin Höhe 49, gleiche Drehpunkte, Körperproportionen und Originalatlas. Die runden vollständigen Pupillen sind im Waldtempel und beim Wasserauftritt geprüft.

Flacher Thaddäus: 1.145 auf 972 Dreiecke, rund 15 Prozent weniger. Außenmaße ändern sich um weniger als eine Spieleinheit je Rand; Atlas und UV-Zuordnung bleiben erhalten. Weiterhin statisch ohne Physik oder Kollision, gleiche Stelle auf Morphas festem Randboden, gleicher Navi-Spruch. Lebendiger Thaddäus und sämtliche anderen Figuren/Weisen sind unverändert.

## Dialoge

5085 ersetzt ausschließlich die allgemeine Windmühlen-Bemerkung des bärtigen Mannes im erwachsenen Kakariko durch die Zigaretten-/Krabbelminen-Explosion. 7068/7069 sind bisher freie Platzhalter für die beiden Comic-Gespräche. 608D/608E gehören Wawario/Wawaluigi und bleiben erhalten. Insgesamt 1.026 eigene Nachrichten; alle anderen deutschen Texte, alle anderen Sprachen und alle Textbox-Kopf-/Positionseigenschaften bytegleich zur vorigen Veröffentlichung. Funktionale Steuerzeichen, Spielername, Fortsetzungen und feste Zeiten bleiben erhalten. Alle kompilierten Textpuffer und Schriftbreiten geprüft.

## MP4s und Laufzeit

| Video | Dauer | Frames |
| --- | ---: | ---: |
| Tripple_T_Tanz.mp4 | 24,00 s | 400 |
| Tripple_T_Auftauchen_und_Tanz.mp4 | 206,16 s | 3436 |
| Thaddaeus_Wassertempel_Animationen.mp4 | 88,38 s | 1473 |

Alle drei sind fortlaufende echte Emulatoraufnahmen desselben oben angegebenen Builds, 640×480 H.264, PAL 50/3 Bilder pro Sekunde, ohne Ton, tatsächliche 4 MiB N64-RAM. Der lange Sahur-Clip enthält auch die native Zwischensequenz zur Waldgeschichte. Thaddäus zeigt Begegnung, vollständiges Gespräch und anschließendes Hochschwimmen; native Aktionswechsel und beide Animationen protokolliert. Lokale Start-Spielstände bereiten die Kapitel vor; anschließend native Steuerung und normale Controller-Eingaben. Keine für die Vorschau versetzten NPCs, umgeschalteten Animationszustände oder geänderten Kameras. Video-Framezahl und fortlaufende Render-Erfassung geprüft; PNGs unveränderte native Screenshots.

Zusätzlich zehn abgeschlossene Proben: beide Comic-NPCs bei allen drei Wasserständen, Chums Augen im Waldtempel, der Kakariko-Spruch sowie das flache Modell nach Morpha und im regulären Kampf. In diesen Proben kein beobachteter Absturz, ungültiger Grafikbefehl oder Objektpufferüberlauf. Mindestens 90,864 Bytes Objektpuffer verbleiben in den Proben. Wassertempel-Raumpuffer unverändert 131.728 Bytes; Waldtempel 161.184. Die vollständige Auftauchsequenz prüft auch die nativen Szenenübergänge. Ein kompletter normaler Spieldurchlauf und echte Hardware sind damit nicht geprüft.

## Neubau / Nachweise

Alle 1.509 komprimierten Segmente gegen den unkomprimierten Neubau und CIC-6105-Prüfsumme geprüft. Sämtliche Objektsegmente außer object_dekujr bytegleich; Fanboys Waldtempelraum und Morphas Boß-Overlay ebenfalls bytegleich. Anderenorts nur geprüfte Linker-Adressen verändert. Im Sproß-Akteur ändern sich Initialskalierung und private Animationsauswahl; native Bewegung, Draw-Fallback, Kameras, Zerstörung und Zustandsfelder erhalten. Elf_Msg2 ändert nur die vier vorhandenen Superhelden-Helfer für die zusätzlichen Räume/Modelle/Textnummern; andere eigene NPCs und native Funktionen bleiben erhalten. RomPatcher.js mit Quellvalidierung erzeugt bytegenau die Produktions-ROM.

Nach den bisherigen Kapitel-/Modell-Buildern `build_sahur_shuffle.py <oot>` und `build_water_comic_heroes.py <oot>` ausführen, anschließend normal bauen/komprimieren. Vorbereitete JSONs und Texturen enthalten; Blender nur für neue Ableitungen nötig. `verify_sahur_comic.py` benötigt die vorige Produktions-ROM und lokale Vergleichsdaten, die ROM bleibt privat. Keine ROM, Saves, Savestates, RAM-Abzüge oder ausführbaren Dateien veröffentlicht. MP4s liegen getrennt vom Quellenarchiv.
