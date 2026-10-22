# Credits V30 – Platzierung und Bodenkontakt

Kumulativ, alle früheren Änderungen einschließlich V29 enthalten. Normal **oder** DEBUG auf eine **saubere europäische PAL-1.0-ROM** anwenden, MD5 `e040de91a74b61e3201db0e2323f768a`. Nicht auf eine bereits gepatchte ROM. Keine ROM enthalten. DEBUG-Menü wie bisher: L+R halten, Z drücken.

## Geänderte Zusammenstellung

- Mystery Inc steht weiter hinten bei der Mystery Machine, in einer lockeren Gruppe mit unterschiedlichen Abständen und Blickrichtungen. Wagen und Gang drängen sich nicht mehr vor Malon. Frankys Position bleibt exakt erhalten.
- Fanboy und Chum Chum sind kleiner und weiter hinten zwischen den anderen Gästen. Fanboy tanzt mit reduzierter Amplitude einer bereits für Mackey und Doofenshmirtz angepaßten Animation.
- Skipper, Kowalski, Private, Rico und Pingu bilden eine lockere Gruppe statt einer geraden Reihe. Unterschiedliche Tiefen und Blickrichtungen; keine zusätzliche menschliche Tanzanimation für diese Modelle.
- Wawario und Wawaluigi sind auf 80 % ihrer bisherigen Credits-Größe verkleinert und weiter im Hintergrund zwischen den ursprünglichen Gästen verteilt.
- Crocker steht seitlich versetzt hinter Pepsiman und bekommt eine kleinere Variante des getesteten Tanzes. Pepsiman und die beiden Tänzer in der Händlerreihe bleiben animiert.
- Wario sitzt weiter seitlich und längs versetzt von Mido. Mido bleibt auch in der hinteren Nahaufnahme sichtbar. Warios Credits-Kopie ist zusätzlich geringfügig auf 95 % verkleinert, damit sie in die breitere Einstellung paßt.
- Marty und Doc stehen links und rechts von Links Weg, auf derselben unteren Rasenebene. Sie begleiten ihn zu Zelda und verdecken ihn in seiner Nahaufnahme nicht. Ihre Arme sind entspannt und bekommen nur kleine Bewegungen. Nur die letzte Totale ist etwas weiter gefaßt, damit die Begleiter neben Link sichtbar bleiben. Die vorherigen Nahaufnahmen und das Ende mit Sepia und eingefrorenen Figuren bleiben erhalten. Kein DeLorean im Hof.

## Füße, Licht und Teppich

Die neuen Credits-Figuren bestimmen beim Anlegen die tatsächliche Bodenhöhe per Bodenabfrage. Figuren mit Füßen erhalten Bodenschatten und verwenden jetzt das Licht der jeweiligen Szene. Eine feste, von der Szene unabhängige Beleuchtung entfällt.

Bei den unbeweglichen Beinen bleiben die Füße am Boden: Das bisherige Kippen des ganzen Körpers und das vertikale Auf-und-ab bei Pepsiman entfallen. Die Tänze verwenden weiterhin Kopf, Arme und eine kleine Drehung, ohne starre Beine durch den Boden zu kippen. Die eigentlichen Modellbanken bleiben bytegleich; keine Gesichter oder Texturen wurden hierfür vereinfacht.

Unter **beiden** Wundererbsenverkäufern wird der schwebende Teppich lokal an deren Sitzfläche angepaßt. Die ursprüngliche Funktion berücksichtigte nur einen Verkäufer. Die kleinen Wellen laufen um die Sitzflächen herum weiter, schneiden aber nicht mehr durch die Unterkörper. Die Verkäufer selbst, ihre Weltpositionen, die Teppich-Kollision und der Händler im normalen Spiel werden hierfür nicht umgebaut. Die neue Stoffanpassung ist ausschließlich in der entsprechenden Credits-Einstellung aktiv.

Triple T, die Waldweise auf Wallace und Frankys bestehender Auftritt sind unverändert. Die ursprüngliche Krabbelminenfrau und die beiden riesigen Goronen bleiben wie in V29 aus der Feier entfernt. Keine neuen Dialoge, Inventar- oder Queständerungen.

## Prüfung

- Normal: alle sechs Ranch-Einstellungen mit ihren ursprünglichen Alterswechseln und Übergang zu den Weisen auf dem Todesberg durchlaufen. Separat die vollständige letzte Hofszene bis nach dem eingefrorenen Schlußbild.
- DEBUG: die volle Tänzer-Einstellung, Mido/Zora/Wario und der Todesberg-Übergang; separat die vollständige Hofszene.
- Tatsächlich 4 MiB RAM in allen vier Tests. Höchstens 16 von 19 Objekt-Slots, keine Überschreitung der Objektbank-Grenzen, keine unbekannten GBI-Befehle oder Vertex-Pufferfehler. Position und Bodenpolygon der neuen Gäste wurden während der Laufzeit geprüft. Die Begleiter frieren beim ursprünglichen Actor-Halt am Ende ein.
- Keine zusätzlichen Modelle, Objektbanken oder geladenen Figuren gegenüber V29. Sämtliche Objektbanken und alle drei Nachrichtenbanken sind in Normal und DEBUG bytegleich zu V29. Alle sechs Ranch-Cutscene-Daten sind bytegleich; im Hof ausschließlich die letzte Totale geändert. Der bisherige Gameplay-Code der Gäste bleibt außerhalb des privaten Credits-Abschnitts identisch.
- Beide BPS auf die saubere Basis angewendet, Ergebnis bytegleich mit dem gebauten ROM; N64-Prüfsummen geprüft. Normalquellen und Normalbuild zum Schluß wiederhergestellt.

Das sind gezielte Szenentests, kein neuer vollständiger Spieldurchlauf und keine Messung auf echter N64-Hardware.

## Aufnahmen

Die MP4s zeigen echte Emulatorbilder mit nativ aufgezeichnetem Spielton. Die 50-fps-Dateien halten ursprüngliche Spielbilder anhand der Audio-Zeitstempel; keine erfundenen Zwischenbilder. Der Szenenaufbau und die letzte Totale entsprechen der ausgelieferten ROM. Die Aufnahmen verwenden Start-Spielstände direkt in den Credits; diese sind nicht im Patch enthalten.

- `Credits_Gaeste_V30.mp4`: vollständige Ranch-Feier und Übergang zu den Weisen.
- `Marty_Doc_Credits_V30.mp4`: vollständiger letzter Hof; die gemeinsame Totale beginnt ungefähr bei Sekunde 34.
- `Fanboy_Crocker_Tanz_V30.mp4`: zwei kurze Ausschnitte aus derselben Ranch-Aufnahme, ohne Kameramanipulation, zum Prüfen der Bewegungen.
- `Credits_Mido_Rueckansicht_V30.png`: die zuvor verdeckte Rückansicht von Mido.
- `Credits_Uebersicht_V30.png`: Übersicht der geänderten Gruppen.

## Quellen

Kumulativer Quellenstand auf V29. Nach den bisherigen Buildern zuletzt ausführen:

```
python3 tools/build_credits_v29.py /pfad/zum/oot-decomp
python3 tools/build_credits_v30.py /pfad/zum/oot-decomp
```

Dann PAL-1.0 mit `COMPARE=0` bauen. DEBUG weiterhin separat mit `tools/build_debug_version.py` erstellen. Prüfskripte, Laufzeitprotokolle, Aufnahmemetadaten und Platzierungsliste liegen unter `validation/credits-v30`. Keine ROMs, Spielstände oder ausführbaren Testprogramme enthalten. Die schon gelieferten Modelle werden wiederverwendet; daraus folgt keine zusätzliche Lizenz an den Vorlagen.
