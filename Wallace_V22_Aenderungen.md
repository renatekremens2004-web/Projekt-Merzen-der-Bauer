# Wallace und Nachspiel V22

Sechs deutsche Nachrichten aktualisiert: 209D, 3041, 3042, 10B7, 10DF und 10B9. Wallace bedankt sich nach der Befreiung, erkennt seinen Gewand-Prototyp, erzählt von der erzwungenen Arbeit an Projekt Atom-Donnerblume und erklärt, warum er den Hammer entwickelte und eingesperrt wurde. Er will sich dem Drachen stellen und hat noch Gouda dabei, um die Drachendame vielleicht zu besänftigen. Das bereitet seinen späteren Weisen-Dialog vor. Der vom Nutzer gelobte Gouda/Fondue-Dialog 209E vor der Befreiung bleibt unverändert.

3041: Drache besiegt, Vater zurück – aber wo ist Wallace? 3042: Vater, Spieler und Wallace als Vorbilder. Die native Fortsetzung 3041 → 3042 bleibt erhalten.

Die diktierte ID 70B2 ist das Verkaufsangebot der Fuchs-Maske und bleibt ausdrücklich unverändert. Der Wald-Spruch gehört zum Kontext der verschwundenen Tauschquest-Person bei Fado: 10B7 mit Medizin-Vorzeigen und 10DF als normale Ansprache. Beide Zustände erzählen dieselbe neue falsche Wegbeschreibung, damit keiner mehr auf die alte Pflanzen-Verwandlungsgeschichte wechselt. 10B9 warnt vor dem Waldmonster. Die native Weiterleitung 10B7 → 10B8, die Ja/Nein-Auswahl und die Säge-Belohnung sind unverändert. Keine Questflags, Item-Übergaben, Befreiungsanimationen, Modelle oder festen Textzeiten geändert.

Geprüft: genau diese sechs deutschen Nachrichten geändert, alle anderen IDs und Sprachen bytegleich. Funktionale Textcodes identisch. PAL-Textbreiten und maximal vier Zeilen je Seite geprüft. Größte geänderte Nachricht 960/1280 Bytes; größte dekodierte Seite höchstens 142/200 Bytes. Normal und DEBUG gebaut, N64-Prüfsummen und sämtliche ROM-Segmente gegenüber V21 geprüft. Beide BPS auf die Original-ROM angewendet und bytegleich gegen die Builds verglichen. Normalausgabe wiederhergestellt. Kein neuer Emulator-Durchlauf für diese reinen Textänderungen.

Die bisherigen Arbeitslisten bis Waldtempel/Feuertempel sind auf V22 aktualisiert. Die zusätzliche neue Arbeitsliste nach Feuertempel bis Wassertempel enthält 116 IDs und 244 Textbox-Seiten, inklusive Zoras Reich, Eishöhle, Sheik, Thaddäus, Navi, neuer Begegnungen sowie optionaler See-/Labor-/Angelteich- und Tauschquest-Texte. Alle Seiten und nativen Fortsetzungen mit der aktuellen Quelle abgeglichen; drei relevante Cutscene-Quellen vollständig erfaßt. Export selbst ändert keine Texte.

Alle bisherigen Änderungen einschließlich V21 enthalten. Normal ODER DEBUG auf unveränderte europäische PAL 1.0 anwenden (MD5 e040de91a74b61e3201db0e2323f768a). DEBUG: L+R halten und Z drücken. Letzter normaler Builder: build_wallace_dialogue_v22.py nach build_fire_dialogue_v21.py; Debug optional danach.

## Tatsächlicher Wortlaut

### 209D

Seite 1: Oh, hi, lad! Wallace hier. Schön, Dich wiederzusehen! Danke, daß Du mich befreit hast. Du bist ein schlaues Bürschchen.

Seite 2: Ich sehe, Du trägst mein Outfit. Das war ursprünglich ein Prototyp, aber ich freue mich, daß er funktioniert!

Seite 3: Die letzte Zeit war schrecklich für mich. Friedrich Merz hat mich hier festgehalten und gezwungen, Tag und Nacht an Projekt Atom-Donnerblume

Seite 4: zu arbeiten.

Seite 5: Es tut mir so leid, lad. Aber hätte ich mich geweigert, hätte er diesen furchtbaren Drachen auf die unschuldigen Bewohnerinnen und

Seite 6: Bewohner Kakarikos gehetzt. Das konnte ich einfach nicht zulassen.

Seite 7: Deswegen habe ich einen besonderen Hammer entwickelt. Merz fand das heraus und sperrte mich aus Zorn in diese Zelle.

Seite 8: Bitte finde diesen Hammer. Ich selbst werde mich nun zu dem Drachen begeben und meinem Schicksal ins Auge blicken.

Seite 9: Ich habe noch ein Stück Gouda in der Tasche. Vielleicht läßt sich die Drachendame damit besänftigen. Wir treffen uns dort, lad!


### 3041

Seite 1: Du hast es geschafft, {name}! Der Drache wurde besiegt. Mein Vater ist auch zurück. Aber wo ist Wallace?


### 3042

Seite 1: Wenn ich groß bin, möchte ich genauso werden wie die großen Männer in meinem Leben, von denen ich gelernt habe.

Seite 2: Mein Vater, das mutige Oberhaupt der Goronen. Du, {name}, der mutige Junge, der uns zweimal den steinigen Arsch gerettet hat. Und

Seite 3: Wallace, ein Forscher, der sein Herz immer am rechten Fleck hatte.


### 10B7

Seite 1: Keine Sorge, ich habe dem Typen gezeigt, wie man hier aus dem Wald rauskommt. Also dem wird's schon gut gehen. Oder warte, ich glaube,

Seite 2: ich habe ihm... Oh nein. Ich habe ihm die falsche Richtung gesagt. Ach, wird schon passen.


### 10DF

Seite 1: Keine Sorge, ich habe dem Typen gezeigt, wie man hier aus dem Wald rauskommt. Also dem wird's schon gut gehen. Oder warte, ich glaube,

Seite 2: ich habe ihm... Oh nein. Ich habe ihm die falsche Richtung gesagt. Ach, wird schon passen.


### 10B9

Seite 1: Wenn Du dem Typen begegnest, dann warne ihn vor dem Waldmonster.

