# Doofenshmirtz, Shrek und Mr. Monopoly

Kumulativer Gesamtpatch für die unveränderte Europa/PAL-1.0-ROM. Original-MD5 `e040de91a74b61e3201db0e2323f768a`, Ziel-SHA256 `89b941e2ca53f5d06d18987a53c82d2b369b26d120a35672a4f19e4bddde1ad9`. Alle bisherigen Figuren, Räume und Dialoge enthalten. Deutsche Sprache wählen und BPS mit RomPatcher.js anwenden.

## Eingebaut

Der native Angelteich-Betreiber wird in der deutschen Kindheitszeit durch den normalen Dr. Heinz Doofenshmirtz ersetzt. Er erzählt von seiner Kindheit, dem Angelverbot, den Jauchegruben und dem Angelinator. Als Erwachsener begegnet man seiner ernsteren Augenklappen-Version mit düsteren Texten über Merz’ soziale und ökologische Politik. Zusammenhängende eigene Dialoge; Herkunft und Figurenstimme wurden anhand der in story/DOOFENSHMIRTZ_NOTIZEN.md verlinkten Quellen recherchiert. Keine vorgeblichen Serien-Zitate.

Auf ausdrücklichen Nutzerwunsch trägt Doofenshmirtz keine Angelmütze. Sein deutscher Haarzustand schaltet zugleich den alten Mützenklau ab, damit kein unsichtbares Zubehör am Haken landet. Bestehende Rekord-/Mützenbits in Spielständen werden nicht gelöscht. Englisch und Französisch behalten das native Anglermodell und das ursprüngliche Mützensystem.

Das eigentliche Angelspiel läuft weiterhin über denselben Fishing-Akteur: 20 Rubine, Fischbestand, Steuerung, Wiegen, Rekorde, Herzteil und goldene Schuppe behalten ihre ursprünglichen Regeln. Keine globale Minispiel-Umschreibung. Das altersabhängige Modell wird jeweils über den nativen Raumheader geladen; die andere Doof-Version liegt nicht zusätzlich im Objektpuffer.

Shrek steht als ansprechbarer NPC ausschließlich in der Kindheitszeit am trockenen Ufer in Raum 3 der Verlorenen Wälder. Er beschwert sich über Merz’ Pläne für seinen Wald. Mr. Monopoly steht als ansprechbarer NPC seitlich der Haupthalle in Merz’ letztem Schloß, ausschließlich als Erwachsener. Er verteidigt Kapitalismus und erklärt, weshalb die menschliche Gier auch einen besiegten Herrscher überlebt. Beide stehen außerhalb der Wege und Türen. Kleine Kopf- und Handbewegungen, entspannte Arme, eigene unverzerrte Proportionen und native Beleuchtung.

29 bestehende deutsche Nachrichten überarbeitet und 21 private Textplätze ergänzt; insgesamt 1.154 eigene Nachrichten. Die reservierten Mützenzeilen 4087/4097/40B2/71D0 sind in der deutschen Fassung nicht mehr regulär erreichbar. Feste Original-Lesezeiten, Antwortreihenfolgen, Ereignisse und dynamische Fischgewichte erhalten. [Aktive Dialoge](../Dialoge_Doof_Shrek_Monopoly.md).

## Modelle und Speicher

| Modell | Dreiecke | Höhe in Spieleinheiten | Objektbytes |
| --- | ---: | ---: | ---: |
| Doofenshmirtz | 374 | 78 | 23.600 |
| Augenklappen-Doof | 564 | 82 | 35.296 |
| Shrek | 442 | 86 | 15.584 |
| Mr. Monopoly | 900 | 64 | 29.248 |

Monopoly wurde von 1.415 auf 900 Dreiecke reduziert. Seine 400 oberen Kopf-/Gesichtsdreiecke bleiben unverändert, der Körper wurde vereinfacht. Ungültige Normalen und 36 UV-Ecken des gelieferten Augenklappen-Modells wurden repariert; die fehlende lambert1-Textur durch die Materialfarbe ersetzt. Alle Texturen höchstens 64×64 in CI4. Vier einfache starre Animationsgruppen je Figur, keine zusätzlichen globalen Animationspuffer.

Der native Objektpuffer bleibt 1.019.904 Byte groß. Berechnete Raumbelegung einschließlich Link und Grundobjekten: Kind-Angelteich 709.680 Byte / 6 Plätze; Erwachsenen-Angelteich 764.512 / 6; Shrek-Raum 799.200 / 15; Schloßhalle 831.680 / 9. Kein vergrößerter Speicherpool, kein vorausgesetztes Expansion Pak.

## Geprüft

PAL-Build und Kompression erfolgreich. 1.524 komprimierte Segmente, CIC-6105-Prüfsumme und 3.664 native Kernsymbole differential geprüft. Alle bisherigen Nachrichten außerhalb der 29 freigegebenen deutschen Änderungen bytegleich; neue private Tabellenplätze in allen drei Sprachen geprüft. Alle 1.154 eigenen Texte passen in die nativen Rohtext- und Zeilenpuffer, einschließlich langer Spielernamen und Fischgewicht. Bestehende Gäste-/Stiefelfunktionen erhalten. Native Raumgeometrie und alle übrigen Raumobjekte unverändert oder ausschließlich durch echte Linker-Relokationen verschoben.

Sieben gezielte Proben der finalen Ziel-ROM mit echten 4 MiB: Doofenshmirtz als Kind und Erwachsener jeweils vom Gespräch über die Abbuchung von 20 Rubinen und den nativen Angelstart bis zum normalen Aufhören; Shreks gesamtes Gespräch; Monopolys gesamtes Gespräch; Shrek als Erwachsener abwesend; Monopoly als Kind abwesend; richtige Augenklappen-Version auch nachts. Die Kindprobe wirft die Leine aus und holt sie ein. Es wurde dabei kein Fisch gefangen und keine Rekordbelohnung erspielt; deren Erhalt wird durch den Vergleich des unveränderten Spielcodes belegt. Keine fehlgeschlagenen Speicherbelegungen, Grafikpufferüberläufe oder beschädigten GfxPool-Marken. Kleinste gemessene zusammenhängende Arena-Reserve 158,320 Byte, kleinste Objektpufferreserve 101,952 Byte. Kein vollständiger Spieldurchlauf oder Hardwaretest.

Die Bilder stammen ausschließlich von der finalen Ziel-ROM und sind unveränderte Emulatorbilder. Produktions-NPCs und native Kameras wurden für die Bilder nicht versetzt. Eine seitliche Testansicht des Angelteichs zeigte schon im vorherigen Patch mit dem ursprünglichen Angler dieselbe schwarze Dreiecksfläche; die dünnen Linien an der Wand sind aufgehängte Angeln. Die verwendete normale Anspracheposition zeigt die saubere Ansicht. Das ist keine Aussage, daß sämtliche früher besprochenen schwarzen Flächen im gesamten Spiel untersucht oder behoben seien.

BPS mit RomPatcher.js und aktiver Quellvalidierung auf die Vanilla-ROM angewandt: Ergebnis bytegleich zur geprüften finalen ROM.

## Reproduzieren

Nach den bisherigen Modell-/Raum-Buildern zuletzt `build_desert_guests.py`, `build_gerudo_dialogue.py`, `build_twinrova_title.py`, dann `build_doof_guests.py` ausführen. Anschließend normaler PAL-1.0-Build und Kompression. Der optionale Modell-Reexport erfolgt über `blender -b --python tools/export_doof_guests.py -- ARBEITSVERZEICHNIS` mit den entpackten Quelldateien unter dessen input-Verzeichnis. Die fertigen Modell-JSONs und Texturen sind im Quellenpaket enthalten, deshalb benötigt der normale Build keinen erneuten Blender-Import.

Quellenpaket ohne ROM, Save, Savestate, ELF, RAM-Abzug oder ausführbare Dateien. Prüfproben verwenden eigene Testspielstände und direkte Raumeinstiege; sie ersetzen keinen normalen Durchlauf.
