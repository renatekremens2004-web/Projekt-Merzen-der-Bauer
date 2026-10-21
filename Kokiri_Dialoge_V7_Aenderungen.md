# Kokiri-Dialoge V7

29 deutsche Text-IDs nach den neuen Vorgaben überarbeitet: Navi weckt den Spieler; Salias Begrüßung und Abschied; Midos Schild-/Schwert-Tirade und Reaktion auf den toten Baum; Deku-Baum-Auftrag, Fluch, Schöpfungs-Erzählung und optimistischer letzter Auftritt; Deku-Brüder und örtliche Navi-Kommentare.

Die ausdrücklich beibehaltenen ursprünglichen Seiten wurden bytegleich übernommen. Längere neue manuelle Seiten werden nach den echten PAL-Zeichenbreiten auf höchstens vier Zeilen umbrochen; dadurch können nachfolgende Seitennummern abweichen. Alle Spieler-Namensfelder bleiben dynamisch. Ja/Nein, TEXTID-Fortsetzungen, EVENT und die bestehenden Lautfolgen sind erhalten; bei den kürzeren Deku-Brüder-Monologen werden die Laute auf die neuen Seiten verteilt. Alte Rechtschreibung und Du/Dir/Dich-Anrede.

Die nicht vollständig genannte ID für „Wenn Merz dieses Triforce erhält“ wurde 1029 zugeordnet. „Du begegnest ein einziges Mal dem Deku-Baum“ ersetzt Midos ursprüngliche achte Seite in 1045. Die beiden Schöpfungsfilm-Einblendungen 108A/108B bleiben bei FADE(90); dort stehen kurze Fassungen. Die ausführliche Göttinnen-/Nietzsche-/Triforce-Bemerkung folgt in der manuell weitergeschalteten 1029. Keine Verlängerung der Einblend- oder Cutscene-Zeiten.

Salias Brückenabschied verteilt sich auf die vorhandenen Schritte: 1094 Waldgrenze, 1013 Okarina-Übergabe mit Holz/Magie/Wetter und 1014 Abschied mit dem Wegwerf-Gag. Die tatsächliche Gegenstandsübergabe bleibt an ihrer nativen Stelle. Midos 10D3 „noch lange kein Mido“ ist bytegleich erhalten.

## Prüfung

Normale und DEBUG-ROM erfolgreich gebaut, N64-Prüfsummen gültig. Alle bearbeiteten Nachrichten und Seiten unter den nativen Roh-/Seitenpuffergrenzen, Auswahlreihenfolge und funktionale Textcodes erhalten. Alle anderen Text-IDs und Sprachen sind bytegleich zur vorherigen Fassung.

Vergleich der dekomprimierten Spielsegmente mit V6: eigentliche Änderungen nur deutsche Nachrichtendaten und deren Zeigertabelle. Durch das Wachstum ändern sich nachfolgende ROM-Adressen; sämtliche sonstigen geänderten Wörter gegen explizite Linker-Relokationen der vorherigen ELF geprüft. Modelle, Animationen, Kollisionen, Dialogzustandsmaschinen und Boßlogik erhalten.

Zwei Laufzeitproben mit tatsächlichen 4 MiB: Mido prüft die Ausrüstung, zeigt alle fünf neuen Seiten 10D2, setzt mit 10D3 fort und geht aus dem Weg. Nach Gohma zeigt er alle acht Seiten 1045 mit der neuen letzten Seite und schließt die Begegnung normal ab. Für den Einstieg nur Spielstand-/Fortschrittsdaten und die anfängliche Spielerposition vorbereitet; keine NPCs versetzt, keine Nachrichten-, Timer- oder Schauspielerzustände erzwungen. Ausgewählte Textboxen visuell kontrolliert. Kein vollständiger Durchlauf des Kapitels oder gesamten Spiels.

Beide BPS mit RomPatcher.js und aktiver Quellprüfung angewandt; Ergebnis jeweils bytegleich mit der gebauten Ziel-ROM. Download-Dateien nach Veröffentlichung separat geprüft.

## Anwendung

Je einen kumulativen Gesamtpatch auf die UNVERÄNDERTE Europe/PAL-1.0-ROM anwenden. Original-MD5 e040de91a74b61e3201db0e2323f768a. Deutsch wählen. Alle bisherigen Änderungen enthalten. Die Debugfassung bietet dieselben Inhalte und die bisherige Debugsteuerung (L+R halten, Z drücken).

## Quellen

Letzter normaler Builder: tools/build_kokiri_dialogue_v7.py nach build_ganon_neck_fit.py und vor optional build_debug_version.py. Teilseiten-Vorgaben in tools/kokiri_dialogue_v7.json, kanonische Kapiteltexte in story/*.json. Die bestehende Textfunktion unterstützt explizit die überprüfte Neuverteilung der Deku-Brüder-Lautcodes. Quellarchiv enthält den kumulativen Quellenstand und Prüfungen, keine ROM/Saves/ELF/ausführbaren Programme.

Größter geänderter Rohtext: 1003 von 1280 Bytes; größte dekodierte Seite (konservative Obergrenze): 150 von 200 Bytes.
