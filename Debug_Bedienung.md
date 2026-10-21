# Debugversion bedienen

Der DEBUG-Gesamtpatch enthält alle bisherigen Änderungen einschließlich Schattengewand und passend orange/hellblau gefärbter Gewandicons. Er schaltet zusätzlich die vorhandene Szenenauswahl und den Inventar-Editor frei. Der normale Gewandicons-Gesamtpatch enthält dieselben Spielinhalte ohne die Debugmenüs.

Beide BPS-Dateien einzeln mit [RomPatcher.js](https://www.marcrobledo.com/RomPatcher.js/) auf die **unveränderte, entpackte Europa/PAL-1.0-ROM** anwenden. Original-MD5: `e040de91a74b61e3201db0e2323f768a`. Im Spiel Deutsch wählen.

## Szenenauswahl

Auf Controller 1 **L und R halten, dann Z drücken**. Das funktioniert am Titelbildschirm, in der Dateiauswahl und im Spiel. Für Ortswechsel aus dem Spiel eine normale steuerbare Spielsituation verwenden.

| Taste | Funktion |
| --- | --- |
| Steuerkreuz hoch/runter | Ort auswählen |
| Steuerkreuz links/rechts | Liste schneller durchlaufen |
| L | Zum nächsten Listenabschnitt springen |
| B | Kind / Erwachsener umschalten |
| Z / R | Tag, Nacht und die ursprünglichen Demo-Varianten durchschalten |
| A oder Start | Ausgewählten Ort laden |

Zum normalen Erkunden **Day** oder **Night** benutzen. Die Demo-Varianten funktionieren nur, wenn die jeweilige Szene eine passende Zwischensequenz besitzt. Eine Szenenauswahl versetzt Link an den Ort; sie stellt den dazugehörigen Storyfortschritt nicht automatisch her. Welche NPCs erscheinen und was sie sagen, hängt weiterhin vom Testspielstand ab.

Einige hilfreiche Listennummern:

| Nummer | Ort |
| --- | --- |
| 2 | Kakariko |
| 5 | Kokiri-Wald |
| 15 | Schloß Hyrule |
| 20 | Zitadelle der Zeit |
| 21 | Halle der Weisen |
| 41 | Hyrule-Stadt |
| 68 | Dodongos Höhle |
| 70 | Jabu-Jabu |
| 72 | Waldtempel |
| 74 | Brunnen |
| 75 | Schattentempel |
| 77 | Feuertempel |
| 79 | Wassertempel |
| 81 | Geistertempel |
| 86 | Eishöhle |

Die verbleibenden Ortsnamen stehen teilweise auf Englisch im ursprünglichen Menü. Beim Alterswechsel wird auch die passende Ausrüstung gewechselt. Die bereits vorhandenen Stiefel-Schnelltasten bleiben im normalen Spiel aktiv: unten Eisenstiefel, oben Gleitstiefel.

## Inventar bearbeiten

**Start drücken, warten bis das Pausemenü offen ist, dann L drücken.** Mit L den Editor wieder schließen; anschließend mit Start ins Spiel zurückkehren.

Das Steuerkreuz wählt ein Feld. Die C-Tasten verändern den Wert. Bei Rubinen: C-links −1, C-rechts +1, C-hoch −100, C-runter +100. Bei den meisten Mengen/Verbesserungen verringern C-hoch/C-links den Wert und C-runter/C-rechts erhöhen ihn. Bei Gegenständen schaltet C-hoch häufig den Besitz um bzw. entfernt sie, C-links/C-rechts ändern den Gegenstand oder die Menge; die Belegung ist feldabhängig. Neue Ausrüstung danach im normalen Ausrüstungsmenü anlegen.

Der Editor bietet Gegenstände, Munition, Herzen, Schlüssel, Verbesserungen, Ausrüstungsbesitz, Lieder, Steine und Amulette. Für einen bestimmten Handlungsstand eignet sich am besten eine Kopie eines entsprechend weit gespielten Spielstands.

Bei den vier Ausrüstungsfeldern rechts stehen die Ziffern für Schwert, Schild, Gewand und Stiefel. Dort schalten C-links, C-unten und C-rechts jeweils das erste, zweite und dritte Ausrüstungsteil ein oder aus. Für Eisenstiefel das ganz rechte Feld markieren und C-unten drücken: Aus 1 wird 3 (normale plus Eisenstiefel). 7 bedeutet alle drei Stiefelpaare. Anschließend als Erwachsener im normalen Spiel mit Steuerkreuz unten umschalten.

## Testspielstände

Für die Debugversion eine **eigene Kopie des Spielstands** verwenden: Änderungen aus dem Editor können beim normalen Speichern dauerhaft werden. Je nach Emulator muß die SRAM-Datei dem Namen/der Kennung der Debug-ROM zugeordnet werden. Keine Savestates einer anderen ROM-Version laden.

Öffnest Du die Szenenauswahl direkt am Titelbildschirm ohne geladenen Spielstand, beginnt eine temporäre Sitzung mit dem ursprünglichen Testinventar. Dieses bleibt bei weiteren Ortswechseln innerhalb der Sitzung erhalten. Die Sitzung hat keinen echten Speicherplatz und wird nicht in einen SRAM-Slot geschrieben; zum Behalten von Fortschritt zuerst einen normalen Testspielstand laden.
