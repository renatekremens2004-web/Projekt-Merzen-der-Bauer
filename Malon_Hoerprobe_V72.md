# „Komm, süßer Tod“ – Malon-Hörprobe

[MP3 anhören / herunterladen](Komm_Suesser_Tod_Malon_Hoerprobe_V72.mp3?raw=true) · [Musikquellen und Prüfungen](Komm_Suesser_Tod_Malon_V72_Quellen.zip?raw=true)

**2:35 Minuten**, Stereo-MP3 mit 192 kbit/s. Die Hörprobe verwendet die ausführlichere hochgeladene Datei `Komm,_süsser_Tod_-_Evangelion_(Complete).mid` und beginnt kurz vor dem ersten Gesangseinsatz. Sie enthält Hauptmelodie, leise Gesangsharmonie, Klavier, Streicher, Bass, dezenten Rhythmus und den später einsetzenden Chor. Dynamik, Stimmenverteilung und Hall wurden für die native OoT-Besetzung eingerichtet. Der Ausschnitt wird sanft ausgeblendet.

Malons Original-Gesangssample aus dem Spiel trägt die Hauptmelodie **wortlos**. Es werden keine englischen Liedtexte gesungen. Die übrigen Instrumente stammen ebenfalls aus den nativen OoT-Samples.

Die Aufnahme stammt aus dem tatsächlich laufenden N64-Soundsystem einer getrennten Testfassung mit **4 MiB RAM**. Nach der Aufnahme wurden Lautheit und Ausklang angepasst. Die MP3 enthält keine Tonspur eines externen MIDI-Players. Die native PCM-Aufnahme hat keine übersteuerten Samples; das tatsächliche Malon-Instrument wurde während der Wiedergabe geprüft.

Für diesen Ausschnitt werden 9.776 Bytes Sequenzdaten und 4.128 Bytes Soundfont-Daten verwendet, mit maximal 13 gleichzeitig geschriebenen Stimmen. Das passt in die unveränderten Audio-Caches. Die vollständige MIDI ist länger; diese Datei ist die angefragte Hörprobe.

**Die Musik ist noch keiner Spielszene zugeordnet.** Die veröffentlichten normalen und DEBUG-Patches V72 behalten ihre bisherige Musik. Die zwei vorübergehend für die Aufnahme ersetzten Musikdateien sowie ihre kompilierten Audiopakete wurden anschließend wiederhergestellt.

## Quellen

Das ZIP enthält die MML-Sequenz, den Soundfont mit Verweisen auf Originalsamples, die Notenreduktion, den Konverter sowie Prüfprotokolle. Die Original-MIDI und extrahierte Nintendo-Samples sind nicht im ZIP enthalten. Mit der bereits hochgeladenen MIDI und einem vorbereiteten OoT-Quellbaum lässt sich die Konvertierung erneut ausführen:

```sh
python3 -m pip install mido
python3 audio/malon-preview-v72/arrange.py /pfad/zur/Complete.mid /pfad/zum/oot
```

Die Dateien im Musikordner sind für die separate Testfassung vorgesehen. Sie werden durch keinen der regulären V72-Builder in das Spiel übernommen. Die Emulator-Prüfskripte dokumentieren die hier verwendete Testumgebung; keine ROMs oder Spielstände im Archiv.
