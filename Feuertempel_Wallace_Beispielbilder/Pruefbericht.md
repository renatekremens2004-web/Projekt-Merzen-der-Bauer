# Feuertempel: Wallace, Ausrüstung und Credits-Sitzpose

Gesamtpatch mit allen bisherigen Änderungen. 19 deutsche Nachrichten für dieses Kapitel geändert, insgesamt 977 eigene Nachrichten. Tatsächlich eingebaute Dialoge: planning/FEUERTEMPEL_WALLACE_DIALOGE_AKTUELL.md. Deutsch vor 1996; normale manuelle Textseiten dürfen länger werden, native Quest-/Item-/Auswahlsteuerung und feste Ausblendzeiten bleiben erhalten.

## Inhalt

Der namensgleiche Gorone beschwert sich über Bombenwurf und seinen eigenen Namen, bemerkt die Namensgleichheit, entschuldigt sich und übergibt die von Wallace entwickelte Goronen-Rüstung. Der Merz-Zwangsdienst im Feuertempel erscheint als schlecht bezahlte Dauer-/Nachtschicht. Die originale Tunika schützt weiterhin vor Hitze, getragenes RGB jetzt 200/75/0 (Orange); das Inventar-Icon bleibt rot. Beschreibung: „Wallace hat die erfunden“. Stahlhammer/Megaton Hammer heißt im deutschen Aufnahmetext und Pausenmenü „Wallace Hammer“, ohne Änderung der Item-ID oder Funktionen. Andere Sprachen bleiben erhalten.

Ein vorher unveränderter NPC (bärtiger Gast im Kakariko-Gästehaus, erwachsene Nacht-Version) schwärmt peinlich von Volvagia. Navis Bossbeschreibung verweist auf ihn. Sheik trägt beim nativen Bolero-Auftritt das neue Feuer-/Einkaufs-/Wallace-/Bean-Gedicht vor; Lehren, Nachspielen und Songfreigabe bleiben nativ.

Wallace ersetzt genau einen normalen Gefangenen im unteren Felslabyrinth, Feuertempel-Raum 5, Parameter 0D83, Zellschalter 3, Position 2212/2800/1091. Der NPC behält Zelle, Befreiung, Schlüsseltruhe und Fluchtpfad; kein zusätzlicher Actor oder Objekt-Slot. Private deutsche Text-IDs 209D und 209E verwenden die normale EVENT-Steuerung. Der Gefangene spricht nach der Freilassung und verschwindet normal über seinen Fluchtweg. Der zusätzliche Text vor der Freilassung ist statisch eingebaut, wurde im schlafenden nativen Zustand jedoch nicht als Gespräch beobachtet.

Darunia bleibt in der Kindheit und bei seinem lebenden Feuertempel-Auftritt erhalten. Erst ab der Feuerweisenrolle (DemoDu-Parameter 0, 2 und 3) erscheint Wallace in deutscher Sprache: Halle der Weisen, finale Siegel und Credits. In der Halle berichtet er vom tödlichen Gouda-/Wensleydale-Versuch an einer laktoseintoleranten Drachendame, ermutigt zum Forschen, klagt über Merz' Forschungskürzungen und verabschiedet sich mit Gromit und Käse. Der Abschied 303D behält exakt seine originale einzelne Seite und FADE(80).

## Modelle und Sitzpose

Nutzerquelle wallace-freeman-hl2-but-ruined-by-mods.zip. Überlappende Körperkopie und alternative unsichtbare Lidvarianten entfernt, auf 2.269 Dreiecke reduziert. Vier eigene Teile mit festen Achsen, eigene Proportionen, einheitliche Höhe 110 Spieleinheiten. Fünf CI4-Texturen 64×64, je 2.048 Bytes plus Palette. Beleuchtung, Nebel und alpha-gesteuertes Einblenden bleiben nativ. Keine Laufzeit-Streckung. Frühere 128×64-Kopftextur verworfen, da sie TMEM-Korruption erzeugte; ausgeliefert wird ausschließlich die korrigierte 64×64-Fassung.

Der Objektblock behält alle ursprünglichen Darunia-Daten und ergänzt das Wallace-Modell. Raum 5 enthält seine eigene Modellkopie im Raumsegment, ohne zusätzlichen Objekt-Slot. Der Kind-Wallace in Dodongos Höhle ist unverändert. Quellen-/Lizenzhinweise: models/wallace-adult/README.md und CREDITS.md.

Die Krabbelminen-Frau erhält ausschließlich für ihre drei Credits-Sitzanimationen eine neue Haltung. Die frühere seitliche Spreizung auch der Unterschenkel ist beseitigt: Oberschenkel nach vorn, Schienbeine fast senkrecht, Hände am Kragen, Oberkörper nur zwei Grad zurückgelehnt. Ihr Körper, eigene Knochenlängen und alle anderen Animationen bleiben gleich. Die Sitzwurzel [-100,9400,300] gleicht die nativen Actor-Abstände (+1/+2,25/−9) aus; relativ zu Wallace liegt sie bei 0/96,25/−6. Die gemeinsame Credits-Kamera ist weiter zurückgesetzt und etwas höher ausgerichtet. Sämtliche Cues, Frames, FOV-Werte und sonstige Kameraabschnitte wurden gegenüber der vorherigen Fassung binär erhalten.

## Echte Credits-MP4

Wallace_Weise_Credits_v3.mp4: 647 aufeinanderfolgende gerenderte Frames, 38,82 Sekunden, 640×480, PAL 50/3 Bilder pro Sekunde, ohne Ton. Native Positionen, keine Eingaben, keine Montage und keine ausgetauschten Bilder. Enthalten ist der Übergang in die nächste Credits-Szene. Die fünf gemeinsamen Weisen sind Wallace, Krabbelminen-Frau, Thaddäus, Waluigi und Mr. Bean. Rauru/Habeck gehört bereits im Original nicht zu dieser gemeinsamen Todesberg-Einstellung. Native Nahaufnahmen dürfen andere Figuren teilweise abschneiden; die gemeinsame Gruppenaufnahme zeigt den neuen Sitz vollständig.

## Prüfungen und Grenzen

Finale ROM-SHA256: `ce303971fb48595d137aec348a323b52a74af487c56d3c34272b8c8b662cfff8`. 32 MiB, CIC-6105. Alle 1509 komprimierten Segmente mit dem unkomprimierten Neubau verglichen. 977 Textpuffer innerhalb ihrer Grenzen, 19 geänderte deutsche Nachrichten. Alle vorherigen deutschen Kapitel sowie englische/französische Texte und native Kontrollsequenzen erhalten. 2954 Kernfunktionen, 93 EnGo2-Funktionen und 91 DemoDu-Funktionen abseits der dokumentierten Hooks über originale Bytes oder echte MIPS-Relokationen geprüft. Ursprüngliche Darunia-/Raum-Assets und andere Modelle/Szenen erhalten.

Auf der finalen ROM abgeschlossen: Hallen-Sequenz mit allen neuen Käse-/Forscher-/Gromit-Texten, nativer Amulettübergabe und Rückkehr zum Todesberg; vollständige gemeinsame Credits-Aufnahme mit allen fünf Actors und nativer Fortsetzung. Emulator Mupen64Plus/GLideN64, echte 4 MiB RAM. Freier Objektpuffer im gemeinsamen Credits-Abschnitt mindestens 15.440 Bytes, in der Feuer-Halle 33.856 Bytes; der Puffer wurde nicht vergrößert.

Frühere gezielte Proben auf SHA256 `d5632e191dbb1dd5c8bd8b037d9fb6cea769e22ca0d6f39efca15c25f6c4ea45`: native Befreiung aus Raum 5, alle sieben privaten Gesprächsseiten und selbständige Flucht; Sheik-Gedicht, Bolero normal nachgespielt und gelernt; vier Seiten des Drachenfreunds; vollständige finale Siegel-Sequenz bis Szenenwechsel; englische Negativproben mit ursprünglichem Darunia und Goronen-Modell. Die finale statische Prüfung bestätigt, daß EnGo2, DemoDu, Sheik, Raum 5, object_du und Item-Namen dieser Proben bis auf Linker-Relokationen gleich geblieben sind. Alle Kapiteltexte dieser Proben sind unverändert, ausgenommen die vier Hallen-Reden, die auf der finalen ROM erneut geprüft wurden.

Zusätzliche assistierte Probe: ein vorbereitetes natives AC_HIT-Trefferbit löst 3031 aus; alle sechs Empörungsseiten gesehen. Kein Nachweis eines echten Bombenwurfs oder der gesamten Tunika-Quest. Die automatisierten Hammertruhen-Proben erreichten wegen der Flammen-/Steuerungsposition nicht den Gegenstandserhalt und zählen nicht als bestandener Item-Erhalt-Test. Hammername, Text, Inventar-ID und native Funktionen sind statisch geprüft. Kein kompletter Spieldurchlauf und kein N64-Hardwaretest.

RomPatcher.js mit aktiver Quellprüfung erzeugt aus Original-MD5 e040de91a74b61e3201db0e2323f768a bytegleich den finalen Neubau. BPS direkt auf die unveränderte entpackte Europa/PAL-1.0-ROM anwenden, nicht auf eine alte Mod-ROM. Normale Spielstände statt alter Emulator-Save-States verwenden. Keine Original-ROM, Spielstände, RAM-Abbilder oder ausführbaren Programme im Downloadpaket.
