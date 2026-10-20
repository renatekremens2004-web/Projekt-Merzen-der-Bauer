# Marty, Doc und DeLorean am jungen Schloß

Kumulativer Gesamtpatch für unveränderte Europa/PAL 1.0, Vanilla-MD5 `e040de91a74b61e3201db0e2323f768a`, Ziel-SHA256 `d83e8a5b717e5b597014d2ceede438e7cd890a37ecdddf8710e921b1e73b0b85`. ROM 40 MiB, tatsächliche 4 MiB RAM. Alle bisherigen Änderungen einschließlich Jabbas verbessertem Gesicht enthalten.

Die Gruppe steht auf der westlichen Grünfläche nach dem Kletterabschnitt, abseits von Tor und Wächterrouten. Marty −390/2340, Doc −500/2310, DeLorean −480/2150 (X/Z); Höhen werden aus der nativen Kollision ermittelt. Native Personen, Wege, Wachen und Skripte behalten ihre Positionen. Der Wagen folgt mit fester leichter Neigung der dortigen Wiese; seine unteren Radpunkte liegen rechnerisch etwa 1,0–1,2 Spieleinheiten über dem nativen Boden. Nur Kinder-Zeit und deutsche Fassung.

Marty 1.274 statt 7.761 Dreiecke, Doc 1.364 statt 7.349, DeLorean unverändert 190 ohne die mitgelieferte Bodenplatte. Zusammen 2.828. Gesichter, Augen und charakteristische Haare erhalten Vorrang vor Kleidung; eigene Gesichts-Ausschnitte statt gemeinsamen kleinen Hand-/Kopf-Texturen. Natürliche eigene Standproportionen: Marty 82,8, Doc 91,53, Wagen 60,42 hoch und 200 lang. Arme offline um eigene Schultern abgesenkt; vier starre eigene Gruppen pro Person, minimale Kopf-/Armgesten, aktive Sprecher nicken. Kein fremdes Skelett und keine Skalierung in der Animation. Die unbeweglichen Instanzen ermitteln den statischen Boden nur beim Laden; die unnötigen drei Raycasts pro laufendem Bild entfallen. Native Beleuchtung, Nebel und Tiefentest.

Beide NPCs starten denselben Dialog: 71B4 → 71B5 → 71B6 → 71B7, vier Sprecherteile auf sechs Seiten. Erster Sprecher immer Marty, Namen in der Textbox; native Gesprächskamera bleibt beim angesprochenen NPC. Die ersten drei privaten Texte verwenden den nativen EVENT-Abschluß und normale A-bestätigte Fortsetzung; der letzte schließt normal. Keine festen Zeiten, keine Geschichte-/Inventar-/Zeitreise-Schalter im neuen NPC-Code. Nach Abschluß wurde normale Bewegung per Controller geprüft. Der DeLorean ist ein geparktes Dekorationsobjekt mit einfacher zentraler OC-Körperkollision.

## Speicher, Grafik und bisherige Figuren

Alle drei teilen ein eigenes Objekt von 111.296 Byte und einen zusätzlichen Slot, maximal 14 von 19. Es wird nur in der normalen Objektliste des jungen Schloßgebiets angefordert. Freier Objektpuffer in den Prüfungen mindestens **27,680 Byte**, größte freie zusammenhängende Arena-Fläche mindestens **60,464 Byte**, null fehlgeschlagene native Belegungen. Der Raumpuffer wächst nur um 64 Byte für die Listen. Neue Objekt-ID 0x0193, DMA-Segment am Ende; bisherige IDs und DMA-Indizes bleiben erhalten. Andere Orte laden diesen Zusatz nicht. Händler-Platzhalter passen sich konsistent an OBJECT_ID_MAX 0x0194 an; 16 Änderungen geprüft.

Zusätzlich ausdrücklich mit gleichzeitig lebenden Talon/Malon und der neuen Gruppe geprüft. Der ursprüngliche Talon wurde mit dem Huhn geweckt, sein nativer Dialog und Weglaufablauf setzten die normalen Fortschrittsbits (0008 → 0018); danach verschwinden Talon/Malon wie vorgesehen. Malons normale Ei-Übergabe lieferte ITEM_WEIRD_EGG 0x21 und setzte ihr ursprüngliches Fortschrittsbit 0004. Der Test bei Malon stellt einen normalen Rückbesuch nach dem Eulengespräch dar. Im separaten frühen Gruppentest sind Talon, Malon und die Eule zugleich aktiv. Bisherige Personen werden nicht zur Speicherersparnis entfernt.

Alle vier nativen Grafik-Arenen zusätzlich geprüft: keine Überlappung der Kopf-/Endzeiger, Puffer-Magic 1234/5678 erhalten. Für undurchsichtige Geometrie mindestens **22,552 Byte** frei in diesen Proben. Die geteilten Speichergrenzen und Meldungen stehen in den Protokollen.

Serieller Vergleich mit derselben Kamera, Startdatei, lebenden ursprünglichen NPCs und 4 MiB im verwendeten Mupen64Plus/GLideN64-Emulator. Neue Gruppe vollständig sichtbar, keine parallele Emulatorinstanz, keine Screenshot-Speicherung während der Messung. Je 400 VI-Intervalle nach 100 Aufwärm-Frames:

| Fassung | VI/s | Spielframes/s | VI-Intervall P95 ms |
| --- | ---: | ---: | ---: |
| baseline | 25.68 | 25.68 | 46.95 |
| new | 24.17 | 24.17 | 47.60 |

Das sind Host-/Emulatormessungen und keine echten N64-Hardwarezeiten oder eine Garantie für einen vollständigen Durchlauf. Die Angaben zum Grafik-/Objektpuffer stammen getrennt aus den tatsächlichen nativen Datenstrukturen.

## Prüfung und Lieferung

Zehn abgeschlossene Szenenproben insgesamt: Ansprache Marty, Ansprache Doc, Nacht, Gruppenansicht, englische Abwesenheitskontrolle, Erwachsenen-Zeit, Yellow Guys Gespräch, früher Zustand mit allen ursprünglichen Personen, Malons Ei und Talons vollständiger Aufbruch. Die veröffentlichte Fassung mit der Bodenabfrage-Optimierung wurde bei Ansprache beider neuen NPCs, Malons Ei-Übergabe, Talons Aufbruch sowie im seriellen Gruppenvergleich erneut geprüft. Die zusätzlichen Alters-/Sprach-/Nacht-/Yellow-Guy-Kontrollen stammen vom vorherigen Build mit bytegleichen Modellen, Dialogen und Altersregeln; das Laufzeitmanifest nennt die jeweilige ROM-Prüfsumme. Vier Gesprächstests der neuen Gruppe durchlaufen alle vier IDs und geben danach wieder Steuerung frei. Yellow Guys bisherige fünf Seiten ebenfalls durchlaufen.

Alle 1.511 komprimierten Segmente gegen den unkomprimierten Build, CIC-6105-Prüfsumme, 3.664 native Kernfunktionen/Datensymbole und die Puffer sämtlicher 1.035 eigener Nachrichten geprüft. Alle bisherigen Texte aller PAL-Sprachen sowohl als Quelle als auch kompiliert unverändert. Vorherige Objektsegmente und Boßmodelle unverändert. Änderungen am Elf_Msg2-Quelltext auf vier private Helfer und drei frühe Verzweigungen begrenzt. Neue Nachrichten haben in allen Sprachen einen gültigen Folge-DMA-Zeiger. Vollständiger Story-Neubau und inkrementeller Aufbau erzeugen dieselbe Reihenfolge der privaten Nachrichten.

RomPatcher.js mit aktiver Quellvalidierung erzeugt bytegenau den getesteten Build. BPS auf die unveränderte entpackte Vanilla-PAL-1.0-ROM anwenden; normale Spielstände laden. Letzter Builder nach build_jabba.py ist build_bttf.py. Modell-Neuableitung mit Blender 4.3.2: export_bttf.py mit -- <Arbeitsordner> und den entpackten Nutzerarchiven unter input/marty, input/doc, input/delorean. Vorbereitete JSON/PNGs reichen für den normalen Bau. Keine ROM, Saves, Savestates, RAM-Abzüge, ausführbare Dateien oder dichte Importobjekte veröffentlicht. Kein vollständiger Durchlauf oder Hardwaretest in diesem Schritt.
