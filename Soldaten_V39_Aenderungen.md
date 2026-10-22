# V39 – Goronen-Soldaten und Credits-Platzierung

Kumulativ auf V38: Alle bisherigen Änderungen sind enthalten. Beide BPS-Patches auf die **saubere europäische PAL-1.0-ROM im .z64-Format** anwenden (MD5 `e040de91a74b61e3201db0e2323f768a`), nicht auf eine bereits gepatchte Version. Die ROM selbst ist nicht enthalten.

## Die sieben Soldaten

Sie erscheinen ausschließlich als erwachsener Link. Jeder trägt einen Soldatenhelm und das gelieferte Gewehr. Die Goronen stehen dauerhaft, blinzeln, atmen leicht und schauen Link an. Sie rollen sich nicht zusammen. Die Gewehre sind sichtbare Ausrüstung ohne Schussfunktion. Die normalen Goronen und die Goronen in den Credits behalten ihr bisheriges Verhalten.

| Standort | Anzahl | Text-ID |
|---|---:|---|
| Vor dem Eingang von Goronia auf dem Todesberg | 2 | 7202, 7203 |
| Neben der Bombe in Goronia | 1 | 7201 |
| Am Todesberg-Tor in Kakariko | 2 | 7200 |
| Im Dorf Kakariko | 1 | 7205 |
| In den Verlorenen Wäldern, abseits des ersten Raums | 1 | 7204 |

7200:

> Halt! Stehenbleiben. Wer bist Du? Was? Du bist [Spielername]? Nun gut, Darunia wies uns an, Dich durchzulassen.

7201:

> Erzähle niemandem, was Du hier gesehen hast. Goronias Projekte sind strengstens geheim und gehen den Rest von Hyrule nichts an!

7202:

> Was ist der Grund für Deinen Aufenthalt in Goronia? Du möchtest mit Darunia sprechen? Bist Du etwa [Spielername]?

7203:

> Ich fürchte, mit Wallace wirst Du aktuell nicht sprechen können. Er wurde zum Feuertempel geschickt. Ein Ort, den man nicht einfach so leicht verlassen kann. Zumindest nicht bis Schichtende!

7204:

> Man schickte mich hierher, um Philipp Amthor als Security zu dienen. Aber irgendwie hab ich mich verlaufen. Mann, ah fuck, Mist, Scheiße! Ich bin ein schlechter Bodyguard.

7205:

> Hallo, Zivilist. Sei unbesorgt, Kakariko steht unter dem Schutz von Goronia!

Die sechs Nachrichten sind neu und ersetzen keinen vorhandenen Text. Die beiden Wachen am Kakariko-Tor teilen sich ihren eigenen Text. Die vorherigen Ergänzungen für Darunia, Wallace und Darunias Sohn sind weiterhin enthalten.

## Credits

- Wawario und Wawaluigi stehen sich auf einem vorhandenen Dach der Gerudo-Festung gegenüber. Der zusätzliche Dachaufbau aus V38 ist entfernt.
- Die Kamera fährt außerhalb des Vordergrundgeländers, damit beide sichtbar sind. Ablauf, Dauer, Schrift, Musik und Übergänge bleiben erhalten.
- Mauzi steht zu Beginn auf dem tatsächlichen Erdboden und schaut zur Eule und zum Mond. Der zusätzliche Felsen ist entfernt.

Das MP4 enthält die ursprüngliche Credits-Musik und Spielgeräusche.

## Prüfung und Speicher

Normal und DEBUG wurden in gezielten Emulator-Szenarien mit **4 MiB RAM** geprüft: alle sieben Gespräche, stehende Positionen auf dem Boden, Kakariko tagsüber und nachts, Kind-Kakariko und Kind-Todesberg ohne neue Soldaten sowie die natürliche Credits-Kette über das DEBUG-Menü mit anschließender Rückkehr ins Spiel. Das ist kein vollständiger Durchlauf des Spiels.

Die Soldaten teilen sich das vorhandene Goronen-Modell. Die neue gemeinsame Objektbank für Helm und Gewehr belegt 11.424 Bytes; das Gewehr hat 136 Dreiecke. In den geprüften Szenen bleiben die Objektbank-Grenzen eingehalten. Kakariko tagsüber nutzt alle 19 Objektplätze und hat noch 12.464 Bytes in seinem Objektbereich frei; dort sollten keine weiteren Objektbanken ergänzt werden.

Vorhandene Charakter-Objektbanken bleiben bytegleich. Aus der Credits-Bank wurden lediglich die beiden zusätzlichen Unterbauten entfernt. Die sechs neuen Texte passen in die nativen Textpuffer. Beide BPS-Patches wurden mit RomPatcher.js erneut auf die saubere ROM angewendet; das Ergebnis entspricht jeweils bytegenau der geprüften ROM.

## DEBUG und Quellen

L+R halten und Z drücken → „Credits starten“ → A. Im Abspann öffnet derselbe Kurzbefehl wieder das Menü. Die normale Ausgabe enthält dieses Menü nicht.

Auf den vollständigen V38-Quellstand anwenden:

1. `python3 tools/build_goron_soldiers_v39.py /pfad/zu/oot`
2. Mit `VERSION=pal-1.0 COMPARE=0 PYTHON=python3 rom compress` bauen.
3. Für die separate DEBUG-Ausgabe anschließend `build_debug_version.py` anwenden und erneut bauen.
4. Nach dem DEBUG-Build `build_debug_version.py /pfad/zu/oot --restore` ausführen und die normale Ausgabe erneut bauen.

Die Modell-Zwischendaten, Textdatei, Quellsicherungen, Prüfskripte und Protokolle liegen im kumulativen Quellen-ZIP. `DEBUG_FEATURES` bleibt in beiden Ausgaben 0.
