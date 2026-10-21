# Goronen- und Darunia-Dialoge V9

22 deutsche Text-IDs nach den neuen Vorgaben überarbeitet. Goronia leidet unter Merz' eingestürztem Kohleabbau; Dodongos und Dodongo-Filet werden ausdrücklich anders beurteilt als die neuen Echsenmenschen. Neue Donnerblumen-/Aufrüstungs-, Urlaub-, Schlaf- und Fackel-Sprüche. Darunia rechtfertigt sich ausführlich mit normalen Goronen-Fähigkeiten, weist Zeldas Wiegenlied zurück, tanzt unfreiwillig wegen der Blutmagie und bietet dem Spieler anschließend den Höhlenauftrag und das Armband an. Ein Gorone begrüßt den Spieler als Heiland. Navi kommentiert Donnerblumen, Lavagruben und Aufzug.

3009 bleibt bytegleich. Die bei 0119 abgebrochene Vorgabe „Sieh, genau“ wurde nicht ergänzt; diese ID bleibt ebenfalls bytegleich. Darunias nicht ausdrücklich nummerierte erste Rede gehört zu 301A. In 3018 bleibt der zuvor gewünschte Rockmusik-Spruch stehen; der Waldmusik-Hinweis wird durch Darunias Blutgruppe ersetzt. „Goldenes Blut“ ist dabei die erfundene Bezeichnung innerhalb Hyrules.

## Technik und Prüfung

3007 hat weiterhin neun Seiten mit den acht unveränderten automatischen Verzögerungen (30/40/30/40/30/40/40/40). Darunias erschrockene Ausrufe passen in die vorhandene Tanzszene. Die längere Schilderung, daß es wehgetan hat, folgt in der manuell weitergeschalteten 301C. Keine Verlängerung der Cutscene-Zeiten. Manuelle Texte sind nach den echten PAL-Fontbreiten auf höchstens vier Zeilen je Seite umbrochen.

Alle funktionalen Textcodes, Auswahlantworten und direkten Fortsetzungen bleiben erhalten. Alle anderen Text-IDs und Sprachen bleiben bytegleich. Normale und DEBUG-ROM gebaut, N64-Prüfsummen und Textpuffergrenzen geprüft. Vergleich mit V8: tatsächliche Änderung nur deutsche Textdaten und Textzeiger; andere veränderte Wörter gegen explizite Linker-Relokationen geprüft. Keine Änderung an Modellen, Animationen, Kollision, Kampflogik, Speicherpools oder Darunias Dialog-/Tanz-/Gegenstandsablauf.

Laufzeitproben mit tatsächlichen 4 MiB dokumentiert in validation/goron-dialogue-v9/runtime-verification.json. Kein vollständiger Kapitel- oder Spieldurchlauf. Beide BPS mit RomPatcher.js und aktiver Quellvalidierung angewandt und byteweise mit ihren Ziel-ROMs verglichen. Downloads nach Veröffentlichung separat geprüft.

## Anwendung und Quellen

Einen der kumulativen Gesamtpatches auf die unveränderte Europe/PAL-1.0-ROM anwenden. Original-MD5 e040de91a74b61e3201db0e2323f768a. Deutsch wählen. Alle bisherigen Änderungen sind enthalten. Die Debugfassung hat dieselben Inhalte und die bisherige Steuerung (L+R halten, Z drücken).

Letzter normaler Builder: tools/build_goron_dialogue_v9.py nach build_castle_dialogue_v8.py, vor optional build_debug_version.py. Neue Vorgaben in tools/goron_dialogue_v9.json; kanonische Texte in story/*.json. Quellenarchiv enthält den kumulativen Quellenstand und Prüfungen, keine ROM/Saves/ELF/ausführbaren Programme.

Größter geänderter Rohtext: 1043 von 1280 Bytes; größte dekodierte Seite (konservative Obergrenze): 146 von 200 Bytes.
