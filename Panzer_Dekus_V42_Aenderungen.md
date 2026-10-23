# V42 – begehbare Wege, Panzer und friedliche Dekus

Kumulativ auf V41. Alle bisherigen Änderungen sind enthalten. Normal- oder DEBUG-BPS auf eine saubere europäische PAL-1.0-ROM (.z64) anwenden, MD5 `e040de91a74b61e3201db0e2323f768a`.

Die drei Panzer am erwachsenen Todesberg stehen weiter am Rand. Link kann an ihnen vorbeilaufen. Beim Panzer vor Dodongos Höhle wurde auch der reguläre Übergang in den Dungeon geprüft. Panzer im normalen Spiel besitzen jetzt eine einfache feste Rumpfkollision. Der Lauf des Geschützes ist weiterhin unterquerbar. Es gibt keine Angriffe, Explosionen oder Schadenswirkung.

Drei weitere Panzer stehen auf freien Flächen in Kakariko, ausschließlich als Erwachsener, tagsüber und nachts. Sie teilen sich eine einzige Modellkopie im Raumspeicher. Damit bleibt die Zahl der Modellslots unverändert: tagsüber 19, nachts 18.

In Wawarios Zelle der Gerudo-Festung steht ein weiterer Soldaten-Gorone mit Helm und ohne Gewehr. Er bleibt stehen und kann angesprochen werden.

Die erwachsenen Verlorenen Wälder erhalten auf der Lichtung mit den beiden Händlern der Kinderzeitlinie den gelieferten grünen Panzer und drei friedliche Dekus: einen Händler, einen grünen Deku und einen roten Deku. Sie haben ihre eigenen Bewegungen, Gespräche und harmlose Körperkollision. Sie greifen nicht an und verschießen keine Kerne. Die vorhandenen Händler der Kinderzeitlinie bleiben erhalten.

Der neue grüne Panzer hat 44 Dreiecke. Verwendete Ausschnitte seiner Textur liegen in einer Objektbank mit 8.528 Bytes. Die drei Dekus benutzen die vorhandenen N64-Modelle.

## Neue Texte

- `720C`, unbewaffneter Gorone in der Zelle: „Junge, dieser Typ hier labert Zeugs, das keinen Sinn macht. Wer ist das überhaupt? Den hab ich vor 7 Jahren noch nicht gesehen!“
- `720D`, Deku-Händler: „Wir haben diesen Goronen-Pennern einen Panzer abgezockt. Wenn wir begriffen haben, wie sowas funktioniert, dann zerstören wir Philipp Amthors Villa!“
- `720E`, grüner Deku: „Einer unserer besten Männer ist zuletzt im Bauch eines Wals gesichtet worden. Was ein komischer Typ!“
- `720F`, roter Deku: „Soll ich dir meine Kerne in die Fresse rotzen? Dann mach besser 'nen Abgang. Hier sind nur Waldbewohner erlaubt. Moment, du bist ein Kokiri? Eyy Bruder, dann sag das doch. Hiermit ernenn ich dich zum Ehrendeku!“

Alle vorherigen Dialoge bleiben erhalten. Die neuen Texte haben eigene IDs und normale Seitenwechsel.

## Prüfungen

Gezielte native Tests mit 4 MiB RAM: alle vier Gespräche, die drei Todesberg-Passagen, Rumpfkollision am Todesberg, in Kakariko und im Wald, Tag/Nacht in Kakariko sowie das Ausbleiben der neuen Figuren und Panzer in der Kinderzeitlinie. Die normale Credits-Feier mit vielen Figuren und der DEBUG-Start der Credits mit anschließender Rückkehr ins normale Spiel funktionieren ebenfalls. Das ist kein vollständiger Spieldurchlauf.

Im Wald bleiben 49.088 Bytes im Objektbereich frei; in Kakariko 12.464 Bytes am Tag und 27.120 Bytes nachts. Die zusätzliche Kakariko-Modellkopie liegt im Raumspeicher und beansprucht keinen weiteren Objekt-Slot. Die Credits-Feier hat weiterhin 43.968 Bytes Reserve im Objektbereich. Vorhandene Modellbanken, Dialoge und Credits-Kameras wurden gegen V41 geprüft.

Beide ROM-Prüfsummen stimmen. Beide BPS-Dateien wurden auf die saubere Basis angewendet und bytegenau mit den geprüften Builds verglichen. Die Bilder von den Laufproben stammen aus der normalen Spielkamera. Übersichtsbilder mit „Testkamera“ im Namen nutzen ausschließlich im Aufnahmewerkzeug eine freie Kamera; die ROM-Kameras bleiben unverändert.

DEBUG: L+R halten und Z drücken. Letzter normaler Builder: `tools/build_tanks_v42.py` nach dem vollständigen V41-Stand. DEBUG anschließend separat mit `tools/build_debug_version.py` erzeugen.
