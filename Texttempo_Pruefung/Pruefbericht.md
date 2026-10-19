# Texttempo: normale deutsche Textboxen

Normale schwarze, blaue und Holz-Textboxen zeigen bis zu zwei statt eines druckbaren Zeichens pro Spielbild. Das ergibt etwa doppeltes Schreibtempo. Seiten bleiben nach vollständigem Aufbau bis zum Tastendruck stehen. A/B, Auswahlsteuerung, Lesepausen, Seitenumbrüche, Nachrichteninhalt und Spielstart sind unverändert.

Die Änderung steckt ausschließlich im westlichen Textzeichner in `src/code/z_message.c`: Der native Parser liest weiterhin jedes Steuerzeichen. Ein zusätzliches Zeichen wird nur freigegeben, wenn beide nächsten Bytes druckbar sind und innerhalb der dekodierten Seite liegen. Eine konservative Prüfung der kompletten dekodierten Seite schließt spezielle Steuerungen aus. Deutsche Standardsprache, normaler Textmodus, kein Credits-Text und keine laufende geskriptete Cutscene sind Voraussetzung.

Ausgenommen bleiben Textseiten mit Zeitvorgaben (verzögerter Umbruch/Überblendung), Wahlmöglichkeiten, Quicktext, explizitem TEXT_SPEED, Instrumentsteuerung, Soundeffekten oder anderen speziellen Steuerzeichen. Andere Sprachen behalten die bisherige Darstellung. Reine manuell weitergeschaltete Ereignistexte können schneller erscheinen. Keine Änderung an B: Die bisherige Sofortanzeige bleibt erhalten; zum normalen Lesen ist sie mit diesem Tempo weniger nötig.

## Messungen in der Produktions-ROM

- mido, Seite 107: 110 → 58 beobachtete Frame-Schritte bis fertig; gleiche 111 dekodierte Textbytes.
- music, Seite 110: 113 → 59 beobachtete Frame-Schritte bis fertig; gleiche 114 dekodierte Textbytes.

Jedes normale Beispiel blieb nach Fertigstellung mindestens 80 beobachtete Frame-Schritte ohne Eingabe geöffnet. Die gleiche englische Gegenprobe ist in allen protokollierten Textzuständen framegleich. Der native Merz-Text 700A nach dem Ziehen des Masterschwerts ist einschließlich seiner vier automatisch getakteten Seiten und Überblendung framegleich. Bei der nativen Wundererbsen-Auswahl 405E ist der Schriftaufbau der Auswahlseite nach deren Beginn framegleich; die manuell gelesene Einleitung erscheint schneller. Auswahlcursor und Kauf/Itemtext 0048 funktionieren weiterhin. B zeigt in beiden Fassungen den offenen Dialog sofort an.

Gleiche SaveContext-Teststände und Controllerabläufe, GLideN64 mit EnableClipping=True und EnableCustomSettings=False, 4 MiB ohne Speichererweiterung. Testpositionen werden über den regulären Respawn des Spielers vorbereitet. Keine Schreibzugriffe auf Nachrichtentext, Anzeigeposition, Nachrichtenzustand oder Timer. Native NPCs stehen an ihren Originalplätzen. Die Versuche mit unpassend aufgestellten Testspielern wurden als Fixture-Probleme verworfen und nicht als erfolgreiche Auswahlprüfung gezählt.

## Binäre Prüfung

- Ausgangspunkt: veröffentlichte Zora-Gags-Fassung, SHA256 e5265a6b63a509db46442920f6500c2f8a1dfd377ad3e7b277d42228a63c3db8.
- Alle 2115 deutschen ROM-Nachrichteneinträge unverändert, ebenso englische/französische Textsegmente und alle 599 bearbeiteten Kontrollsequenzen/Seitenzahlen.
- Alle 1509 gepackten Segmente geprüft, CIC-6105-Prüfsumme korrekt, weiterhin 32 MiB.
- Modelle, Räume, Animationen und Speicherbudgets erhalten; andere ausführbare Segmente ändern sich nur an verifizierten Linker-Relokationen auf verschobene Adressen.
- Rücknahme exakt des Helfers und der Zusatzzeichen-Freigabe ergibt die SHA256-geprüfte vorherige Produktionsdatei z_message.c. Spielstandinitialisierung bytegleich zur normalen Vorfassung.
- BPS mit RomPatcher.js auf die validierte Vanilla-ROM angewandt und Ausgabe bytegleich zur geprüften Produktions-ROM.

Kein kompletter Spieldurchlauf und kein Test auf echter N64-Hardware. Die gezielten Vergleiche sind in `validation/text-speed/` protokolliert. Laufzeit-Save-Dateien, komplette ROMs und ELF-Dateien werden nicht veröffentlicht.

## Nachbauen

Bestehende Mod-Generatoren in der bisherigen Reihenfolge anwenden. Nach `build_story.py` immer `build_habeck.py` ausführen, um dessen sichere TEXTID-Fortsetzungen wiederherzustellen. Danach `python tools/build_text_speed.py /pfad/zum/oot` anwenden; wiederholtes Anwenden ist ohne weitere Änderung möglich. Normalen PAL-1.0-Build und Kompression wie bisher ausführen. Prüfung: `python tools/verify_text_speed.py /pfad/zum/oot /pfad/zur/veröffentlichten-Zora-Gags-ROM.z64`.
