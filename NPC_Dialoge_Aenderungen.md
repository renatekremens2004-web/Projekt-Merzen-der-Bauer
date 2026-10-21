# NPC-Dialoge: Erstgespräch und erneutes Ansprechen

35 ausdrücklich geprüfte Erst-/Wiederholungs-Paare sind jetzt getrennt: Der erste Text endet, und der zweite Text erscheint erst nach erneutem Ansprechen. Das betrifft Markt/Kakariko, Zimmerleute, Luigi als Kind, Malons Vorstellung, Kokiri/Mido, Goronen und Zoras. Die vollständige Zuordnung steht in planning/NPC_Erst_Wiederholung.json im Quellenpaket.

Die Frau mit dem aufgemalten Gesicht sagt beim ersten Gespräch ausschließlich:

> Man sieht mich nur von weiter weg, ansonsten würde auffallen, daß mein Gesicht nur grottenschlecht aufgemalt wurde.

Beim erneuten Ansprechen:

> Mehr Nähe verträgt meine Textur nicht.

Farm-, Klima- und Wegbeschreibungszusätze sind bei ihr entfernt. Ihre Variante nach Zeldas Flucht enthält weiterhin allein die Gesichtspointe. Alle übrigen eigenen Texte bleiben erhalten, lediglich die direkte Verknüpfung zu bestätigten Wiederholungsantworten entfällt. Mehrseitige, zusammengehörende Texte bleiben mehrseitig.

Dialoge mit Antworten, Geschäften, Aufgaben, Belohnungen, Liedern, Zwischensequenzen oder nicht unabhängig erreichbaren Folgeseiten bleiben zusammenhängend. Kein pauschales Abschneiden aller TEXTID-Verbindungen. Die originalen Gesprächsflags und die NPC-Programme bleiben unverändert; sie wählen den Wiederholungstext weiterhin selbst aus. Bei bereits angesprochenen Figuren bleibt der gespeicherte Gesprächsstand gültig.

Der flache Thaddäus ist unverändert ausschließlich für Erwachsenen-Link im Morpha-Raum aktiv. Mit Kind-Link erscheint er absichtlich nicht. Keine Änderung an seiner Geometrie, Platzierung, Altersbedingung oder am Bosskampf.

## Download und Anwendung

Beide Fassungen sind kumulative Gesamtpatches auf die unveränderte Europa/PAL-1.0-ROM, nicht auf eine zuvor gepatchte ROM. Original-MD5 e040de91a74b61e3201db0e2323f768a. Mit https://www.marcrobledo.com/RomPatcher.js/ anwenden und Deutsch wählen.

- Mr_Burns_Mr_Bean_DE_PAL10_NPC_Dialoge.bps: normale Fassung.
- Mr_Burns_Mr_Bean_DE_PAL10_DEBUG_NPC_Dialoge.bps: gleiche Inhalte plus die bereits funktionierenden Debugmenüs. L+R halten, Z drücken; im offenen Pausemenü L für den Inventar-Editor. Für Tests eine eigene Spielstandkopie verwenden.

## Prüfung

PAL-Builds und ROM-Prüfsummen geprüft. Nur 36 deutsche Nachrichten ändern sich: 35 erste Nachrichten verlieren ihre bestätigte Wiederholungsverknüpfung; bei der Gesichtspointe ändern sich zusätzlich die Worte der Wiederholungsantwort. Alle anderen deutschen Nachrichten und sämtliche anderen Sprachen sind bytegleich. Alle Räume, Modelle, Kollisionen und Schauspielerprogramme bleiben bytegleich. Im Engine-Segment ändern sich ausschließlich deutsche Texttabellen-Zeiger. Textpuffer und Zeilenbreiten geprüft; keine veränderten festen Lesezeiten oder größere Speicherpools.

Zwei gezielte Laufzeitproben der finalen Debug-ROM mit echten 4 MiB: Gesichtsfrau und Autobatterien-Frau. Jeweils erstes Gespräch über normale Controller-Eingaben, normales Ende mit gesetzter ursprünglicher Gesprächsflag, anschließende Wartephase ohne automatisch angehängten Wiederholungstext und dann ein zweites, ausdrücklich gestartetes Gespräch mit der richtigen Wiederholungs-ID. Testspielstand-Einstieg mit Kind-Link tagsüber, gelöschten Erstgesprächsflags und Spielerposition nahe dem unveränderten NPC; keine versetzten NPCs. Keine fehlgeschlagenen Arena-Belegungen oder Grafik-/Objektpufferüberläufe. Kein vollständiger Spieldurchlauf und keine Einzel-Laufzeitprobe jedes der 35 Paare.

Beide BPS sind mit RomPatcher.js und aktiver Quellvalidierung auf Vanilla angewandt und bytegleich mit den jeweiligen gebauten ROMs.

## Quellen

Nach den bisherigen kumulativen Buildern zuletzt build_shadow_tunic.py, build_tunic_icons.py, build_market_face_dialogue.py und build_npc_repeat_dialogue.py ausführen. Für Debug danach build_debug_version.py. Zum normalen Quellstand mit dessen --restore zurückkehren und neu bauen. Der gemeinsame Text-Builder erlaubt das Kürzen normaler, manuell bestätigter Seiten nur mit ausdrücklichem short_manual-Eintrag und schützt Antwort-/Item-/Timer-Steuerungen weiterhin. Keine ROMs, Spielstände, SRAM, Savestates, ELF oder ausführbaren Programme im Quellenpaket.

Normale Ziel-SHA256: d9936c901aec39e893a31da2a3e999a779ede4056ff3a049ffecd794b2422345

Debug-Ziel-SHA256: 88e5a9fdd65db1f8adc0dafd25d59f39eaad3dc7af9cb025b3278e4ac5f1209e
