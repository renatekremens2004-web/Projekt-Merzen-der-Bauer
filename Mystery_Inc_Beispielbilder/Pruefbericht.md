# Mystery Inc. im Brunnen und sichtbarer Kenny

Kumulativer Gesamtpatch auf unveränderte Europa/PAL 1.0. Vanilla-MD5 `e040de91a74b61e3201db0e2323f768a`, Ziel-SHA256 `47d586454330c90ff54b155a32fb87b00085edbee1d0a0e0d35f0e7064ea5754`. Alle bisherigen Änderungen einschließlich Naboo-Starfighter und bedingter Mystery Machine enthalten. BPS mit RomPatcher.js anwenden, normale Spielstände statt alter Emulator-Savestates laden. Deutsche Sprachfassung.

## Figuren und Standorte

Die fünf vom Nutzer gelieferten N64-Modelle aus Scooby-Doo: Classic Creep Capers bleiben in originaler Dreieckanzahl und ihren natürlichen Proportionen erhalten. Shaggy 414, Velma 342, Daphne 340, Scooby 358, Fred 349; zusammen 1.803 Dreiecke. Die bereits entspannten Originalposen bleiben erhalten. Kopf und Arme bewegen sich leicht, Scooby bewegt Kopf und Schwanz; vier eigene starre Transformationsgruppen, ausschließlich kleine Rotationen ohne Skalierungsanimation oder fremdes Skelett. Beim Sprechen wenden sich die Figuren sanft Link zu und gestikulieren etwas stärker. Kein Laufen vorgesehen. Native Beleuchtung, Nebel, Tiefentest und kleine Bodenschatten.

Jede Figur steht in einem anderen Raum. Shaggy im blutigen Nordgang von Raum 0, abseits des Einstiegskriechgangs; Velma im Keller Raum 1; Daphne am freien Ostrand des Sargraums 2; Fred auf dem festen vorderen Rand des Fallengrubenraums 5; Scooby am vorderen rechten Rand von Raum 6. Positionen und gleichmäßige Größen stehen in validation/mystery-inc/placements.json. Figuren nur als Kind in deutscher Sprache aktiv. Jeder Auftritt hat eine eigene nur im jeweiligen Raum geladene Objektdatei; beim Übergang können die beiden beteiligten Raumobjekte gleichzeitig geladen sein. Die ganze Gang wird nicht gemeinsam vorgehalten. Kollisionszylinder 12 Einheiten Radius, kein Kampf, keine Quest-Funktionen oder Besitzbedingungen.

Kenny liegt weiterhin nach Erhalt der Gleitstiefel im Sensen-/Silberrubinraum 6 des Schattentempels, jetzt gut sichtbar auf der Eingangsseite bei **2990/−542/−1020**, um 90 Grad gedreht. Tatsächlicher Boden −543, Körperbasis +1. Kein neuer Objekt-Slot im Schattentempel. Besitzbedingung, tote/lebende Variante und Navi-Kommentare bleiben unverändert. Die Sensenbahn, Rubine, Truhen, Türen, Raumverbindungen und ursprünglichen Gegner bleiben bestehen.

## Mystery Machine

Das gelieferte N64-Fahrzeug behält seine 456 Dreiecke und Texturen. Natürliche Proportionen: 150 Spieleinheiten lang, 64,1 breit, 95,66 hoch. Geparkt bei −2300/138/1130, parallel zum Zugang auf dem ebenen Randstreifen. Die vier Radpositionen liegen auf nativem Boden bei Y=138. Wario, Wache und der Durchgang bleiben frei. Reines statisches Dekoobjekt ohne Ansprache, Körper-/Gegnerkollision oder zusätzliche Objekt-ID. Daten im vorhandenen Kakariko-Raumsegment; der größere Raumpuffer wird mit 4 MiB geprüft.

Nur die beiden Kind-Actorlisten (Tag/Nacht) enthalten den Wagen. Zusätzlich fordert die Instanz LINK_IS_CHILD und QUEST_SONG_STORMS. Diesen dauerhaften Liedbesitz setzt Guru-Guru beim erfolgreichen Erlernen der Hymne des Sturms als Erwachsener. Das vorübergehende Windmühlenmerkmal EVENTCHKINF_65 wird nicht verwendet, da es beim Betreten von Kakariko zurückgesetzt wird. Keine neue Quest-/Zeitreisefunktion. Beim ersten Besuch unsichtbar, nach dem Lernen und Zurückreisen als Kind tags wie nachts sichtbar, als Erwachsener unsichtbar.

## Dialoge

Neue private IDs 71BA–71BE, normales Ansprechen und manueller A-Seitenwechsel, keine festen Lesezeiten. Alle bisherigen Dialoge in allen drei PAL-Sprachen als Quelle und kompiliert bytegleich.

**71BA**

ZOINKS! Hier ist echt ne Menge Blut. Ich hatte gehofft, das ist KETCHUP!

Da vergeht einem echt der Appetit... Wobei, was rede ich denn DA!

Ein leckeres Sandwich wäre jetzt doch genau das Richtige. Hmm!

**71BB**

JINKIES! Der Gestank hier unten ist unbeschreiblich ekelig. Es riecht nach Schwefel und Eisen.

Ob es wirklich so gut war, daß wir uns aufteilen? Ich hoffe, die anderen sind vorsichtig...

**71BC**

JEEPERS! Hier unten sollte echt mal geputzt werden. Und das ist definitiv kein Platz für Kinder wie Dich!

Wo ist überhaupt Fred? Wobei, Velma dürfte mich natürlich auch gerne begleiten...

Mit ihr würde ich mich hier gleich viel wohler fühlen. Und das liegt nicht nur an ihrer Taschenlampe.

**71BD**

Ruh-roh! Rer Brunnen ist riel zu gruselig! Wo ist Raggy?

Für einen Scooby-Snack würde ich ja bleiben... Zwei? Rein, lieber drei!

Scooby-Dooby-Doo! Aber jetzt bitte raus hier!

**71BE**

FUCK! Hier unten gibt es echt eine Menge Fallen, und ich Idiot habe natürlich mein Notizbuch vergessen!

Wie schade. Blöder, blöder Fred! Was bin ich nur für ein Hornochse!

Eine Falle MIT einer Falle zu fangen, wäre so schön gewesen. Aber ohne Notizbuch? Das wäre unprofessionell.

## Prüfungen

Dreizehn gezielte Emulatorproben mit echten 4 MiB: alle fünf Auftritte mit natürlicher Ansprache bis zur letzten Textseite, Kenny am neuen Standort samt Navi-Kommentar, speicherkritischster Schattentempelraum 9 und Abwesenheit der Gang als Erwachsener; zusätzlich fünf Bedingungen der Mystery Machine (Kind vorher tags/nachts, Kind nachher tags/nachts, Erwachsener nachher). Für die Zustandsproben wird nur der normale Liedbesitz im Testspielstand gesetzt; die native Lied-Lernfunktion bleibt unverändert. Keine fehlgeschlagenen Speicherbelegungen, Grafikpufferüberläufe oder beschädigten GfxPool-Marken. Mindestreserve: größte freie zusammenhängende Arena-Fläche 54,592 Byte; Objektpuffer 50,064 Byte. Statischer Audit sämtlicher Brunnen- und Schattentempel-Raumlisten für beide Link-Alter, einschließlich Keep-/Link-Modellen und maximal 19 Slots. Der größte Objektbedarf bleibt Schattentempelraum 9 mit 969.840 von 1.019.904 Byte; der native Allokator bleibt unverändert. Brunnenraum 0 verwendet alle 19 Slots, überschreitet sie aber nicht. Keine neuen Modelle in Raum 4/Dead-Hand-Kampf. Kein vollständiger Durchlauf oder echter Hardwaretest.

1.517 komprimierte Segmente gegen den unkomprimierten Build und CIC-6105-Prüfsumme geprüft; 3.664 Kernsymbole unverändert bzw. ausschließlich echte Linker-Relokationen. Bestehende ElfMsg2-Sonderfunktionen unverändert, vier neue Gang-Funktionen, fünf auf Kakariko begrenzte Wagen-Helfer plus deren streng eingegrenzte Init/Update/Destroy-Verzweigungen. Fünf neue Objekt-IDs am Ende der Tabelle, keine Verschiebung bestehender IDs. Bestehende Gegner- und Spielerphysik unverändert. Alle 1.042 eigenen Texte passen in die nativen Textpuffer, die Folge-DMA-Zeiger aller neuen Texte sind für alle PAL-Sprachen gültig. BPS mit RomPatcher.js und aktiver Quellvalidierung angewandt: bytegleich zur geprüften ROM.

**Baufolge:** `tools/build_mystery_machine.py` als letzten Builder nach `build_mystery_inc.py`. Beispiel für die Gang: `python3 tools/build_mystery_inc.py /pfad/zur/oot-decomp` nach `build_naboo.py` (dieser nach `build_kenny.py`). Anschließend regulärer PAL-1.0-Bau und Kompression. Vorbereitete JSONs unter tools und Texturen unter models reichen für den normalen Bau. Optionaler Original-OBJ-Export: `python3 tools/export_mystery_inc.py WORK`, Nutzerarchive unter WORK/input/shaggy, velma, daphne, scooby, fred entpacken. Ausgangsdateien für die Builder unter tools/originals/mystery-inc im Paket enthalten. Der zusätzliche Wagen-Builder benötigt außerdem tools/originals/mystery-machine, ebenfalls enthalten. Quellenpaket enthält keine ROMs, Saves, Savestates, RAM-Abzüge oder ausführbare Programme. Bilder sind unveränderte Emulatoraufnahmen der geprüften Ziel-ROM.
