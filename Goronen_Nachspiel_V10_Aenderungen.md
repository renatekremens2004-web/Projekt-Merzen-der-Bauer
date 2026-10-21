# Goronen-Nachspiel V10

21 deutsche Text-IDs nach den neuen Vorgaben geändert: Darunias Rückblick und Legende des Spielers, Ehren-Goronen-Ernennung, Verlust-Warnung beim Opal, seltener dritter-Stein-Zweig mit Sequence-Breaking-Spruch, Hinweis auf die Fee, Merz' Interesse an radioaktivem Material, Goronen auf dem Berg, die Video-Editor-Fee, Wirbelattacken-Nachsatz und die neuen Navi-/Salia-Texte. Gemeint sind in 3023 besiegte Dodongos; Transkriptionsvarianten Meers/Sora/Zalia als Merz/Zora/Salia normalisiert.

3027 (Kohlenstaub auf dem Teller), die Eule 3062/3063 und Darunias Tanz 3007 sind bytegleich zur Vorversion. In 3068 bleibt der bestehende Freunde-/Umarmungsabsatz erhalten. Der Schwimm-Spruch 3064 besteht nur noch aus dem einen gewünschten Satz.

## Navi und Salia

Die vorhandene deutsche Regel ersetzt die Grundhinweise 0148 und 0149 nach dem Opal durch 0135. Diese Logik wird nicht geändert. 0135 behält den bisherigen Höhlen-Rückblick, aber der einzelne Mund-im-Mund-Nachsatz ist gestrichen. Als letzte Seite folgt der neue Kommentar „Goronia abgehakt / Können wir jetzt aufhören?“. Dieser Wortlaut steht auch im Grundhinweis 0148. Der neue Salia-/Blutmagie-Spruch ist in 0149 gespeichert, wird in dieser Phase jedoch weiterhin übersteuert und nicht automatisch angehängt.

0162–0164 sind Antworten von Salia, wenn man sie über Salias Lied ruft. Es sind keine weiteren Navi-Texte. Alle Aufruf-/Fortschrittsbedingungen bleiben unverändert. Die vorhandenen Arbeitslisten erklären die tatsächlich angebotenen und die übersteuerten Zustände.

## Textabläufe und Prüfung

0081 behält die originale Item-Anzeige samt Icon. Der neue Verlust-Warnsatz folgt auf einer zusätzlichen manuellen Seite. 00DD behält die Wirbelattacken-Anleitung und erhält danach den gewünschten Nachsatz. Keine Verlängerung von festen Lese-/Einblendzeiten. 00DA und 00DB sind gemeinsam verwendete Große-Fee-Nachrichten; deren neue Texte gelten auch bei anderen entsprechenden Feen-Besuchen. Heilungs-EVENT und Dialogabschlüsse bleiben erhalten.

Alle funktionalen Textcodes, Fortsetzungen und Namensfelder erhalten. Andere Text-IDs und Sprachen bytegleich. Beide Builds mit gültigen N64-Prüfsummen; geänderte Rohtexte und dekodierte Seiten innerhalb der nativen Puffer. Sämtliche sonstigen Segmentänderungen gegenüber V9 gegen explizite Linker-Relokationen geprüft. Keine Änderung an Modellen, Kollision, Speicherpools, Kampf, Hinweislogik oder Questbedingungen.

Laufzeitproben der Opal-Szene mit tatsächlichen 4 MiB: normaler zweiter-Stein-Zweig 3000 und seltener dritter-Stein-Zweig 3001. Native Darunia-Szene, Item-Anzeige mit Zusatzseite, Feenhinweis und anschließende Goronen-Umarmung. Nur Anfangs-Spielstand, Fortschritt und Szeneneinstieg vorbereitet; keine NPCs, Textzustände oder Boßaktionen für die Bilder versetzt/erzwungen. Kein vollständiger Spieldurchlauf und keine eigene Laufzeitprobe sämtlicher Feen-/Salia-Varianten.

Beide BPS mit RomPatcher.js und aktiver Quellvalidierung angewandt und byteweise mit ihren Ziel-ROMs verglichen. Downloads nach Veröffentlichung separat geprüft.

## Anwendung und Quellen

Einen kumulativen Gesamtpatch auf die unveränderte Europe/PAL-1.0-ROM anwenden. Original-MD5 e040de91a74b61e3201db0e2323f768a. Deutsch wählen. Alle bisherigen Änderungen enthalten. Debugsteuerung unverändert (L+R halten, Z drücken).

Letzter normaler Builder: tools/build_goron_aftermath_v10.py nach build_goron_dialogue_v9.py und vor optional build_debug_version.py. Vorgaben in tools/goron_aftermath_v10.json; kanonische Kapiteltexte in story/*.json. Der kürzere Salia-Text 0164 behält sein natives EVENT; nur gewöhnliche manuelle Seiten zusammengefaßt. Die ausdrücklichen Nutzerregeln gegen nachgeschobene politische Vergleichspointen sind in story/LEITLINIEN.md enthalten. Quellenarchiv ohne ROM/Saves/ELF/ausführbare Programme.

Größter geänderter Rohtext: 354 von 1280 Bytes; größte dekodierte Seite (konservative Obergrenze): 143 von 200 Bytes.
