# Okto, der Oktorok – friedlicher NPC in Jabu-Jabu

Ein zusätzlicher Oktorok steht rechts im Eingangsraum von Jabu-Jabu, bei (140, Bodenhöhe, 240). Seine tatsächliche Bodenhöhe wird nativ ermittelt, im Test ungefähr -249,7. Er stellt sich als „Okto, der Oktorok“ vor. Mit Z anvisieren und A sprechen; das Gespräch ist wiederholbar. Vier normale, frei weiterklickbare Seiten über Vorurteile und den großen bösen Oktorok. Der Spieler muß nichts kaufen oder abgeben.

## Verhalten

- Ein einzelner neuer En_Okuta-Eintrag mit reserviertem Parameter 0x7F00 in Raum 0. Native Modelle, Skelett, ruhige Float-Animation und Szenenbeleuchtung. OBJECT_OKUTA war bereits geladen; kein zusätzliches Objektpaket und kein importiertes Modell.
- Dieses Exemplar wird beim Initialisieren in ACTORCAT_NPC umgehängt; keine Feindmarkierung, kein Navi-Gegnertext. Sein Update verwendet ausschließlich Animation, Blickrichtung, Sprechen und Körperkollision. Keine Angriffs-/Trefferkollision, Projektile, Schadens-, Todes- oder Versteckroutine.
- Normale Oktoroks und Projektile gehen unverändert durch ihre ursprünglichen Zweige. Der große Oktorok und seine Arena sind unverändert. Gegnerzahlen, Türen, Schalter und Belohnungen zählen Okto nicht als Feind.
- Eine eng begrenzte Ausnahme im nativen Actor_Spawn-Clear-Test läßt ausschließlich diesen deutschen NPC auch im bereits geräumten Raum zu. Andere Gegner behalten die ursprüngliche Raumfilterung. Kein Löschen oder Manipulieren von Clear-Flags.
- Der Zusatz-NPC ist auf Deutsch aktiv. In Englisch/Französisch entfällt dieser Zusatz; keine leere Platzhalterbox. Bestehende Gegner bleiben vorhanden.

## Prüfung

- Produktions-ROM SHA256 e09953490120959b4bd1ae215e64238c8d78fd47b71a47d898fb3a0be3d60fcd. Basis ist die veröffentlichte Eulen-/Tagesdialogfassung SHA256 81bfa6f9aa1c339c48012327c4dd02c19371acf44b0fe48bc6967eabd9e24858.
- 32 MiB, gültige CIC-6105-Prüfsumme; 1509 komprimierte Segmente gegen unkomprimierte Ausgabe geprüft.
- Genau ein deutscher Textplatz (00F8, vorher Platzhalter) geändert; Vorlage 0022, native normale Textsteuerung. Alle bisherigen 681 eigenen Nachrichten bytegleich erhalten, jetzt 682 insgesamt. Namen, Zähler, Auswahlfelder, Puffer und Textbreiten geprüft. Keine festen Lese-/Cutscene-Zeiten verändert.
- Änderungen: Raum 0 erhält genau einen zusätzlichen Actor-Eintrag; En_Okuta erhält den eigenen NPC-Zweig und die Skelett-Darstellungsfreigabe; Actor_Spawn genau die markierte Ausnahme. Entfernen dieser Einfügungen ergibt die jeweiligen nativen Quellen bytegleich. Das übrige kompilierte code-Segment wird an Symbolgrenzen verglichen; zusätzliche Veränderungen sind ausschließlich geprüfte Linker-Relokationen und Nullausrichtung außerhalb der absichtlich geänderten Actor_Spawn-Funktion.
- Normales OBJECT_OKUTA bytegleich; andere Figuren/Modelle, großer Oktorok, Nintendo 64, X-Wing und bisherige Kapitel erhalten. Normaler Start und schnelleres Texttempo unverändert.
- Vier gezielte native 4-MiB-Szenarien: Gespräch und Wiederholung mit anschließendem Schwertgebrauch in Oktos Nähe; Okto im bereits geräumten Eingangsraum ohne normale Gegner; normale Oktoroks erzeugen weiterhin Projektile; englische Fassung ohne Zusatz-NPC. Okto wird als Kategorie 4 mit AT=0/AC=0 protokolliert, reguläre Gegner bleiben separat vorhanden. Die Raum-Clear-Probe beginnt mit einem lokal vorbereiteten normalen Clear-Flag; NPCs werden nicht versetzt und Text-/Timerzustände nicht geschrieben.
- BPS mit RomPatcher.js auf die validierte Vanilla-ROM angewandt; Ergebnis bytegleich zur geprüften ROM.

Drei echte, unbearbeitete Aufnahmen mit Herkunft in previews/okto/Aufnahmen.json. Rohlogs und Prüfberichte in validation/okto. Kein vollständiger Durchlauf oder Hardwaretest. ROMs, Spielstände und Emulator-Binaries bleiben lokal.

## Nachbauen

Auf der bestehenden PAL-1.0-Rekonstruktion nach den bisherigen Modellgeneratoren `build_story.py OOT`, `build_habeck.py OOT`, `build_npc_stimmen.py OOT`, `build_text_speed.py OOT` und zuletzt `build_friendly_octorok.py OOT` ausführen. Die normalen PAL-1.0-Ziele bauen und komprimieren. `python tools/verify_friendly_octorok.py OOT VORFASSUNG.z64` benötigt die oben genannte Vorfassung und deren Linker-Map als baseline.map daneben (mitgeliefert: validation/okto/baseline.map.txt). Runtime-Skripte benötigen den lokalen Emulator und private Testspielstände.
