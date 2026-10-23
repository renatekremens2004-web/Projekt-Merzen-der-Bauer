# Wasser-Dialoge V58

Die neue Fassung enthält alle bisherigen Änderungen einschließlich der Spezial-Soldaten aus V57.

## Neue Texte

Deine überarbeiteten Sätze sind bei 706B, 4012, 401F, 4013, 4045, 0153, 403E, 403F, 0625, 4046, 4043, 4059, 4044, 406D–4077 (nur die genannten IDs), 4079, 4019, 4030 und 40A1/40A2/40A3/40A6/40A7 eingebaut. Ungewünschte Nachsätze sind entfernt. 0199 und das Augentropfen-Tauschgeschäft bei 4014 bleiben erhalten. Bei 40A7 endet der abgebrochene diktierte Satz mit „Also ich muß mal wieder neues Stroh nachfüllen.“

Der Vier-Meter-Text gehört zu **4070**, der Sieben-Meter-Text zu **4073**. So werden die beiden versehentlich gleich benannten Tiefenstufen getrennt.

Sheiks neuer Zweizeiler steht **nur in der Eishöhle**, unter der eigenen ID **722A**. Der Waldtext 106C und der bisher gemeinsam verwendete Abschluß 106D bleiben erhalten. Alle Kamerafahrten und Einblendungszeiten der Eishöhle sind unverändert.

## Patchen und Debug

Genau einen der beiden BPS-Patches auf eine saubere europäische PAL-1.0-ROM anwenden. Nicht auf eine bereits gepatchte ROM anwenden. Basis-MD5: `e040de91a74b61e3201db0e2323f768a`.

Die DEBUG-Ausgabe behält das Menü über **L+R halten und Z drücken**, „Alle Items“, die Gewandstufen und die Credits-Option. Eisenstiefel liegen weiter auf Steuerkreuz unten, Gleitstiefel auf Steuerkreuz oben. Ein ROM-Abbild ist nicht enthalten.

## Prüfungen

Alle 33 neuen bzw. geänderten Texte passen in die kompilierten Textspeicher: größte Nachricht 1.065 von 1.280 Bytes, größte dekodierte Seite konservativ höchstens 148 von 200 Bytes. Native EVENT-/Fortsetzungscodes bleiben erhalten; keine Änderungen an den Auswahl- oder Belohnungsabläufen.

Normal- und DEBUG-Ausgabe wurden gegen V57 verglichen: 406 Modellbanken, 388 Räume, 101 Szenen und die drei Musikdaten-Segmente. In der Eishöhle ist ausschließlich die abschließende Text-ID geändert; Kameras, Zeiten und alle anderen Szenendaten bleiben gleich. Die normalen Produktionsquellen wurden nach dem DEBUG-Bau wiederhergestellt und die normale ROM identisch erneut gebaut.

Native Gesprächstests laufen mit 4 MiB. Die Testvorrichtungen setzen Alter, Fortschritt und Startposition, damit der jeweilige Abschnitt direkt erreichbar ist; beim Labortest wird der gemessene Tiefenzähler gezielt auf vier bzw. sieben gesetzt. Das ist kein neuer vollständiger Spieldurchlauf. Die einzelnen Ergebnisse stehen im Prüfbericht des Quellenpakets.

## Quellen

Nach dem vollständigen V57-Stand: `python3 tools/build_water_dialogue_v58.py /pfad/oot`. Für die separate Debugfassung anschließend den optionalen letzten Builder `build_debug_version.py` ausführen. Die Textvorgaben stehen in `tools/water_dialogue_v58.json`.

Die beiden Kapitelabschriften enthalten die tatsächlichen IDs und Textbox-Seiten: den nun überarbeiteten Wasserabschnitt sowie den anschließenden Abschnitt bis zum Schattentempel. Die Schattentempel-Abschrift ändert dessen Texte nicht.
