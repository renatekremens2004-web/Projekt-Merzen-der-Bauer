# V43 – Harkinian, Moseby und der Fahrgast auf der Geisterfähre

Alle Änderungen bis V42 bleiben enthalten. Beide BPS-Patches direkt auf die saubere europäische PAL-1.0-ROM anwenden, nicht auf einen früheren Patchstand. Basis-MD5: `e040de91a74b61e3201db0e2323f768a`. Keine ROM im Downloadpaket.

## Figuren und Endkampf

- **King Harkinian** steht in der Kindheits-Fensterszene Merz gegenüber. Leichte Drehung zur Kamera, Kopf- und Armgesten. Nur der König aus dem gelieferten Sammelmodell wird verwendet. Die normale Zelda-Szene einschließlich Fensterkameras, Merz' Kniefall und Blick zum Fenster bleibt erhalten. Der vollständige Burns in der Kindheit bleibt unverändert.
- **Marion Moseby** steht nur als Erwachsener am Hylia-See, auf der festen Uferfläche in der Nähe des Labors. Größe 76 Spieleinheiten, gesenkte Arme, Kopf- und Sprechgesten. Seine ursprünglichen DS-Texturen und Vertexfarben werden gemeinsam dargestellt.
- **Friedliches Skelett** auf der Geisterfähre im Schattentempel. Es spricht über A, nickt und bewegt seine Arme. Keine Gegner-KI und keine Angriffskollision. Es folgt der tatsächlichen Schiffsposition einschließlich der Höhenbewegung; Triforce, ursprüngliche Gegner und Ausstieg bleiben frei.
- **Triangle Guy** hält während der Verwandlung beide Hände vor den Mund. Zwei zusätzliche starre Unterarmteile ermöglichen angewinkelte Ellbogen; keine gedehnten Hände. Die normalen Gesten und bisherigen Texte bleiben erhalten.
- Der deutsche Boss-Schriftzug **„Ganon“ heißt „Merz“**. Gleiche Texturabmessungen und Einblendungsdauer; Englisch und Französisch bleiben unverändert.
- **Kaputter Franky** liegt nun nahe Links Anfangsposition, innerhalb des Feuerrings. Sein Gespräch ist nach der Verwandlung erreichbar. Andere Franky-Auftritte, Credits und Texte bleiben erhalten.

## Kämpfe

- **Kokiri-Schwert:** doppelter positiver Schaden bei Schlag, Wirbel- und Sprungattacke. Gegnerische Immunitäten und reine Betäubung bleiben bestehen. Die bisherige Masterschwert-Verstärkung bleibt erhalten. Auch die allgemeine Schwert-Schadensabfrage für Bosse berücksichtigt die Verdopplung.
- **Wallmaster:** Die von der Decke kommenden Hände werden in ihrer Initialisierung entfernt. Ihr noch nicht eingerichteter Destruktor wird abgeschaltet. Aufrufer bekommen weiterhin eine gültige Actor-Instanz, die regulär entfernt wird. Floormaster bleiben bestehen.
- **Sonnenrätsel in Friedrichs Schloß:** Die drei falschen Sonnen dürfen ihre ursprünglichen Auslöser setzen und verschwinden; nur die Bestrafungshände fehlen. Die richtige Sonne und ihr eigener Schalter sind unverändert.
- **Kleine Quallen/Biri:** kein elektrischer Gegenschlag mehr beim Waffentreffer und kein elektrisches Nachspiel eines Schwerttreffers. Schwert, Deku-Stab, Bomben, Bumerang, Pfeile, Hammer, Fanghaken und jetzt auch die Schleuder können sie töten. Deku-Nüsse betäuben weiterhin. Direkter Körperkontakt bleibt gefährlich. Große Quallen und Barinade sind unverändert.

## Neue Texte

**Moseby, 7210:**

> Gestatten, Marion Moseby. Ich arbeite in einem berühmten Fünf-Sterne-Hotel. Vielleicht ist es selbst jemandem wie Ihnen ein Begriff. Wenn ich endlich ein paar Minuten frei habe, spaziere ich am Hylia-See, um den Kopf freizubekommen. Mein Beruf wäre durchaus angenehm, wären da nicht diese beiden Zwillinge, die mich Tag für Tag in den Wahnsinn treiben. Hier herrscht wenigstens Ruhe. Und ich muß niemandem zum hundertsten Mal erklären, daß man in einer Lobby nicht rennt!

**Skelett, 7211:**

> RATTLE ME BONES!! WELCOME ABOARD MATEY!

## Prüfung und Vorschauen

Gezielte native Tests mit **4 MiB**: regulärer Zelda-Dialog bis zur Fensterszene; Moseby-Gespräch und Ausschluß als Kind; Skelett-Gespräch und Mitfahrt; Verwandlung, Schreckpose und Franky-Gespräch; alle drei falschen Sonnen, danach die richtige Sonne; tödlicher Schwert- und Schleudertreffer auf Biri ohne Gegenschaden; Schwert-Schadensberechnung einschließlich unverändertem Masterschwert; volle Credits-Feier; DEBUG-Menü mit Credits-Start und Rückkehr.

405 bisherige Modellbänke sind bis auf die deutsche Bossnamen-Zeile identisch, abgesehen von technisch neu adressierten Identitätsmatrizen. Die neun Credits-Kameraskripte und beide Fensterszene-Skripte sind bytegleich. Alle bisherigen Dialoge bleiben unverändert. Neue Dialogpuffer und beide BPS-Rückanwendungen werden geprüft. Kein vollständiger Spieldurchlauf in dieser Version.

Die Fensterszene, Mosebys Gespräch und Frankys Position werden mit Spielkameras gezeigt. Skelett und Triangle Guys Schreckpose haben zur Sichtprüfung eine **freie Testkamera**, die nicht im Patch enthalten ist. Bei der Schreckpose ist der Boss für das Testfoto kurz angehalten; die eigentliche Verwandlung wurde zusätzlich mit ihrer normalen Kamera durchlaufen.

Die neuen Figuren sind raumgebunden. Keine zusätzlichen Objektbänke oder Objektplätze: Harkinian 480, Moseby 262, Skelett 1004 Dreiecke; vier starre Matrizen pro Figur. Triangle Guy benötigt zwei zusätzliche Matrizen, insgesamt 128 Byte mehr pro Zeichnung. DEBUG: **L+R halten, Z drücken**; „Credits starten“ bleibt der erste Menüeintrag.

Letzter kumulativer Builder: `tools/build_characters_v43.py` nach dem vollständigen V42-Stand. Für den Build werden die fertigen Modell-JSONs und Texturen mitgeliefert; erneuter FBX-Import ist nicht nötig.
