# Credits und zweiter Erbsenhändler V31

Alle bisherigen Änderungen einschließlich V30 enthalten. Normal **oder** DEBUG auf eine **unveränderte europäische PAL-1.0-ROM** anwenden, MD5 `e040de91a74b61e3201db0e2323f768a`. Nicht auf eine schon gepatchte ROM. Keine ROM enthalten. DEBUG-Menü wie bisher: L+R halten, Z drücken.

## Änderungen

- **Crocker und Fanboy:** volle Stärke derselben 59-Frame-Tanzvorlage, die bereits Mackey und Doofenshmirtz verwenden. Keine abgeschwächte Variante mehr. Die Arm- und Kopfdrehungen werden um die eigenen Drehpunkte der Modelle ausgeführt; unbewegliche Beine bleiben auf dem Boden.
- **Fanboy und Chum Chum:** die Plätze und Blickrichtungen getauscht. Fanboy steht vorne auf Chum Chums bisherigem Platz; Chum Chum steht weiter hinten auf Fanboys bisherigem Platz. Größen wie in V30.
- **Wawario und Wawaluigi:** deutlich schnellere, wechselnde Armbewegungen nach vorne/hinten und seitlich. Die übrige Positionierung und Größen bleiben erhalten. Der echte, sitzende **Wario bleibt unverändert**, entsprechend der Klarstellung.
- **Vierer-Tanzreihe:** nur die erste Kamera dieser Einstellung von 60 auf 56 Grad Blickwinkel verengt, also etwas näher. Kamerafahrt, Blickziel und Zeitpunkte bleiben erhalten. Die späteren Perspektiven dieser Einstellung werden nicht vergrößert.
- **Pepsi-Müll:** sechs kleine Dosen rund um Pepsiman, darunter drei seitlich liegende und zwei zerdrückte Dosen. Die liegenden Dosen liegen mit ihrer Unterseite auf dem Boden. Vorhandene Modelle wiederverwendet, keine zusätzlichen Texturen und keine neue Modellbank für die Dosen.
- **Deku-Händler:** steht bei Pepsiman, Crocker und der Hühnerfrau. Er verwendet sein ursprüngliches vollständiges Skelett und die Bewegung aus seiner Händlerphase. Dazu kommen auf seine eigenen Arm- und Blattgelenke angepaßte Tanzbewegungen. Er verkauft in den Credits nichts, greift nicht an und schreibt keine Questflags.
- **Zweiter Erbsenhändler am Zora-Fluß:** steht als Kind schräg neben dem ursprünglichen Händler, auf derselben zugänglichen Uferseite. Bodenhöhe einschließlich Sitzfläche geprüft. Die normale Eßanimation bleibt erhalten. Sein neuer Text besteht aus zwei manuell weitergeschalteten Seiten:

> Ja, ich bin der andere Erbsenhändler. Aber ich konnte gar keine Erbsen mehr kaufen, weil die schon alle aufgekauft wurden.
>
> Und ich esse gerade auch keine Erbsen. Was ich hier im Beutel habe und mir in den Mund stopfe, sind tatsächlich Chips.

Der zusätzliche Händler hat **keine Kaufoption** und verändert weder Rubine noch Erbsenbestand noch Preise. Der ursprüngliche Händler bleibt weiterhin der Verkäufer. Der zusätzliche NPC erscheint tagsüber und nachts als Kind; als Erwachsener ist er weg. Keine zweite Modellbank nötig, beide nutzen die bereits vorhandene native Händlerbank.

Die Teppich-Anpassung für die beiden Credits-Erbsenhändler bleibt exakt wie in V30. Franky, Triple T, die Weisen, Wario bei Mido und der letzte Hof mit Doc und Marty bleiben unverändert. Es wurde kein anderer bestehender Dialog umgeschrieben.

## Speicher und Prüfung

Eine zusätzliche vorhandene Bank (`object_shopnuts`, 17.808 Bytes) nur in der betroffenen Ranch-Credits-Einstellung. Dort 12 Objekt-Slots belegt und weiterhin **43.968 freie Bytes im Objektbereich**. Keine weitere Vergrößerung des Objektbereichs. Das ist keine Angabe zum insgesamt freien RAM. Sämtliche bisherigen Modellbanken sind bytegleich zu V30.

- Normal: komplette Ranch-Feier mit allen Alterswechseln bis zur Todesberg-Einstellung sowie separat die vollständige Hof-Schlußszene durchlaufen.
- DEBUG: vollständige betroffene Tanz-Einstellung, anschließend Wario/Mido/Zora und Todesberg; separat der gesamte Schlußhof.
- Tatsächlich **4 MiB RAM** in allen Tests. Keine Objektbank-Überläufe, unbekannten GBI-Befehle oder Vertex-Pufferfehler. Bodenkontakte einschließlich liegender Dosen und Deku-Händler geprüft. Das ursprüngliche Einfrieren am Ende funktioniert weiterhin.
- Zusätzlicher Erbsenhändler zweimal hintereinander angesprochen und beide Seiten geschlossen: weiterhin 99 Rubine, unveränderter Erbsenzähler. Ebenso nachts mit bereits zehn gekauften Erbsen getestet.
- Ursprünglicher Händler: erste Erbse regulär gekauft, 99 → 89 Rubine, Bestand und Kaufzähler jeweils 0 → 1. Anschließender Preistext korrekt die nächste Stufe. Keine Änderung an seiner Preis- oder Verkaufslogik.
- Als Erwachsener kein zusätzlicher Erbsenhändler geladen.
- Jeder bestehende kompilierte Text in allen drei PAL-Sprachen bytegleich geprüft. Einzige neue Nachricht: `71EC`. Zeilenbreite, Seiten und Puffergrößen geprüft. Keine automatischen Folgetexte oder Kaufantworten im neuen Dialog.
- BPS auf die saubere Basis angewendet; Ergebnis bytegleich mit den gebauten ROMs. N64-Prüfsummen geprüft. Abschließend Normalquellen und Normalbuild wiederhergestellt.

Das sind gezielte Prüfungen, kein neuer vollständiger Spieldurchlauf und kein Test auf echter N64-Hardware.

## Aufnahmen

- `Credits_Tanzupdate_V31.mp4`: kurze Ausschnitte von Fanboy, der näheren Viererreihe, Crocker/Pepsiman/Deku-Händler und den Wawas. Mit nativem Spielton, ohne Kameramanipulation für die Aufnahme.
- `Credits_Gaeste_V31.mp4`: komplette Ranch-Feier und Übergang zu den Weisen, ebenfalls mit Spielton.
- `Anderer_Erbsenhaendler_V31.png` und `Erbsenhaendler_Chips_V31.png`: beide Dialogseiten des neuen Händlers aus dem fertigen Build.

Die Credits-Aufnahme entstand vor der abschließenden Verschiebung des neuen Händlers auf die andere Seite des Zauns am Zora-Fluß. **Ausschließlich `spot03_room_0` unterscheidet sich danach**: sämtliche aufgenommenen Szenen, Modelle und der gesamte ausführbare Code sind bytegleich zum finalen Build. Dieser Vergleich ist in `validation/credits-v31/verification.json` dokumentiert. Die Fluss-Tests und Bilder stammen aus dem finalen Build.

Die 50-fps-MP4s halten die ursprünglichen Emulatorbilder anhand der aufgezeichneten Audio-Zeitstempel. Keine erfundenen Zwischenbilder. Die Test-Spielstände starten direkt in der jeweiligen Szene und sind nicht im Patch enthalten.

## Quellen und Wiederaufbau

Kumulativer Quellenstand auf V30. Nach den bisherigen Buildern zuletzt:

```
python3 tools/build_credits_v29.py /pfad/zum/oot-decomp
python3 tools/build_credits_v30.py /pfad/zum/oot-decomp
python3 tools/build_credits_v31.py /pfad/zum/oot-decomp
```

Dann PAL-1.0 mit `COMPARE=0` bauen. DEBUG wie bisher separat mit `tools/build_debug_version.py`. Platzierungsdaten, neue Dialogquelle und native Deku-Tanzanpassung liegen unter `tools` und `story`; Prüfskripte und Laufzeitprotokolle unter `validation/credits-v31`. Keine ROMs, Spielstände oder ausführbaren Testprogramme enthalten. Wiederverwendete Modelle begründen keine zusätzliche Lizenz an den Vorlagen.
