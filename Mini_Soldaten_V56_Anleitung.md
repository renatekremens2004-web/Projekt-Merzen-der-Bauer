# V56: Beans Mini und Schrotflinten-Goronen

V56 enthält alle bisherigen Änderungen einschließlich der Musik aus V55. Genau einen BPS-Patch auf eine **saubere europäische PAL-1.0-ROM** anwenden (MD5 `e040de91a74b61e3201db0e2323f768a`). Die Patches sind kumulativ; nicht auf eine bereits gepatchte ROM anwenden.

## Mr. Beans Auto

Der grüne Mini mit schwarzer Motorhaube steht als Kind am Rand des Weges zum Schloß Hyrule, nahe dem ersten Abschnitt mit Malon. Anvisieren und C-oben öffnet Navis Kommentar:

> Mr Beans Auto. Er fährt damit jeden Morgen zur Arbeit.

Der Mini bleibt nach dem Lesen bestehen und läßt sich erneut ansehen. Er erscheint ausschließlich im normalen deutschen Spiel als Kind. Marty, Doc, DeLorean, Malon, Mario/Talon, Wachen und Eule bleiben erhalten. Der erste normale Eulen-Dialog am Schloß kann weiterhin vor dem Untersuchen des Autos starten.

Das Wii-Modell wurde von 2.142 auf 728 Dreiecke reduziert. Seine Länge beträgt 140 Spiel-Einheiten. Die Geometrie steckt direkt im vorhandenen Raum und benötigt keinen zusätzlichen Objekt-Slot. Eine passive Kollision schützt die Wagenmitte vor dem Durchlaufen; das Auto bleibt abseits der Laufwege.

## Zweite Soldaten-Variante

Im erwachsenen Todesbergkrater stehen zwei zusätzliche Soldaten mit dem hochgeladenen Schrotflinten-Modell. Die bisherigen Soldaten behalten ihre Gewehre. Die neuen Soldaten stehen dauerhaft aufrecht, atmen, blinzeln und schauen zum Spieler. Die Waffen sind ausschließlich getragene Requisiten.

Nahe dem verbrannten Körper:

> Wie schaffst du es, hier drin zu überleben? Der letzte Typ ist in Flammen aufgegangen. Sein Name war Joe.

Erst beim erneuten Ansprechen:

> Joe Mama!

Es gibt keine automatische Textverkettung. Nach dem Schließen verhindert zusätzlich eine kurze Pause das unmittelbare Wiederöffnen durch A-Spam. Die Pointe bleibt für weitere Gespräche dieses Gebietsbesuchs erhalten; nach erneutem Laden des Gebiets beginnt die Geschichte wieder von vorn. Es werden dafür keine Quest- oder Speicherflags verwendet.

Am Weg aus Goronia:

> Goronia hat die stärkste Armee in ganz Hyrule. Und das nur dank Friedrich Merz!

Beide stehen neben den Wegen, fern von der Bolero-Lernstelle. Sie erscheinen nur im normalen deutschen Erwachsenen-Spiel. Kinder-, Bolero- und Credits-Header bleiben unverändert.

Die Schrotflinte hat 136 Dreiecke. Beide Soldaten teilen sich die vorhandene Ausrüstungsbank; deren Zuwachs beträgt 5.744 Bytes. Vorhandene Helme und Gewehre bleiben erhalten.

## Prüfung

Normal- und DEBUG-Build mit nativer 4-MiB-Konfiguration geprüft: beide Gespräche, getrennte Joe-Pointe, Mini mit Navi-Text bei Tag/Nacht, Abwesenheit in der falschen Altersstufe sowie bestehender Gewehrsoldat. Objektbank im Krater: 18/19 Slots und 97.264 Bytes frei. Schloß mit Mini, Zeitreisenden und ursprünglichen Figuren: 14/19 Slots und 27.680 Bytes frei.

Alle bisherigen Texte wurden verglichen und bleiben identisch. 404 andere Objektbanken, 386 andere Räume, sämtliche Szenen einschließlich Credits-Kameras und alle drei Musiksegmente wurden gegen V55 geprüft. Die einzigen neuen Modell-/Platzierungsdaten betreffen die gemeinsame Soldatenausrüstung sowie die beiden betreffenden Räume. Beide BPS-Patches wurden unabhängig angewandt und mit den getesteten ROMs verglichen.

Die Bilder stammen aus dem echten Spiel im Emulator; die Nahansichten verwenden eine Testkamera, ohne die Kameras im Patch zu verändern. Ein kompletter neuer Spieldurchlauf ist damit nicht ersetzt.

## DEBUG und Quellen

DEBUG weiterhin: L+R halten und Z drücken. Die bisherigen Optionen für alle Items, Standard-/Licht-/Schattengewand und Credits bleiben vorhanden.

Der Quellenstand baut auf V55 auf. Danach `python3 tools/build_guests_v56.py /pfad/zum/oot-decomp` ausführen. Die separate Debug-Edition wird zuletzt mit `tools/build_debug_version.py` erstellt; `--restore` stellt die normalen Quellen wieder her. Die neuen Dialoge stehen in `story/guests_v56_de.json`.
