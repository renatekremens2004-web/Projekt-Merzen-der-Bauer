# V40 – Panzer, Grenz-Soldaten und ursprüngliche Credits-Kamera

Kumulativ auf V39. Beide BPS-Patches auf die saubere europäische PAL-1.0-ROM im .z64-Format anwenden, MD5 `e040de91a74b61e3201db0e2323f768a`. Alle bisherigen Änderungen sind enthalten. Die ROM selbst ist nicht enthalten.

## Credits-Korrektur

Die originale Kamerafahrt der Gerudo-Festung ist vollständig wiederhergestellt und im kompilierten Spiel bytegleich mit V38. Wawario steht links, Wawaluigi rechts auf dem vorhandenen mittleren Dach. Beide behalten ihre kleine Größe. Das Vordergrundgeländer bleibt erhalten und darf sie zeitweise verdecken.

Mauzi steht weiterhin auf dem Erdboden. Ein einzelner verlassener Panzer steht auf der entfernten Seite des Tals; Mauzi schaut in seine Richtung. Die Kamera bleibt auch in diesem Shot unverändert. Das MP4 enthält die originale Credits-Musik und Spielgeräusche.

## Panzer und Soldaten

- Drei Panzer an verschiedenen Stellen des erwachsenen Todesbergs: am unteren Pfad, bei Dodongos Höhle und an der breiteren Stelle weiter oben am Pfad. Vor Goronias Eingang bleibt Platz.
- Zwei Panzer und drei bewaffnete Goronen auf der östlichen Seite des Gerudotals, auf der Seite ohne Zelt.
- Zwei Panzer und drei bewaffnete Goronen vor dem Gerudotal-Eingang im Hyrule-Feld.
- Ein einzelner Panzer im ausdrücklich gewünschten Mauzi-Credits-Shot.

Die neuen Begegnungen in den normalen Gebieten erscheinen ausschließlich als Erwachsener. Die Panzer sind unbewegliche Kulissen ohne Kampfverhalten, Explosionen oder neue Kollisionswände. Die Soldaten verwenden die bestehende stehende Wachpose und rollen sich nicht zusammen. Ihre Armeehelme sitzen 1,2 Spieleinheiten tiefer; das gilt auch für die entsprechenden Helme der Credits-Goronen.

Das gelieferte PZ4-J-Modell hat 282 Dreiecke. Alle Panzer teilen sich eine Objektbank mit 14.672 Bytes. Die sechs zusätzlichen Soldaten teilen sich die vorhandenen Goronen-, Helm- und Gewehrdaten.

## Neue Gespräche

Gerudotal, Seite ohne Zelt:

**7206:** Diese Gerudo-Kriegerinnen haben die Brücke gekappt. Was soll sowas?? Ach, Moment mal, wir sind ja die Invasoren... Dann ist's vielleicht doch gar nicht mal so unberechtigt.

**7207:** Merz hat uns den Auftrag gegeben, an der Grenze zum Gerudotal eine Militärübung durchzuführen. Ich wußte nicht, daß wir den Auftrag zum Angriff bekommen würden.

**7208:** Ich will wieder zum Todesberg zurück und mies Steine fressen!

Hyrule-Feld am Gerudotal-Eingang:

**7209:** Wir haben klare Anordnungen, auf die ich ganz klar keinen Bock hab.

**720A:** Bis zur nächsten Woche haben wir das Ding hier erobert!

**720B:** Ich hasse Rock Music. Sie geht mir auf den Goronen-Sack!

Die sechs Nachrichten belegen neue IDs. Kein bestehender Dialog wurde überschrieben. Der aktualisierte vollständige Kapitel-Export enthält 166 IDs mit Seiten und Antwortzweigen: `Storydialoge_Gerudotal_Wueste_Geistertempel.md` beziehungsweise `.txt`.

## Prüfung

Gezielte native Emulator-Tests mit 4 MiB: alle sechs neuen Gespräche, Gerudotal nachts, Ausschluß der neuen Figuren in den drei Kind-Gebieten, Darstellung der Panzer, Credits mit Originalmusik sowie DEBUG-Credits-Start und Rückkehr ins Spiel. Kein vollständiger Spieldurchlauf.

Das Gerudotal nutzt 18 Objektplätze und hat in den geprüften Erwachsenen-Szenen noch 8.944 Bytes im Objektbereich frei. Der Todesberg nutzt 19 Plätze und hat dort noch 165.888 Bytes frei. Die übrigen Charakter-Geometrien und Texturen bleiben erhalten; erforderliche echte Linker-Adreßanpassungen wurden gesondert geprüft. In den beiden bestehenden Helm-Banken wurden ausschließlich die Helm-Vertexhöhen geändert. Die Kind-Actor- und Objektlisten sind für Tag und Nacht bytegleich mit V39. Beide BPS-Patches werden zusätzlich mit RomPatcher.js auf die saubere ROM angewendet und mit den geprüften ROM-Dateien verglichen.

Die letzte kosmetische Anpassung versetzte nur den dritten Erwachsenen-Panzer am Todesberg. Die unveränderten übrigen Segmente und die native Credits-Kamera wurden binär geprüft; die neue Todesberg-Position wurde anschließend im Emulator angesehen.

## DEBUG und Quellen

DEBUG: L+R halten und Z drücken. „Credits starten“ mit A auswählen. Derselbe Kurzbefehl öffnet aus dem Abspann erneut das Menü.

Nach dem vollständigen V39-Stand:

1. `python3 tools/build_credits_roof_v40.py /pfad/zu/oot`
2. `python3 tools/build_tanks_v40.py /pfad/zu/oot`
3. Mit `VERSION=pal-1.0 COMPARE=0 PYTHON=python3 rom compress` bauen.
4. Für die separate DEBUG-Ausgabe `build_debug_version.py` zuletzt anwenden und erneut bauen. Anschließend mit `--restore` zurücksetzen und die normale Ausgabe erneut bauen.

Quellen, Modelldaten, Text-JSON, Prüfskripte und Protokolle liegen im kumulativen Quellen-ZIP unter `tools`, `models`, `story` und `validation/tanks-v40`.
