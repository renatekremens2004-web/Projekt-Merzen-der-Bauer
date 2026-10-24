# V61: Neue Inszenierung der Goronen-Verteidigung

Diese Fassung ersetzt den V60-Auftritt der drei Soldaten in Kakarikos Nocturne-Sequenz. Der Schwerpunkt liegt auf einem dramatischen Verteidigungsversuch mit Einlauf, Stellungnahme, angelegten Waffen und anschließender Verfolgung.

## Ablauf

1. Vor Sheiks Sturz sind die drei Goronen unsichtbar und geben keine Schüsse ab.
2. Nach seinem tatsächlichen Sturz stürmen sie zeitlich versetzt von hinten in die niedrige Kameraeinstellung. Die native Laufanimation bewegt ihre Beine; die Waffen werden dabei getragen.
3. Die Soldaten verteilen sich über den unteren, mittleren und oberen Treppenbereich. In der Totale mit Brunnen und Treppe feuern sie dem Schatten nach.
4. Danach laufen sie auf einem Weg durch das Dorf zur Eingangsfläche. In der Einstellung mit dem Baum nehmen sie erneut Stellung und schießen dem Schatten hinterher.
5. Die ursprünglichen Kameras, Sheiks Gespräch, das Lied und die Rückkehr ins Dorf laufen weiter.

Die volle Szene ist im Video `Kakariko_Inszenierung_V61.mp4` mit echtem Spielton zu sehen. Das Video enthält ausschließlich die ursprünglichen Spielkameras und läuft im PAL-Tempo von 50/3 Spielbildern pro Sekunde. Die Nahaufnahme zur zusätzlichen Haltungskontrolle wurde separat im Emulator mit einer Testkamera erstellt; diese Kamera ist nicht Bestandteil der Mod.

## Waffenhaltung

Die bisherigen Standard-Arme werden für diese drei Rollen ersetzt. Das Gewehr liegt an der rechten Schulter; beide Armketten einschließlich Ellbogen und Handgelenken bewegen sich entsprechend der Zielhöhe. Die Stützhand folgt dem Vorderschaft. Dafür sind 23 vorberechnete Haltungen für -30 bis +80 Grad enthalten, mit fließenden Übergängen. Die inverse Kinematik wird einmal beim Export berechnet, nicht im laufenden Spiel.

Jeder Schuß startet an der transformierten Mündung des sichtbaren Gewehrs. Seine Richtung wird aus zwei Punkten auf der tatsächlichen Laufachse berechnet. Die kurze Mündungsflamme, der Rückstoß und die warmen Leuchtspuren gehören zum selben Schuß. Die ursprüngliche Arwing-Lasergrafik dient weiterhin als kleine, separat verwendete Effektgrafik; ihre Textur wurde für die warme Einfärbung angepaßt.

## Prüfung und Grenzen

- Normale und DEBUG-Ausgabe mit 4 MiB RAM: vollständige Nocturne-Sequenz, Sheiks Dialog, erfolgreich nachgespieltes Lied und Rückkehr ins steuerbare Kakariko.
- Keine sichtbaren Verstärkungen vor dem Einlauf-Zeitpunkt. Die drei Rollen werden beim Wechsel zu Sheiks zweitem Szenenteil abgebaut.
- Die Schußspuren haben keine Trefferprüfung und verursachen keinen Schaden. Ein fester Pool begrenzt sie auf sechs gleichzeitig; keine zusätzlichen Projektil-Actors.
- Die tatsächlichen Gelenkwinkel, Waffenpositionen und Flugrichtungen werden aus dem Emulator ausgelesen und unabhängig nachgerechnet. Die Mündung muß innerhalb von 0,2 Spieleinheiten übereinstimmen, Lauf- und Flugrichtung einen Skalarproduktwert über 0,99999 erreichen und die Zielabweichung unter neun Grad bleiben. Die konkreten Meßwerte liegen im Prüfbericht.
- Alle Einstellungen wurden im Emulator angesehen, einschließlich Einlauf, Treppen-Totale und Eingangsfläche. Die zusätzlichen Prüfkameras ändern keine Produktions-Kamerafahrt.
- Die vorhandenen Modellbanken, Texte und Sprachen, Musik sowie sämtliche Szenen einschließlich Credits werden verglichen. Notwendige Linker-Adressverschiebungen werden ausdrücklich geprüft. Die normale Ausgabe wird gegen V60, die DEBUG-Ausgabe gegen den weiterhin gesicherten V59-Stand verglichen; in beiden Fällen ist ausschließlich die Verteidigungs-Erweiterung ausgenommen.
- Das unveränderte Objektbank-Budget der ersten Nocturne-Sequenz beträgt 14 Slots mit 3.808 freien Bytes; der zweite Teil bleibt bei elf Slots mit 140.800 freien Bytes.
- Beide BPS werden unabhängig auf die saubere Basis angewendet und bytegenau geprüft. Kein vollständiger neuer Spieldurchlauf.

## Anwendung

Genau einen V61-BPS-Patch auf eine **saubere europäische PAL-1.0-ROM** anwenden. Basis-MD5: `e040de91a74b61e3201db0e2323f768a`. Die neuen Patches enthalten alle bisherigen Änderungen. Alte Emulator-Savestates enthalten weiterhin den vorherigen RAM-/Codezustand; für diese Prüfung die neue ROM neu starten und einen regulären Spielstand verwenden.

Der normale Ereignis-Auslöser der Nocturne-Sequenz ist erhalten. Ein DEBUG-Spielstand, in dem die Sequenz bereits erledigt ist, löst sie beim Betreten Kakarikos nicht erneut aus.

## Quellen

Nach dem vollständigen V60-Stand `python3 tools/build_defenders_v61.py /pfad/oot` ausführen und wie bisher mit `VERSION=pal-1.0 COMPARE=0` bauen und komprimieren. `build_debug_version.py` bleibt der optionale letzte Schritt; mit `--restore` werden die normalen Quellen wiederhergestellt, anschließend erneut bauen.

Die erzeugte Haltungs-Tabelle ist enthalten. Nur zur erneuten Erzeugung wird `export_defender_poses_v61.py` mit NumPy und SciPy benötigt. Das kumulative Quellenpaket enthält die bisherigen Assets und Builder sowie die neuen Prüfberichte und Skripte; keine ROM. Vollständige historische Linker-/Symbol-Dumps bleiben wie im V60-Paket zugunsten der Dateigröße ausgelassen und können aus den jeweiligen Builds neu erzeugt werden.
