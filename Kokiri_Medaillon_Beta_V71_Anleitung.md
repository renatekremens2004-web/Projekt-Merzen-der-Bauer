# V71 – Kokiri, erkennbares Medaillon und Beta-Gorone

[DEBUG-Patch](Mr_Burns_Mr_Bean_DE_PAL10_DEBUG_Sonichu_Medaillon_V71.bps?raw=true) · [Normaler Patch](Mr_Burns_Mr_Bean_DE_PAL10_Sonichu_Medaillon_V71.bps?raw=true) · [Quellenergänzung](Kokiri_Medaillon_Beta_V71_Quellen_Update.zip?raw=true)

Beide BPS-Patches sind **kumulativ**, einschließlich aller bisherigen V70-Inhalte. Genau einen Patch auf eine saubere europäische Ocarina-of-Time-PAL-1.0-ROM mit MD5 `e040de91a74b61e3201db0e2323f768a` anwenden. Nicht auf eine bereits gepatchte ROM anwenden. Danach die neue ROM vollständig neu starten und einen regulären Spielstand statt eines alten Emulator-Savestates laden. Spielstände können weiterverwendet werden.

## Änderungen

- Der blonde Kokiri mit mintfarbener Mütze bleibt als Kind im Wald. Als Erwachsener steht er bis zum Waldtempel ebenfalls dort. Nach dem Waldtempel steht er draußen auf der Hylianischen Steppe unmittelbar vor dem Waldeingang und erzählt Deinen neuen Text über seine Magie, mit der die Kokiri künftig den Wald verlassen können.
- In der Wald-Kamerafahrt der Credits bleibt er ruhig. Auf der Feier auf der Lon-Lon-Farm tanzt er mit der originalen Kokiri-Tanzanimation an einem früheren, sichtbaren Platz. Die ursprünglichen Credits-Kameras bleiben erhalten. Keine anderen Partygäste wurden hierfür versetzt.
- Das Sonichu-Medaillon erhält eine dünne, dreidimensionale Silhouette und die unmittelbar aus Deinem Originalmodell gerenderte Vorderseite. Gesicht, Ohren und Aufhängung sind erkennbar. Es liegt links neben der Sonnenlied-Inschrift frei auf dem Boden. Navi sagt weiterhin: **„Fass es bloß nicht an!“**
- Die verkleinerte Pistole des Beta-Goronen sitzt am Griff in seiner Hand.
- Im Darunia-Raum der Credits steht zusätzlich der gewöhnliche Beta-Gorone: ohne Soldatenausstattung, Helm oder Waffe.

Die MIDI-Hörprobe ist separat in Arbeit und verändert in dieser Version keine Musik.

## Prüfungen und Speicher

Mit nativen **4 MiB N64-RAM** im Emulator geprüft: Medaillon und Navi-Text; Kokiri vor und nach dem Waldtempel, Steppe bei Tag/Nacht sowie als Kind; korrekte Gesprächszuordnung; Beta-Pistole; normale Credits-Kameras mit tanzendem Kokiri und anschließendem Szenenwechsel; gewöhnlicher Beta-Gorone im Darunia-Raum und Fortsetzung der Credits. Die DEBUG-Ausgabe wurde zusätzlich in den neuen Bereichen geprüft. Kein vollständiger neuer Spieldurchlauf.

Das Medaillon verwendet **98 Dreiecke**, seine Vorderseite 128×128 Pixel in vier N64-gerechten 64×64-CI4-Kacheln. Das Grabraum-Paket ist mit 37.680 Bytes kleiner als vorher (39.408 Bytes). Es entstehen dort weder weitere Modellbank-Slots noch zusätzliche Medaillon-Instanzen.

Die Modelle des Kokiri auf der Steppe sind ausschließlich im vorhandenen privaten Overlay untergebracht; sie vergrößern weder den gemeinsamen Elf-Msg2-Actor noch den Raum der Steppe. Dadurch bleibt der Modellbankbedarf der Steppe unverändert. Das private Overlay belegt 37.744 Bytes und wird nur in seinen vorgesehenen Situationen geladen. Der gemeinsame Elf-Msg2-Actor bleibt bei 59.088 Bytes.

Auf der Feier wird ein vorhandener Kokiri-Tänzer ersetzt. Sein zusätzlicher Kopf liegt in den Raumdaten, ohne weiteren Object-Slot. Der Darunia-Creditsraum erhält zwei passende native Modellpakete; die Bank bleibt innerhalb ihres Budgets. Objektbank, Actor-Allokationen und Grafikpuffer wurden im Emulator überwacht.

Die BPS-Dateien werden mit einer zweiten Patch-Implementierung auf die saubere Basis angewandt und byteweise mit den gebauten ROMs verglichen. Der Build verwendet die regulären PAL-1.0-Linkschritte und Overlay-Relokationen.

## Quellen

`Kokiri_Medaillon_Beta_V71_Quellen_Update.zip` ist eine **Quellenergänzung** zum [vollständigen V70-Quellenarchiv](Merzen_Kokiri_Poe_Medaillon_V70_Quellen_Patch.zip?raw=true). Über dessen entpackte Dateien legen und nach sämtlichen V70-Buildern in dieser Reihenfolge ausführen:

```sh
python3 tools/build_sonichu_v71.py /pfad/zum/oot
python3 tools/build_mint_story_v71.py /pfad/zum/oot
python3 tools/build_beta_credits_v71.py /pfad/zum/oot
```

Danach den regulären PAL-1.0-Build starten. Für die separate DEBUG-Ausgabe wie bisher anschließend `build_debug_version.py` ausführen. Modellquellen, Builder und deren Originaldatei-Caches sind enthalten; keine ROMs oder Spielstände.
