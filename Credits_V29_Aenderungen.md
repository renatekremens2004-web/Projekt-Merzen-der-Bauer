# Credits V29

Alle früheren Änderungen einschließlich V28 enthalten. Normal ODER DEBUG auf eine **unveränderte europäische PAL-1.0-ROM** anwenden (MD5 `e040de91a74b61e3201db0e2323f768a`), nicht auf eine bereits gepatchte Version. Keine ROM enthalten. DEBUG-Menü weiterhin: L+R halten, Z drücken.

## Neue Auftritte

| Einstellung | Figuren |
|---|---|
| Ranch, zweite Einstellung | Skipper, Kowalski, Private, Rico und Pingu zusammen. Ohne Dynamit; kleine Kopf- und Flossenbewegungen. |
| Ranch, Händler-Einstellung | Fanboy und Chum Chum zusammen. Die **originale** Krabbelminen-Bowlingfrau entfernt; die angepaßte Waldweise bleibt erhalten. Ein zusätzlicher echter Wundererbsenverkäufer sitzt neben dem ersten auf dem fliegenden Teppich. |
| Ranch, Pferd/Malon/Zimmerleute | Alle fünf von Mystery Inc samt Mystery Machine. Locker verteilt hinter Malon, mit kleinen Bewegungen. Frankys vorhandener geklebter Credits-Auftritt bleibt an derselben Stelle. |
| Ranch, Tänzer und Gerudos | Mackey ersetzt den Krabbelminen-Ladenbetreiber in der Männerreihe; der böse Doofenshmirtz ersetzt den Angler. Beide tanzen mit den übrigen beiden Händlern. Pepsiman tanzt in der nächsten Kameraperspektive neben zwei Dosen und einer zerdrückten Dose. Crocker steht dahinter. Wawario und Wawaluigi stehen weiter hinten bei den Gerudos, mit kleinen Bewegungen. |
| Ranch, Mido und König Zora | Wario sitzt rechts neben beiden, mit gebeugten Knien, gesenkten Armen und einem kleinen Holzsitz. Nur seine Credits-Kopie wurde dafür umgeformt. |
| Letzter Hof mit junger Zelda und jungem Link | Marty und Doc stehen im Vordergrund, als hätten sie Link begleitet. Ohne DeLorean. Ihre Bewegung friert mit der ursprünglichen Schlußszene ein. |

Die beiden riesigen Credits-Goronen (5-fach und 15-fach vergrößerte Varianten) sind entfernt. Normale Goronen bleiben. Die eigene Animationsbank der kleineren Riesenvariante entfällt ebenfalls. Die eigentliche Goronen-Modellbank bleibt für die normalen Goronen nötig; das Entfernen der Riesen spart daher vor allem Zeichenaufwand und verdeckt keine Gäste mehr.

**Doppelter Wundererbsenverkäufer:** Dieser Doppelgänger-Gag ist neu. Zuvor saßen dort ein Wundererbsenhändler, der Teppichhändler und der Forscher.

Triple T und die bestehende Weisen-Szene wurden nicht umgestellt. Die Krabbelminenfrau als Waldweise bleibt erhalten. Keine neuen Dialoge, Dialogketten oder Änderungen an bisherigen NPC-Texten.

## Bewegungen

Mackey und Doofenshmirtz verwenden eine auf ihre eigenen Proportionen angepaßte Fassung der ursprünglichen 59-Frame-Händlertanzbewegung. Sie folgen dem Animationsstand des benachbarten Tränkehändlers. Körper, Kopf und Arme bleiben getrennte starre Modellteile; keine Übernahme des Anglerkörpers und keine Anglermütze.

Pepsiman bekommt einen eigenen stationären Tanz mit Körperwippen, Drehung und wechselnden Armbewegungen. Die übrigen Gäste bekommen nur leichte Bewegungen, die zu ihren Modellen passen. Wawario, Wawaluigi, die Pinguine und Pingu werden nicht in eine unpassende menschliche Tanzanimation gezwungen. Die Mystery Machine und die Dosen bleiben statisch.

## Speicher und Ablauf

Sechs neue, getrennte Objektbanken. Jede betroffene Einstellung lädt genau **eine** davon; nicht sämtliche Gäste gleichzeitig. Unbenutzte Originalbanken der entfernten Bowlingfrau und der beiden ersetzten Tänzer entfallen in ihren jeweiligen Einstellungen. Kein zusätzlicher Modellbank-Slot für den zweiten Wundererbsenverkäufer. Die bereits bestehenden Gameplay-Modelle bleiben bytegleich.

Nur die beiden besonders vollen Ranch-Credits-Einstellungen (Szenenebenen 9 und 11) erhalten 128 KiB mehr Objektbank-Platz **innerhalb der weiterhin 4 MiB Gesamtspeicher**. Die normale Farm und alle übrigen Spielgebiete behalten ihre bisherige Aufteilung. Höchstens 16 von 19 Objekt-Slots gleichzeitig belegt.

Gemessene freie Bytes in den Objektbanken der jeweiligen neuen Einstellungen:

| Einstellung | Freie Bytes |
|---|---:|
| Pinguine | 7.232 |
| Fanboy/Chum Chum/Händler | 46.624 |
| Mystery Inc | 75.680 |
| Tänzer/Pepsiman/Wawas/Crocker | 61.776 |
| Wario | 66.016 |
| Letzter Hof | 154.752 |

Das sind freie Bytes der **Objektbank**, keine Angabe zum gesamten freien RAM. Gäste außerhalb des Kamerabilds können regulär vom Spiel ausgeblendet werden. Die neuen Credits-Actors bieten keine Gespräche an, besitzen keine zusätzliche Kollision und schreiben keine Quest- oder Inventarflags.

Alle sechs ursprünglichen Ranch-Kameraszenen und die Hof-Schlußszene sind in Normal und DEBUG als Cutscene-Daten bytegleich zu V28. Die bisherigen drei Nachrichtenbanken und sämtliche bestehenden Objekt-Modelldaten sind ebenfalls bytegleich. Link läuft unverändert zu Zelda; Übergänge, Einblendungen, Musik und das ursprüngliche Einfrieren am Ende bleiben erhalten.

## Prüfung und Aufnahmen

- Normal: alle sechs Ranch-Einstellungen ohne Controller-Eingaben nacheinander abgespielt, einschließlich Alterswechseln und Übergang zur Todesberg-Weisen-Einstellung. 1.857 aufgezeichnete native Frames.
- Normal: gesamte letzte Hofszene bis nach dem Einfrieren geprüft, 740 native Frames.
- DEBUG: volle Tänzereinstellung, anschließende Mido/Zora/Wario-Einstellung und Todesberg-Übergang sowie separat die vollständige Hof-Schlußszene geprüft.
- In allen vier Tests tatsächlich **4 MiB RAM**; erwartete neue Gäste geladen, Objektbank-Grenzen eingehalten, keine unbekannten GBI-Befehle oder Vertex-Pufferfehler.
- BPS mit Flips erzeugt und mit RomPatcher.js auf die saubere Basis angewendet; Ergebnis jeweils bytegleich zum gebauten ROM. N64-Prüfsummen geprüft.

Dies sind gezielte Credits-Tests; es wurde kein neuer vollständiger Spieldurchlauf durchgeführt und keine Messung auf echter N64-Hardware vorgenommen.

Die MP4s zeigen Emulatorausgabe mit nativ aufgezeichnetem Spielton. 50-fps-Dateien halten die ursprünglichen Spielbilder anhand der Audio-Zeitstempel; es werden keine Zwischenbilder erfunden. Das hält auch Ladeübergänge synchron. Die Kameras werden für die Aufnahme nicht umgebaut. Die Testaufbauten starten direkt in den Credits; sie sind nicht Bestandteil der normalen ROM.

- `Credits_Gaeste_V29.mp4`: 116,40 Sekunden, sämtliche Ranch-Einstellungen und anschließender Todesberg-Übergang.
- `Marty_Doc_Credits_V29.mp4`: 44,48 Sekunden, vollständige letzte Hofszene einschließlich Schlußbild. Marty und Doc sind in der letzten Gesamtansicht ab ungefähr Sekunde 34 gut zu sehen.

## Quellen und Wiederaufbau

Kumulativer Quellenstand auf V28. Nach den bisherigen Buildern und `tools/build_franky_v28.py` zuletzt ausführen:

```
python3 tools/build_credits_v29.py /pfad/zum/oot-decomp
```

Dann PAL-1.0 mit `COMPARE=0` bauen. Die Tanzdaten sind bereits vorbereitet; optional lassen sie sich mit `tools/prepare_credits_v29_dance.py /pfad/zum/oot-decomp` neu aus den Original-Animationsdaten ableiten. Dafür werden NumPy und die extrahierten PAL-Assets benötigt. DEBUG wird weiterhin separat mit dem bisherigen Debug-Builder erstellt; abschließend wurden Normalquellen und Normalbuild wiederhergestellt.

Prüfskripte, Laufzeitprotokolle, Modell- und Platzierungslisten und Aufnahmemetadaten befinden sich unter `validation/credits-v29`. Keine ROMs, Spielstände oder ausführbaren Testprogramme enthalten. Die bereits gelieferten Modelle werden wiederverwendet; daraus folgt keine zusätzliche Lizenz an den Vorlagen.
