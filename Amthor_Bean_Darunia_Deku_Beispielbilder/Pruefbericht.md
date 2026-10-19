# Phantom Amthor, Bean, Darunia, Deku-Baum und Stadt-Dialogtausch

Alle bisherigen Kapitel und Modelle enthalten. 26 deutsche Nachrichten gegenüber dem veröffentlichten Weisen-/Masken-Patch geändert; insgesamt 962 eigene Nachrichten. Der Jabu-Dialog wird über die NPC-Auswahl getauscht, sein neunseitiger Wortlaut ist unverändert.

## Modelle und Bosssequenz

Variante 1 umgesetzt: Burns-Kopf vor der nativen Enthüllung, Smithers-Kopf darunter; originale Rüstung, Pferd, Skelett und Animationen bleiben erhalten. Köpfe gleichmäßig skaliert, 636 beziehungsweise 521 Dreiecke. object_gnd wächst von 77.824 auf 99.904 Bytes (+22.080); keine neue Actor-Instanz und keine Vergrößerung des En_fHG-Actors. Ein Padding-Byte steuert die neue deutsche EVENT-Begrüßung 209B, die über A fortgesetzt wird. Bereits vorhandene Zeitvorgaben und der Kampfablauf sind unverändert. Wiederholungsversuche verwenden den nativen verkürzten Einstieg.

Die eigenen CI4-Köpfe erhalten native Beleuchtung. Bei der Begrüßung wird die normale Raum-Lichteinstellung verwendet. Index 0 ist transparent; der ursprüngliche Todesmasken-Effekt löscht zusätzlich die eigenen Kopftexturen. Alle 256 Maskenindizes auf gültige Grenzen geprüft. Deutsche Boss-Einblendung ersetzt nur die mittlere 128×40-Platte; englische/französische Bilddaten und das Pferdeobjekt sind sonst bytegleich.

## Dialoge und Marktplatz

Navi nennt Amthor und rätselt über 15 oder 55. Bean erklärt in seiner bisherigen knappen englischen Stimme Ast, Sturz und Genickbruch. Darunia verteidigt seinen Posten mit Stärke, Steineessen, Rollen und Hitzebeständigkeit; einzelne Goronen kommentieren seine Rechtfertigungen. Bestehende Nutzerideen wie die Goronen-Umarmung bleiben erhalten.

Der Deku-Baum erklärt den Parasiten für erledigt und sich für unaufhaltsam. Sein letzter Satz vor dem ursprünglichen Tod lautet „Nichts kann diesen Tag ruinieren!“. Mido reagiert mit Kompost, „Deku-Baum“ und der siebenjährigen Kokiri-Geschichte. Merz-/Triforce-Warnung und Auftrag zu Zelda bleiben verständlich. Die native Mido-EVENT-Steuerung bleibt erhalten.

Nach Zeldas Flucht: Der blaue Mann mit Schnurrbart am Brunnen (EnHy Typ 10, nativ −85/0/204) erhält 7044; der Mann auf der hohen Plattform (Typ 12, nativ −343/160/241) erhält dessen kürzeren 7046-Text. Nur deutsche Markt-Tages-/Nachtvarianten; frühere Gespräche, andere Gebiete und Maskenreaktionen behalten Priorität und ursprüngliche Behandlung. Kein NPC versetzt.

## Statische und Patch-Prüfung

Finale ROM-SHA256 `2258268d6d19086683b429c9bf804309b364511c208d7126df307537d32988ef`. 32 MiB, CIC-6105 korrekt. Alle 1509 komprimierten Segmente gegen den unkomprimierten Neubau geprüft. Gegen veröffentlichten Stand `03fd8d7124b11ea661b9d2b506a2c61ca076ce2279029557edcceda69c55aaa6` sind alle anderen Modelle und Szenen unverändert; unvermeidbare Linker-Adressen streng über ELF-Relokationen geprüft. 195 erhaltene Phantom-Symbole einschließlich nativer Skelette, Animationen und Körperdaten geprüft. Alle 962 Textpuffer, Antwort-/EVENT-Steuerungen, Textketten und festen Zeiten geprüft. Englisch/französischer Text unverändert; nur die zuvor unbenutzte gemeinsame Kopfzeile von 209B erhält die untere Textboxposition.

RomPatcher.js validiert die unveränderte Original-ROM (MD5 e040de91a74b61e3201db0e2323f768a) und erzeugt bytegleich diese finale Fassung. BPS direkt auf die entpackte Original-ROM anwenden, nicht auf eine ältere Mod-Fassung.

## Emulatorproben und Grenzen

11 abgeschlossene gezielte Läufe in runtime-checks.json, jeweils mit tatsächlichem ROM-Hash, Text-IDs und Framegrenze. Mupen64Plus/GLideN64, tatsächliche 4 MiB. Vorbereitete Spielerstarts/Fortschritte, normale A-/C-Up-Eingaben, keine direkt gestarteten Textboxen und keine versetzten NPCs. Navis normal ausgelöster Zieltext ist zusätzlich als einzelne Beobachtung in runtime-observations.json dokumentiert; der damalige früh abgebrochene Controllerlauf wird nicht als vollständiger Kampf gewertet. Die gesonderte Todessequenz-Probe bereitet nach dem nativen Übergang zur Flugphase den nativen Todes-Einstieg vor und prüft dessen Animation und Kopftexturen; sie ist ausdrücklich kein gewonnener Durchlauf des Kampfes. Im Bossraum bleiben 119.568 Bytes des nativen Objektpuffers frei. Bilder sind unveränderte Emulator-PNGs; Aufnahmen.json nennt Aufnahme und Revision.

Einige bereits abgeschlossene Proben stammen von `a09b6738cdce1ca33aeae158145b21e7f95d6b2b9c53500a906ba93e71e7ecd0`. Der anschließende Deku-/Mido-Nachtrag ändert nach binärem Vergleich ausschließlich 1091, 1029, 102A und 1045 samt Textoffsets/ROM-Prüfsumme; alle anderen Texte, Modelle, Actor-Codes und Szenen sind bytegleich. Die spätere reine Transkriptkorrektur von „Wurm“ zu „Baum“ betrifft ausschließlich 1045; der Zwischenstand ist zusätzlich im Delta-Bericht ausgewiesen. Die abschließende Mido-Probe verwendet den finalen Hash. Verwarfene Auswahl-/Startproben werden nicht als bestandene Zielgespräche gezählt. Kein kompletter Spieldurchlauf oder N64-Hardwaretest.

## Neubau

README-Baureihenfolge verwenden; build_phantom_amthor.py immer nach Text-/Namensbau anwenden. Die vorbereiteten Kopf-JSONs und Texturen genügen; Blender ist nur für eine optionale neue Ableitung aus den hochgeladenen Modellen nötig. Original-ROM, Emulator-Spielstände, ausführbare Dateien und RAM-Abbilder sind nicht im Paket.
