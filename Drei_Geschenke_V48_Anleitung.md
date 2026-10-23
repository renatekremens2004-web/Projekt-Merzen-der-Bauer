# V48: Drei Geschenke, Lichtgewand erst in der Zitadelle und kleinere Figuren im Fenster

Diese Version enthält alle Änderungen bis V47.

Nach dem ersten Ziehen des Master-Schwerts bekommt Link zunächst das Licht-Amulett. Habeck sagt anschließend: „Ach ja, das ist noch nicht alles. SPIELT DIE ANIMATION NOCH MAL AB!“ Darauf folgt die zweite Erhalt-Animation mit dem gelben Lichtgewand. Danach sagt er: „Warte, das hier sollte auch noch ganz praktisch sein zu haben“, und die dritte Animation zeigt den Glotzaugenfrosch.

Link bleibt während der ganzen Zeremonie grün. Erst zurück in der Zitadelle trägt er das gelbe Lichtgewand. Navi beginnt ihren bisherigen Dialog dort mit: „Och nee, jetzt ist der Frosch einfach weggehüpft“. Ihre bisherigen Seiten folgen unverändert.

Der Frosch ist ein Gegenstand nur für diese Erhalt-Animation. Er wird nicht in den Tauschgegenstand-Slot geschrieben und startet oder beendet keinen Tauschquest-Timer. Ein bereits vorhandener Tauschgegenstand wird dadurch nicht ersetzt.

Merz und König Harkinian sind ausschließlich in der Fensterszene mit Zelda zehn Prozent kleiner. Die Positionen, ursprüngliche Kamera und Bewegungsabläufe bleiben erhalten. Merz' andere Auftritte werden dadurch nicht verkleinert.

## Gewänder und DEBUG

Die bisherige Schutzwirkung bleibt erhalten: Lichtgewand, orangefarbenes Wallace-Gewand und hellblaues Wassergewand halbieren den Schaden; das Schattengewand reduziert ihn auf ein Viertel und bleibt das stärkste Gewand. Das Schattengewand hat weiterhin Vorrang vor dem Lichtgewand.

Nur in der DEBUG-Ausgabe: L+R halten und Z drücken. C-links gibt alle Items, C-rechts wechselt Standard → Lichtgewand → Schattengewand. A lädt den gewählten Ort. Die vorhandene Credits-Option bleibt erhalten. Zum Prüfen der ersten Erhalt-Zeremonie einen passenden Spielstand vor dem ersten Master-Schwert-Ziehen benutzen; ein beliebiger DEBUG-Ortswechsel stellt den Storyablauf nicht automatisch her.

## Anwendung

Genau einen der beiden kumulativen BPS-Patches auf eine saubere europäische Ocarina-of-Time-PAL-1.0-ROM anwenden, nicht auf einen vorherigen Patchstand. Quell-ROM-MD5: `e040de91a74b61e3201db0e2323f768a`. Spielstände vorher sichern. Das Quellen-ZIP enthält keine ROM.

## Prüfung

- Normal- und DEBUG-Ausgabe gebaut, ROM-Prüfsummen geprüft; beide BPS-Patches unabhängig zurückangewendet und mit dem jeweiligen Build verglichen.
- Mit 4 MiB nativer Speichergröße die erste Master-Schwert-Sequenz bis zu allen drei Übergaben und zurück zu Navis Satz in der Zitadelle durchlaufen. Reihenfolge, Froschdarstellung, grüne beziehungsweise gelbe Link-Farbe, leerer Tauschslot und unveränderter Timer wurden dabei geprüft.
- Die Zeremonie nutzt die vorhandenen Get-Item-Objekte. Ihr Objektbereich hatte im Test 49.440 Bytes Reserve.
- Fensterszene mit Originalkamera im Emulator geprüft: beide Figuren verwenden 90 Prozent ihrer bisherigen Größe.
- Andere Modelle und Räume sowie die neun ursprünglichen Credits-Kameras gegenüber V47 verglichen. Keine zusätzlichen Modelle oder Texturen für den Frosch.
- Die MP4 enthält native Spielmusik und Effekte und wurde mit dem veröffentlichten normalen ROM-Build aufgenommen.

Dies ist ein gezielter Test der Änderungen, kein vollständiger neuer Spieldurchlauf.

## Wiederaufbau

Nach dem bisherigen V47-Ablauf `python3 tools/build_frog_award_v48.py /pfad/zum/oot-burns-pal` ausführen. Für die DEBUG-Ausgabe weiterhin `build_debug_version.py` zuletzt ausführen; mit dessen `--restore` danach die normale Ausgabe wiederherstellen. Die Sicherungen unter `tools/originals/frog-award-v48` enthalten die V47-Ausgangsdateien für einen reproduzierbaren erneuten Builder-Aufruf.
