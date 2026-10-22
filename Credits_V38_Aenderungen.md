# V38 – Credits und ergänzte Feuertempel-Gespräche

Kumulativ auf V37. Beide BPS-Patches werden auf die saubere europäische PAL-1.0-ROM im .z64-Format angewendet (MD5 e040de91a74b61e3201db0e2323f768a), nicht auf eine schon gepatchte Version. Die ROM selbst ist nicht enthalten.

## Neue Dialogabschnitte

Darunia im Feuertempel (3039):

> Merz bezeichnet sich selbst als jemand, der den drei Göttinnen treu ist. Doch er militarisierte Goronia, um den Rest Hyrules unter seiner gewalttätigen Kontrolle zu halten. Meine Männer waren friedlich, und nun zwang er sie zum Dienst an der Waffe.

Der Satz mit der modernen Inquisition und der Goronen-Union ist entfernt. „Wir sehen uns!“ bleibt als Abschied erhalten.

Wallace im Feuertempel (209D):

> Das Volk der Goronen war ein friedliches, gemütliches Volk. Doch unter Merz wurden nun Soldaten ausgebildet.

Darunias Sohn (3032):

> Merz sagt, wenn ich groß bin, dann soll ich selbst zum Goronensoldaten ausgebildet werden. Der hat sie doch nicht mehr alle!

Diese Abschnitte ergänzen die vorhandenen Gespräche. Die Fortsetzung 3032 → 3033, die übrigen Texte und alle anderen Sprachen bleiben erhalten. Prüfung der kompilierten Nachrichten: maximal 1178 von 1280 Rohtext-Bytes, maximal 148 von 200 dekodierten Bytes pro Seite.

## Credits

- Vier Bauhelm-Goronen nähern sich der Aktion. Der Einweiser steht zwischen ihnen und den Trägern. Die Bombe bewegt sich auf diese Gruppe zu. Die vier Träger schauen in die Bewegungsrichtung; die Armposen berücksichtigen das unterschiedliche Bodenniveau.
- Soldaten- und Bauhelme sind schmaler und sitzen tiefer. Alle neun Goronen verwenden das vorhandene Goronen-Skelett und gemeinsam geladene Objekte.
- Okto steht im Zora-Gang und schaut zur Kamera. Seine eigenen Hauttexturen sind türkis, auch bei den bisherigen Auftritten in Jabu-Jabu und im Wassertempel. Die Texturen gewöhnlicher Oktoroks bleiben unverändert.
- Die erwachsene Ruto ist auf dem Absatz im folgenden Bereich zurückgekehrt. Ihr ursprüngliches Modell liegt in einer eigenen Objektbank; Thaddäus bleibt bei seinen bisherigen Auftritten erhalten.
- Wawario und Wawaluigi stehen sich auf einem erhöhten, mit der örtlichen Mauertextur versehenen Dachaufbau der Gerudo-Festung gegenüber. Die ursprüngliche Kamerafahrt bleibt erhalten.
- Mauzi schaut zu Beginn vom Felsen aus zur Eule und zum Mond, mit dem Rücken zur Kamera. Die Felsentextur stammt aus dem Gebiet.

Die neuen Credits-Gäste bieten keine Gespräche an, erzeugen keine Kollisionen und ändern keine Story-Flags. Die ursprünglichen Kameradaten, Übergänge und Musikbefehle bleiben unverändert. Die zusätzlichen Standflächen bestehen aus je 12 Dreiecken und werden gemeinsam mit den Figuren geladen.

## DEBUG

L+R halten und Z drücken → „Credits starten“ → A. Im Abspann funktioniert derselbe Kurzbefehl zurück ins Menü. Die normale Ausgabe enthält dieses Menü nicht.

## Quellen bauen

Auf den bestehenden V37-Stand anwenden:

1. `python3 tools/build_fire_additions_v38.py /pfad/zu/oot`
2. `python3 tools/build_credits_v38.py /pfad/zu/oot`
3. Normal mit `VERSION=pal-1.0 COMPARE=0 PYTHON=python3 rom compress` bauen.
4. Für eine separate DEBUG-Ausgabe anschließend `build_debug_version.py` anwenden; nach dem DEBUG-Build mit `--restore` zurücksetzen und die normale Ausgabe erneut bauen.

`DEBUG_FEATURES` bleibt in beiden Ausgaben 0. Prüfskripte, Protokolle und Versionsprüfsummen liegen unter `validation/credits-v38` beziehungsweise `validation/fire-additions-v38`.
