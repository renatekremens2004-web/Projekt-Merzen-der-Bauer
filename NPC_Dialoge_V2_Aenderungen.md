# NPC-Dialoge V2: keine unnötigen Wegzusätze; Twinrova nennt Merz

Kumulativer Gesamtpatch mit allen bisherigen Änderungen einschließlich schwarzem Schattengewand, orange/hellblauen Icons und den getrennten 35 Erst-/Wiederholungs-Paaren. Debugsteuerung bleibt wie in der bereits funktionierenden Version.

## Geändert

Überflüssige Richtungs-/Ortszusätze aus 14 deutschen Texten entfernt oder gekürzt: Schloß rechts, Seitengassen links, Zitadelle im Nordosten, Treppen im Norden, Dorf-/Trainingslager-Eingänge und ähnliche Anweisungen. Keine zufälligen Wegbeschreibungen mehr hinter den entsprechenden Gags. Wiederholung zum Thaddäus-Gerücht besteht nur noch aus dessen Klarinetten-/schlechter-Laune-Gag; Beans Überdosis-Rettungsspruch steht ohne den angehängten Weg zum Schloß. Goronen-Nachfragen konzentrieren sich auf Merz/Darunia statt auf eine Wegbeschreibung.

Konkrete Rätsel, Aufgaben, Spielregeln und nötige Fortschrittshinweise bleiben erhalten, zum Beispiel Malons Suche nach Mario, die Wald-Musik, das Auge der Wahrheit in der Wüste, Zoras Brief und die königliche Erlaubnis. User-Witze wie Sheiks Warnung vor schwebenden Krügen oder Boris' ausdrücklicher Verweis auf den Waldtempel bleiben erhalten.

Zusätzlich steht in der Einleitung des Koume-/Kotake-Bosskampfs (6048) jetzt: „Sieh Dir diesen Dummkopf an! Er kam freiwillig als Opfer für den mächtigen Friedrich Merz...“ Der bisher verbliebene Ganondorf-Verweis ist an dieser Stelle ersetzt. Der absichtliche Gerudo-Dialog über Ganondorf, den Merz abgeschoben hat, bleibt als Handlungsteil bestehen.

## Anwendung

Je einen BPS-Gesamtpatch mit https://www.marcrobledo.com/RomPatcher.js/ auf die unveränderte entpackte Europa/PAL-1.0-ROM anwenden, nicht auf eine bereits gepatchte ROM. Original-MD5 e040de91a74b61e3201db0e2323f768a. Deutsch wählen. Normale und DEBUG-Fassung enthalten dieselben Spielinhalte; Debug fügt die bestehenden Menüs hinzu.

## Prüfung

15 bestehende deutsche Nachrichten geändert, keine zusätzlichen IDs oder Schauspieler. Alle übrigen Nachrichten, alle anderen Sprachen und sämtliche Steuersequenzen sind erhalten. Insbesondere bleibt FADE(90) bei der Twinrova-Einleitung exakt gleich; auch die verzögerten Eulenseiten behalten ihre Timer. Beide PAL-Builds und Prüfsummen sowie alle betroffenen Textpuffer und Zeilenbreiten geprüft. Alle 35 vorherigen Dialogtrennungen bleiben erhalten. Geometrie, Kollisionen und Akteurslogik sind gegenüber der letzten veröffentlichten Fassung erhalten. Die kürzeren Texte verschieben einige ROM-Adressen über eine Ausrichtungsgrenze; alle daraus folgenden Änderungen an Raum-/ROM-Zeigern und anderen Stellen sind einzeln als Linker-Relokationen geprüft. Im Engine-Segment ändern sich die deutschen Texttabellen-Zeiger und diese geprüften Relokationen. Keine vergrößerten Speicherpools oder geänderten Eingaben.

Beide Patches wurden mit RomPatcher.js und aktiver Quellvalidierung auf Vanilla angewandt; die Ergebnisse sind bytegleich mit den gebauten ROMs. Für diese reine Textänderung keine neue Laufzeitprobe. Die vorherigen 4-MiB-Gesprächsproben sind weiterhin im Quellenpaket dokumentiert; kein vollständiger Spieldurchlauf.

## Quellen

Nach den bisherigen kumulativen Buildern zuletzt build_shadow_tunic.py, build_tunic_icons.py, build_market_face_dialogue.py, build_npc_repeat_dialogue.py und build_no_wayfinding_dialogue.py ausführen. Debug optional danach mit build_debug_version.py. Das Kürzen gewöhnlicher manueller Seiten benötigt einen ausdrücklichen short_manual-Eintrag; Choices, Items und Timer sind dagegen geschützt. Die neue Ausnahme für eine unveränderte Uhrzeit-Anzeige wird zusätzlich durch den vollständigen Steuersequenzvergleich abgesichert.

Vollständige Zuordnung der 15 Änderungen: planning/NPC_ohne_Wegbeschreibungen.json. Quellenpaket ohne ROM, Saves, SRAM, Savestates, ELF oder ausführbare Dateien.

normal Ziel-SHA256: 66e8354f255a994144a769c2ceff7b60211e924a0935615ef9d834a79ef4a75d

debug Ziel-SHA256: 5887b9ec2c470af1367cd8772f17b5c6c17f54fb5d73922102684a5dddb1a026
