# Franky, Krater-Fundstück und Handhelds – V28

## Franky die Heugabel

Die drei hochgeladenen N64-Vorlagen werden verwendet: heil 145, kaputt 149, geklebt 171 Dreiecke. Alle Texturmaterialien bleiben erhalten. Die heile Variante ist 80 Spieleinheiten hoch, die geklebte etwa 79; das entspricht einer langen Heugabel neben erwachsenem Link. Leichtes Schwanken und Nicken, beim Reden etwas deutlicher. Seine Vorderseite wurde für die originale Blickrichtung angepaßt.

- Lon Lon Farm als Kind: bei den Ställen, (500, 0, -2200). Franky stellt sich ausdrücklich als „Franky die Heugabel“ vor und freut sich über den zu seinen Qualifikationen passenden Job. Tags und nachts enthalten.
- Lon Lon Farm als Erwachsener, derselbe Platz: Wiedersehen, unveränderter Lohn, gestiegene Lebenshaltungskosten, fehlende Krankenversicherung und Ankündigung seines Besuchs bei Merz. Tags und nachts enthalten. Jimmy bleibt erhalten; Franky steht außerhalb der Rennstrecke.
- Friedrichs normales Schloß: Eingangskorridor, (90, 240, 1480). Er begrüßt Link wieder und kündigt an, Merz in den Hintern zu pieksen. Die Flucht-Szenen enthalten ihn nicht.
- Finalarena: kaputte Originalvariante liegt bei (-930, 1086, -340) innerhalb des begehbaren Arenabereichs am Rand. Bei freier Steuerung regulär ansprechbar: Sein Plan war ein Schuß in den Ofen, seine Zeit sei gekommen, er bedankt sich. Auch während Boss-Kamerasequenzen bleibt er sichtbar; Gesprächsangebote sind währenddessen gesperrt. Keine Änderungen am Boss, dessen Lebenspunkten, Arena-Kollisionen oder Feuerring.
- Credits: geklebte Originalvariante bei (5, 0, -495), ausschließlich in der bestehenden vierten Farm-Einstellung (Szenenebene 9). Sichtbar im Vordergrund neben Pferd und Feiernden. Keine Kollision, keine Gesprächsangebote oder Story-Schreibzugriffe. Ursprüngliche Kameras, Musik, Texteinblendungen, Zeitmarken, Credits-Gäste und Szenenwechsel bleiben erhalten. Franky verschwindet beim Wechsel zur nächsten Einstellung.

Nachrichten 71E5 bis 71E8, manuelle Seitenwechsel. Die ausführliche Erwachsenen-Farmrede erstreckt sich über sechs Seiten. Keine automatischen Folgedialoge.

## Fundstück im Todesbergkrater

Das gelieferte PS1-Körpermodell liegt auf der oberen, ebenen Landefläche bei (-800, 1360, 1900), mit Abstand zur Kiste. Bestehende Vorlage mit 610 Dreiecken, zum Liegen gedreht; ungefähr 65 Spieleinheiten lang. Keine zusätzlich erzeugten Verletzungs- oder Blutmodelle. In beiden Zeitlinien bei normalem Spiel sichtbar. Alle Eckpunkte liegen über der vorhandenen ebenen Bodenfläche.

Mit Z anvisieren und C-oben:

> Hmm. Der hatte wohl keine magische Anti-Hitzerüstung... Ärgerlich... Wirklich ärgerlich...

## Game Boys im Kokiri-Tunnel

Im Tunnel zwischen Mido und dem Deku-Baum bei (1800, 0, 130), Raum 1: als Kind der gelieferte gelbe Game Boy Color, als Erwachsener der lila Game Boy Advance. Ein einziger Actor wählt Modell und Text nach Links Alter; beide Modelle stehen daher niemals gemeinsam dort. Tags und nachts enthalten, aus Film-Szenen ausgeschlossen. Keine neue Kollision oder Item-Aufnahme.

- Color: 40 Dreiecke, 7,5 Einheiten längste Seite. Navi: „Nanu, da hat jemand seinen Game Boy Color rumliegen lassen.“
- Advance: von 1612 auf 194 Dreiecke reduziert, 8 Einheiten breit. Navi entsprechend mit „Game Boy Advance“. Bildschirm, Bedienelemente und lila Gehäuse bleiben erkennbar.

Navi-Kommentare mit Z und C-oben, manuell schließen und erneut abrufbar. Nachrichten 71E9, 71EA und 71EB. Alle früheren Nachrichten sind bytegleich zu V27.

## Prüfung und Videos

Normal und DEBUG gebaut, N64-Prüfsummen geprüft. BPS auf saubere PAL-1.0-ROM angewendet und bytegleich mit dem jeweiligen Build verglichen. ROM-Segmente gegenüber V27 geprüft; außerhalb der Ergänzung nur erwartete Linker-Adressen. Alle ursprünglichen Raum-Actors erhalten. Keine neuen Objektbank-Slots oder DMA-Einträge. Raumlokale Modelladressen werden beim Zeichnen gesetzt und danach zurückgesetzt. Die neuen Nachrichten passen in die Textpuffer.

Gezielte Tests mit tatsächlich 4 MiB RAM: beide Farm-Zeitlinien, Schloß, kaputter Franky nach der Endkampf-Einleitung, Krater in beiden Zeitlinien sowie beide Handheld-Versionen. Alle Dialogseiten gelesen und geschlossen. Native Credits-Kamerafahrt mit Franky aufgenommen und Übergang in die nächste Einstellung geprüft; anschließend auch die weiteren Farm-Einstellungen bis zum nächsten Schauplatz durchlaufen. Triple Ts vorhandener Credits-Auftritt wurde zusätzlich mit 4 MiB ausgeführt und aufgenommen; seine Position und sein Modell bleiben unverändert. Keine Behauptung eines vollständigen Spieldurchlaufs.

Die MP4s zeigen tatsächliche Emulatorausgabe, ohne Ton. Frankys Video benutzt unveränderte Credits-Kameras und keine Controller-Eingabe. Für Barinade überspringt ein reiner Testaufbau den Kampf und aktiviert die vorhandene Todessequenz einschließlich Nebenarmen. Das ist keine zusätzliche Spieländerung. Der Clip zeigt die vollständige Sequenz bis zur Rückkehr zur normalen Steuerung; die bestehende rote Partikelfarbe aus V15 bleibt erhalten. Der Barinade-Code und seine Modelle sind gegenüber V27 unverändert.

## Anwendung und Quellen

Alle bisherigen Änderungen einschließlich V27 enthalten. Normal ODER DEBUG auf eine unveränderte europäische PAL-1.0-ROM anwenden (MD5 e040de91a74b61e3201db0e2323f768a). Nicht auf eine bereits gepatchte ROM. DEBUG-Menü: L+R halten und Z drücken.

Nach sämtlichen bisherigen Buildern zuletzt tools/build_franky_v28.py mit dem Decomp-Verzeichnis als Argument ausführen. JSON-Modelle und aufbereitete Texturen sind enthalten. Optionaler Export mit tools/export_franky_v28.py; der reduzierte GBA-OBJ ist im Quellenverzeichnis enthalten. Danach PAL-1.0 mit COMPARE=0 bauen, DEBUG optional separat. Normalquellen und Normalbuild sind abschließend wiederhergestellt.

Prüfskripte, Modellberichte, Laufzeitprotokolle und Video-Metadaten unter validation/franky-v28. Keine ROMs, Spielstände oder ausführbaren Testprogramme enthalten. Vorlagen stammen aus den hochgeladenen Dateien; daraus folgt keine zusätzliche Lizenz an den Vorlagen.
