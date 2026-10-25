# V70 – Kokiri, gelber Poe und Medaillon

Stand: 25. Oktober 2026. Kumulativer PAL-1.0-Patch einschließlich sämtlicher V68-Ladekorrekturen. V69 wurde nicht separat veröffentlicht; dessen Änderungen sind hier enthalten.

[DEBUG-Patch](Mr_Burns_Mr_Bean_DE_PAL10_DEBUG_Kokiri_Poe_Medaillon_V70.bps?raw=true) · [Normaler Patch](Mr_Burns_Mr_Bean_DE_PAL10_Kokiri_Poe_Medaillon_V70.bps?raw=true) · [Quellen](Merzen_Kokiri_Poe_Medaillon_V70_Quellen_Patch.zip?raw=true)

## Medaillon im Königsgrab

Das hochgeladene Medaillon liegt mit dem Gesicht nach oben auf dem Boden vor der Inschrift im Raum, in dem Link das Sonnenlied lernt. Navi sagt beim Anvisieren und C-oben: **„Fass es bloß nicht an!“**

Das Ausgangsmodell wurde von 2.808 auf 320 Dreiecke reduziert. Zusammenfallende Eckpunkte werden vor der Reduktion verbunden, damit die Oberfläche geschlossen bleibt. Es ist etwa zwölf Spieleinheiten breit und nutzt eine 64×64-CI4-Textur. Das Modell liegt ausschließlich im Modellpaket dieses Grabraums. Ein kleines, eigenes Prop-Overlay (Actor 0161) stellt den Navi-Hinweis bereit. Es hat keine Kollision, kein Item und keine Belohnungslogik. Das Sonnenlied und die Inschrift bleiben unverändert.

## Fünfter Poe im Waldtempel

Ein friedlicher, knallgelber Poe schwebt abseits der vier ursprünglichen Fackeln am Rand des zentralen Aufzugraums. Seine zusätzliche goldene Fackel brennt dauerhaft gelb. Er sagt genau:

> Ähm, Leute? Ich hab das Gefühl meine Fackel ist jetzt nicht so wirklich mit dem Aufzug verbunden! Ich möchte mich ja nicht aufdrängen, aber warum ist gerade meine Fackel so weit von euren entfernt?

Beide verwenden ein eigenes kleines Overlay (Actor 0154) und bereits geladene Modelle. Die vier ursprünglichen Fackeln, ihre Schalter, die Geisterkämpfe und der Aufzug bleiben unverändert. Der neue Poe gehört zur NPC-Kategorie; er greift nicht an, wird nicht als zu besiegender Gegner gezählt und schreibt keine Rätsel- oder Raumabschlussflags.

## Neuer Kokiri und Beta-Soldat

Der blonde Kokiri mit mintfarbener Mütze steht auch in der erwachsenen Zeitlinie im Kokiri-Wald. Sein Wiedererkennungsdialog enthält den Spielernamen und endet mit „Right on Link!“. Der ursprüngliche Beschleunigungszauber für den jungen Link bleibt unverändert.

In der Feier der Credits übernimmt er den Körper und die vorhandene Tanzanimation eines Kokiri. Es wird dafür kein zusätzlicher Tänzer geladen. Zusätzlich steht er in der ursprünglichen Kamerafahrt durch den Kokiri-Wald auf dem vorhandenen Vorsprung beim Laden. Die Kamerafahrten bleiben unverändert.

[15 Sekunden Tanzvorschau mit Abschlussmusik](Kokiri_Tanz_Credits_V70.mp4?raw=true): Für die Detailvorschau wurde nur im Test die Kamera näher gesetzt und die originale Credits-Musik gestartet. Der Patch verändert weder Credits-Kamera noch Credits-Musik.

Die Pistole des Beta-Goronen-Soldaten ist um seinen Handgriff auf 70 Prozent verkleinert. Er steht weiter von der Wand entfernt. Ein regulärer Soldat derselben Szene wurde entfernt; die übrigen Grenzposten bleiben bestehen.

Triple T wurde regulär mit dem Wald-Amulett sowie in den Credits geprüft. **Sein Programmcode bleibt unverändert.** Es gibt keinen zusätzlichen Eingriff für unvollständige Debug-Spielstände.

## Speicher und Prüfungen

Die neuen V70-Ergänzungen vergrößern weder den gemeinsamen Elf-Msg2-Actor noch dessen Modellpakete. Das gemeinsame Overlay bleibt bei 59.088 Bytes. Poe/Fackel und Medaillon benötigen **keinen neuen Object-Slot**. Die eigenen Overlays werden nur in ihren jeweiligen Räumen geladen.

Geprüft mit nativem Emulator und **4 MiB N64-RAM**:

- Poe ansprechbar bei ungelöstem, teilweise gelöstem und gelöstem Fackelrätsel; exakt vier originale Fackeln vorhanden; Gespräch verändert keine Rätsel- oder Raumabschlussflags.
- Nach gelöstem Rätsel kann Link den ursprünglichen Aufzug nach unten fahren.
- Medaillon als Kind und Erwachsener sichtbar; Navi öffnet die richtige Warnung.
- Beide neuen Szenen zusätzlich in der DEBUG-Ausgabe geladen und angesprochen.
- Alle 2.220 vor V69 vorhandenen Nachrichten bleiben unverändert; hinzu kommen nur die drei Nachrichten 7235, 7236 und 7237.
- Die vorherigen V69-Prüfungen decken Wiedererkennungsdialog vor/nach dem Waldtempel, Tag/Nacht, den ursprünglichen Kinderzauber, beide Credits-Auftritte, den nativen Tanz, Triple T und den versetzten Beta-Soldaten ab.

Modellbankreserven: Waldtempel-Halle 96.832 Bytes; Königsgrab als Kind 343.840 Bytes, als Erwachsener 300.704 Bytes. Bei den V69-Credits benötigt die tatsächliche Kinderfeier 965.936 Bytes; frei bleiben 53.968 Bytes. Diese Werte beziehen sich auf die Modellbank, nicht auf den gesamten freien Arbeitsspeicher.

Die kumulativen V68-Prüfungen und deren 83 Raum-/Zeitlinien-Ladetests liegen ebenfalls im Quellenarchiv. Das ist kein Nachweis eines vollständigen Durchspielens. Die BPS-Dateien werden unabhängig auf die saubere Basis angewandt und mit den gebauten ROMs byteweise verglichen.

## Anwenden

Eine saubere **Ocarina of Time PAL 1.0**-Basis verwenden: MD5 `e040de91a74b61e3201db0e2323f768a`. Einen der beiden BPS-Patches auf diese Basis anwenden. Nicht auf eine bereits modifizierte ROM patchen. Die neue ROM vollständig neu starten; für die Kontrolle einen normalen Spielstand laden, keinen alten Emulator-Savestate.

DEBUG: L und R halten, dann Z drücken. Ortswahl, Alter und Tageszeit sowie die vorhandenen Optionen für alle Items, Standard-/Licht-/Schattengewand und Credits-Start bleiben enthalten. Direkte Sprünge oder hinzugefügte Amulette stellen nicht automatisch alle Storyflags her.

## Quellen nachbauen

Nach sämtlichen V68-Buildern in dieser Reihenfolge ausführen:

```sh
python3 tools/build_mint_kokiri_v69.py /pfad/zum/oot
python3 tools/build_beta_soldier_adjust_v69.py /pfad/zum/oot
python3 tools/build_yellow_poe_v70.py /pfad/zum/oot
python3 tools/build_sonichu_v70.py /pfad/zum/oot
```

Nur für die separate DEBUG-Ausgabe anschließend `build_debug_version.py` ausführen. Zum Wiederherstellen der normalen fünf Quelldateien besitzt dieser Builder `--restore`.

Das fertige Medaillonmodell liegt als C-Displayliste und Zwischenformat bei. Die optionale Neukonvertierung des Uploads erfolgt mit `export_sonichu_v70.py` (Blender), gefolgt von `generate_sonichu_v70.py`. Das Archiv enthält weder eine ROM noch einen Spielstand oder Emulatorbinaries.
