# V44: Sonnengewand, Schutzstufen und bequemeres DEBUG-Menü

Normal und DEBUG enthalten sämtliche Änderungen aus V43 sowie das neue Sonnengewand und die angepaßten Schutzstufen. Nur die DEBUG-Version enthält zusätzlich die beiden neuen Menüoptionen.

## Die Gewänder

Habeck kündigt bei der ersten Begegnung nach dem Ziehen des Master-Schwerts das Sonnengewand an. Bei der Übergabe des Lichtamuletts erhält Link zusätzlich dieses Gewand; eine eigene Meldung bestätigt den Erhalt. Die native Cutscene und das Lichtamulett bleiben erhalten.

Das Sonnengewand ersetzt die grüne Kleidung durch Goldgelb und wird automatisch angelegt. Es gilt auch nach einer Rückkehr zur Kindheit. Inventarsymbol und Name passen zum aktuellen Gewand. Das Schattengewand aus der bestehenden Brunnen-Kiste ersetzt es später durch Schwarz und schützt stärker.

| Gewand | Gewöhnlicher Schaden |
| --- | --- |
| Ursprüngliches grünes Gewand | 100 % |
| Gelbes Sonnengewand | 50 % |
| Oranges Wallace-/Feuergewand | 50 % |
| Hellblaues Zora-/Wassergewand | 50 % |
| Schwarzes Schattengewand | 25 % |

Die Schutzboni werden nicht miteinander multipliziert. Auch mit einem nativen Doppelverteidigungsbonus bleibt das Schattengewand bei einem Viertel. Positive Heilung bleibt unverändert; sehr kleine Treffer verursachen weiterhin mindestens eine native Gesundheitseinheit. Hitze- und Unterwasserfunktionen der Spezialgewänder bleiben erhalten.

## Bedienung des DEBUG-Menüs

1. Im Spiel **L + R halten und Z drücken**.
2. **C-links: Alle Items** – nach dem Drücken erscheint **[OK]**.
3. **C-rechts: Schattengewand AN/AUS** – jeder Tastendruck wechselt die Auswahl.
4. Wie bisher Ort auswählen, mit **B** Kind/Erwachsen bestimmen und mit **Z/R** Tageszeit/Cutscene wählen.
5. Mit **A oder Start** den Ort laden. Dabei werden die gewählten Optionen übernommen.

Die C-Tasten sind die gelben C-Tasten des N64-Controllers bzw. deren Belegung im Emulator, nicht das Steuerkreuz. Das Steuerkreuz bleibt für die Ortsliste und im Spiel für die Stiefel zuständig.

## Was „Alle Items“ gibt

- Sämtliche normalen Inventarwerkzeuge in ihrer stärksten Version, darunter Okarina der Zeit, langer Fanghaken und Wallace-Hammer.
- Alle Schwerter, Schilde, drei Gewänder und drei Stiefelpaare, einschließlich Eisen- und Gleitstiefeln; das Biggoron-Schwert ist unzerbrechlich.
- Maximale gültige Tragetaschen, Köcher, Stärke, Schuppe und Geldbörse; volle Munition, zehn Wundererbsen und 500 Rubine.
- Volle doppelte Magieleiste und Auffüllen der vorhandenen Herzen. Die Zahl der Herzcontainer wird nicht verändert.
- Alle zwölf Okarina-Lieder, Gerudo-Pass und Stein des Wissens sowie Dungeon-Karten, Kompasse, große Schlüssel und mindestens neun kleine Schlüssel pro Schlüsselzähler.
- Leere fehlende Flaschen. Vorhandene Flaschen samt Inhalt und die beiden Masken-/Tauschslots bleiben erhalten; ein leerer Tauschslot bekommt das jeweilige Ei als Startgegenstand. Mehrere Masken bzw. Tauschgegenstände passen im nativen Inventar nicht gleichzeitig in denselben Slot.

Zusätzlich wird das Sonnengewand freigeschaltet. Das Schattengewand bleibt separat steuerbar.

Die Option fügt keine weiteren heiligen Steine oder Amulette hinzu und setzt keine zusätzlichen Story-, Tempelabschluss- oder Schaltermarkierungen. Bereits vorhandener Fortschritt bleibt bestehen, auch der bisherige Startzustand einer frischen temporären DEBUG-Sitzung.

## Schattengewand

**AN** aktiviert das vorhandene Schattengewand und legt es an. **AUS** legt das Sonnengewand an, wenn es bereits freigeschaltet wurde; andernfalls wird das ursprüngliche grüne Gewand wiederhergestellt. Die Auswahl gilt für Kind und Erwachsen und übersteht den Alterswechsel.

Das Auffüllen der Items schaltet das Schattengewand nicht automatisch ein. Ohne eine Änderung am Gewandschalter bleibt dessen bisheriger Zustand erhalten. Beide Funktionen lassen sich unabhängig verwenden.

Das Schattengewand gibt beim Tragen ein Viertel Schaden. Feuer- und Wassergewand bleiben orange bzw. hellblau und geben unabhängig davon dauerhaft halben Schaden. Es wird kein permanenter Doppelverteidigungsbonus hinzugefügt.

## Geprüft

- Sechs native Lade-/Menüdurchläufe mit **4 MiB RAM**: frischer Einstieg vom Titel, vorhandener Spielstandzustand, Kind/Erwachsen und mehrfaches Umschalten des Gewands.
- Tatsächliche Controller-Eingaben für die neuen Optionen; Prüfung aller normalen Inventarslots, maximaler Upgrades, Munition, Lieder, Magie, Stiefelbesitz und aktualisierter C-Tasten.
- Gewand allein verändert keine Ausrüstung oder Upgrades; die getrennten Altersausrüstungen, Flaschenpost, Tauschfortschritt und benachbarte Speicherflags bleiben erhalten.
- „Credits starten“, laufende Originalmusik und Rückkehr ins normale Spiel funktionieren weiterhin.
- Die vollständige erste Master-Schwert-/Habeck-Sequenz mit neuer Ankündigung, Lichtamulett und Sonnengewand-Übergabe wurde mit 4 MiB durchgespielt.
- 6.912 Prüfungen der tatsächlichen Schadensfunktion und 40 Ausrüstungsprüfungen bestanden. Diese ergänzenden Hostprüfungen ersetzen keinen vollständigen Spieldurchlauf.
- Alle 405 Modellbanken und 388 Räume bleiben gegenüber V43 bis auf neu gelinkte Verweise auf die unveränderte Identitätsmatrix gleich. Die neun überprüften Credits-Kamerafahrten und beide Hof-Cutscenes sind bytegenau unverändert.
- Bestehende Texte bleiben erhalten; nur Habecks Abschluß und die Lichtamulett-Meldung bekommen eine Fortsetzung. Die Schattengewand-Meldung nennt den neuen stärkeren Schutz. Beide neuen Text-IDs bleiben innerhalb der nativen Puffer.
- Die nach dem DEBUG-Bau wiederhergestellte normale ROM ist byteidentisch zum normalen V44-Bau.
- BPS mit geprüfter Quell-ROM angewendet und mit dem gebauten DEBUG-Ergebnis bytegenau verglichen.

## Patch anwenden

Den normalen V44-BPS-Patch oder den DEBUG-V44-BPS-Patch auf die **saubere europäische PAL-1.0-ROM (.z64)** anwenden, nicht auf eine bereits gepatchte ROM. MD5 der sauberen Quell-ROM: `e040de91a74b61e3201db0e2323f768a`.

Das Quellenarchiv enthält die kumulativen Quellen, den normalen V44-Patch und den neuen DEBUG-V44-Patch. Es enthält keine ROM.
