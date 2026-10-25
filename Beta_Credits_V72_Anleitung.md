# V72 – Beta-Gorone mittig vor der Statue

[DEBUG-Patch](Mr_Burns_Mr_Bean_DE_PAL10_DEBUG_Beta_Credits_V72.bps?raw=true) · [Normaler Patch](Mr_Burns_Mr_Bean_DE_PAL10_Beta_Credits_V72.bps?raw=true) · [Bild](Beta_Gorone_Teppich_V72.png) · [Quellenergänzung](Beta_Credits_V72_Quellen_Update.zip?raw=true)

Der gewöhnliche Beta-Gorone steht in den Goronia-Credits jetzt mittig auf der Teppichfläche vor der Statue in Darunias Raum. Ohne Helm, Soldatenkleidung oder Waffe. Seine Füße stehen auf dem Boden. Die ursprünglichen Kameras und alle anderen Figuren bleiben unverändert.

Normal und DEBUG wurden mit 4 MiB N64-RAM im nativen Emulator geprüft, einschließlich der anschließenden Fortsetzung der Credits zum Hylia-See. Modellbankbedarf und Actor-Anzahl bleiben gegenüber V71 unverändert. Beide BPS-Dateien wurden unabhängig auf die saubere Basis angewandt und byteweise mit dem Build verglichen.

Die Patches enthalten **alle bisherigen Änderungen einschließlich V71**. Genau einen auf eine saubere europäische PAL-1.0-ROM anwenden (MD5 `e040de91a74b61e3201db0e2323f768a`), danach vollständig neu starten und einen regulären Spielstand laden. Die MIDI-Hörprobe ist separat; die Musik im Spiel ist in diesem Patch unverändert.

Die Quellenergänzung wird nach dem vollständigen V70-Quellenarchiv und der V71-Quellenergänzung ausgeführt:

```sh
python3 tools/build_beta_credits_v72.py /pfad/zum/oot
```

Der normale PAL-1.0-Build und die bisherige DEBUG-Erstellung bleiben gleich. Keine ROMs oder Spielstände im Quellenpaket.
