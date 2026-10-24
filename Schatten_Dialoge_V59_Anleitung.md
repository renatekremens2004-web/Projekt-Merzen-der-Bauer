# Brunnen, Schattentempel und Kakariko – Dialoge V59

V59 enthält alle bisherigen Änderungen einschließlich der Wassertexte aus V58. Die eingefügte Textdatei ist in 42 deutschen Text-IDs umgesetzt.

## Neue Texte und Seitenumbrüche

Sheik erklärt den Dämon im Brunnen, Mr. Beans Schutz des Dorfes und die Schwächung des Siegels durch Friedrich Merz. Die beanstandeten Umbrüche bei 5031 und 5033 sind korrigiert: „Davon hast Du ja sogar geträumt“ steht gemeinsam auf Seite 2; beim Windmühlenmann beginnt „Wenn ich nicht genug Kram mühle …“ auf Seite 2. Andere Seiten von Sheiks Rede bleiben wortgleich erhalten.

Der neue Zusatz zum Auge der Wahrheit folgt auf dessen unveränderte Fund- und Bedienseiten. Die Gleitstiefel erklären Steuerkreuz oben und das Rutschen. Ihre beiden Item-Symbole bleiben erhalten. Bei neu umgebrochenen Absätzen werden einzelne Restwörter nach Möglichkeit nicht allein auf die nächste Seite gesetzt.

Mr. Beans neue Sätze sind auf Englisch eingebaut: Nackenbruch am Ast, Staubsaugen im Schattentempel, sein geparktes Auto, Merz, der lila Schattentempelteller und die Einladung zum Wiederbesuch. Die festen Ausblendzeiten seiner Verabschiedung bleiben erhalten.

Die neuen Texte für Mr. Mackey, die weiteren Bewohner Kakarikos, Hühnerfrau, Mario und sein Date, Schleimhexe sowie Salia sind ebenfalls eingebaut. 016D bleibt unverändert. Erst-, Wiederholungs- und Questvarianten behalten ihre bisherigen Bedingungen.

## Zuordnung der versprochenen IDs

- Der Warnruf „Bleib zurück“ gehört zu **501B**; im Diktat stand 051B.
- Der Herzteile-Kommentar gehört zu **5030**. **5036** ist der andere Text der Hühnerfrau und bleibt erhalten.
- Bongo Bongos tatsächlicher Navi-Text ist **0629**. In der vorigen Kapitelabschrift war 0624 falsch als Bongo Bongo beschriftet. Dein neuer Trommel-/Telefon-Dialog steht jetzt bei 0629; 0624 bleibt die Beschreibung des Roten Todes.
- Marios Rückkehr zur Farm gehört zu **508D**; die Schlaf-/Herz-Zeile bleibt bei **508C**.

## Kapitelabschriften

Die aktualisierte Brunnen-/Schattenliste enthält alle 153 Textzustände mit den neuen Seiten. Die anschließende Liste vom Schattentempel bis Ende Geistertempel enthält 173 Textzustände, einschließlich Gerudos, Handwerker, Rennläufer, Wüste, Waluigi, Hexen, zusätzlichen Figuren und bedingten Rückbezügen. Die Geistertempeltexte werden durch diesen Export nicht umgeschrieben.

## Patchen und DEBUG

Genau einen BPS-Patch auf eine saubere europäische PAL-1.0-ROM anwenden. Basis-MD5: `e040de91a74b61e3201db0e2323f768a`. Nicht auf eine bereits gepatchte Fassung anwenden. Alle bisherigen Änderungen sind enthalten; kein ROM-Abbild im Paket.

DEBUG bleibt erreichbar über **L+R halten und Z drücken**. „Alle Items“, Standard-/Licht-/Schattengewand und die Credits-Option bleiben vorhanden. Steuerkreuz unten wechselt Eisenstiefel, Steuerkreuz oben Gleitstiefel.

## Prüfungen und Quellen

Alle 42 geänderten Texte wurden nach dem Kompilieren gegen die tatsächlichen Textpuffer geprüft: größter Rohtext 944 von 1.280 Bytes, größte dekodierte Seite konservativ höchstens 146 von 200 Bytes. Auswahl-, EVENT-, Item-Symbol-, Fortsetzungs- und Ausblendcodes bleiben erhalten. Andere Sprachen und nicht beauftragte Text-IDs bleiben unverändert.

Die Modelle, Räume, Szenen, Musik und vorhandenen Actor-Overlays wurden gegen V58 verglichen; auch die ausführbaren Hauptprogramm-Instruktionen bleiben unverändert. Die Credits-Kameras werden nicht bearbeitet. Normal- und DEBUG-Patches werden unabhängig angewendet und bytegenau mit den Builds verglichen. Nach dem DEBUG-Bau werden die Produktionsquellen wiederhergestellt und die normale Fassung erneut identisch gebaut.

Native Emulatorprüfungen laufen mit 4 MiB: Mr. Beans vollständige Halle-der-Weisen-Sequenz einschließlich Amulett, zeitgesteuertem Abschied und Rückkehr; außerdem Erhalt der Gleitstiefel aus der normalen Truhe, alle drei neuen Textseiten und anschließendes Umschalten per Steuerkreuz oben. Die Testvorrichtung setzt Startposition und vorherige Fortschrittsflags direkt, unter anderem den bereits besiegten Raumgegner für die Truhe. Kein vollständiger neuer Spieldurchlauf.

Nach dem vollständigen V58-Stand: `python3 tools/build_shadow_dialogue_v59.py /pfad/oot`. Für eine separate DEBUG-Ausgabe anschließend den optionalen letzten Builder `build_debug_version.py` verwenden. Die Vorgaben stehen in `tools/shadow_dialogue_v59.json`, die Ergebnisse im Ordner `validation/shadow-dialogue-v59`.
