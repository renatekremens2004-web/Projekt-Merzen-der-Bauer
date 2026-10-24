# V64: Gaster im Schattentempel und Sound bei jedem Goronen-Schuss

Gaster hat vier mögliche Standorte im Schattentempel (Räume 2, 6, 7 und 11). Beim Laden des jeweiligen Raums besteht eine Chance von 50 Prozent, daß er erscheint. Dadurch können Auftritte ausbleiben und sich zwischen Besuchen ändern. Er steht still, blickt bei seinem Erscheinen zu Link und verschwindet bei Annäherung auf 90 Spieleinheiten, nachdem er sichtbar geworden ist. Innerhalb desselben Raumbesuchs erscheint er anschließend nicht erneut. Es gibt keinen Dialog, keine Navi-Ansprache, keine Kollision und keine Animation. Schalter, Items und Fortschrittsmarkierungen werden nicht verändert.

Das bereitgestellte Modell bleibt bei 108 Dreiecken und ist 75 Spieleinheiten hoch. Es verwendet drei kleine CI4-Texturen mit jeweils 32 × 32 Pixeln. Das Modell steckt im vorhandenen Elf-Msg2-Actor-Overlay; neue Objektbank-Slots oder zusätzliche Modellblöcke in den doppelt gepufferten Räumen sind nicht notwendig. Pro möglichem Standort kommt ein leichter Actor-Eintrag hinzu. Die Bodenhöhe wird beim Erscheinen geprüft; ungeeignete Höhen werden verworfen.

Die Goronen-Änderung aus V63 ist enthalten: jeder tatsächlich erzeugte Schuß startet genau einen Sound der jeweiligen Rolle. Der nächste Schuß startet den Clip neu, auch wenn er noch läuft. Die vorherige Wartezeit entfällt; Schußfolge und Zielverfolgung bleiben unverändert. Im vollständigen DEBUG-Durchlauf wurden 23 Schüsse mit 23 Soundstarts nachgewiesen (9/8/6). Der normale Durchlauf erreichte ebenfalls das gelernte Lied und die Rückkehr; dessen ursprünglicher Prüfer las den Soundzähler erst nach dem Entladen des Actor-Overlays aus. Dieser Fehler im Prüfer wurde korrigiert. Die Soundzähler im normalen Lauf wurden bereits während des geladenen Abschnitts als 9/8/6 aufgezeichnet.

## Prüfungen

Die vier Gaster-Räume wurden mit 4 MiB im Emulator geladen. Ein normaler Zufallsdurchlauf zeigte Gaster in Raum 11 und prüfte das Verschwinden bei Annäherung; andere Durchläufe zeigten die ausgelassenen Erscheinungen. Zusätzliche Prüfungen können die Zufallsfunktion ausschließlich im Emulator überschreiben, um alle Standorte gezielt zu kontrollieren. Diese Überschreibung ist kein Teil der veröffentlichten ROM oder Builder. Alle vier Standorte haben die gezielt erzwungene Sichtbarkeits- und Annäherungsprüfung bestanden; zusätzlich wurde der Auftritt in DEBUG mit 4 MiB geprüft. Die Protokolle unterscheiden reguläre, versetzte und erzwungene Prüfungen.

Die Goronen-MP4 enthält echten Spielton aus V63. V64 ergänzt ausschließlich Gaster; die Goronen-Implementierung ist dieselbe. Beide V64-Patches wurden mit einem unabhängigen Patcher auf die saubere Basis angewendet und bytegenau geprüft. Kein vollständiger neuer Spieldurchlauf.

## Anwendung und Quellen

Genau einen V64-BPS-Patch auf eine saubere europäische PAL-1.0-ROM anwenden. Basis-MD5: `e040de91a74b61e3201db0e2323f768a`. Alle bisherigen Änderungen sind enthalten. ROM neu starten und reguläre Spielstände verwenden; alte Emulator-Savestates enthalten alten Code und RAM-Zustände.

Auf dem V62-Quellenstand zuerst `python3 tools/build_defender_shots_v63.py /pfad/oot`, dann `python3 tools/build_gaster_v64.py /pfad/oot` ausführen und normal bauen/komprimieren. DEBUG bleibt der optionale letzte Builder. Der Gaster-Export und die vorbereiteten Modelldaten sind enthalten. Das kumulative Quellenpaket enthält keine ROM.
