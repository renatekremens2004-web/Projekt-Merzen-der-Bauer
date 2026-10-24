# V66: Früher Gorone, früher Kokiri und umschaltbares Lauftempo

## Die Figuren

Der frühe Gorone aus dem originalen Objekt **00CF / object_oF1s** steht am Todesberg neben dem dortigen Goronen, nur in der Kinder-Zeitlinie und im normalen Spiel. Sein Text lautet:

> Alle anderen sagen immer, ich sei so anders. Ich verstehe das nicht goro goro

Das originale Modell, seine Texturen und sein 17-gliedriges Skelett bleiben erhalten. Die kompatible native Goronen-Animation bewegt ihn im Stand. Eine neue Rolle im vorhandenen Goronen-Actor übernimmt Gespräch und passive Kollision; die normale Goronen-KI wird für diese einzelne Figur nicht gestartet. Das Laden des zusätzlichen Modellobjekts wird abgewartet.

Im Kokiri-Wald steht ein neuer Kokiri mit dem blonden Kopf und der mintfarbenen Mütze aus **0052 / object_oE9**. Er verwendet einen vorhandenen männlichen Kokiri-Körper mit nativen Bewegungen und spricht als Kind:

> Hey [Spielername], na was geht so? Der Deku-Baum will mit dir quatschen? Right on Link! Warte, laß mich dir eine Funktion einbauen, die dich schneller macht!

Nach dem Gespräch hebt er den Arm und zaubert mit Feen-Klang und einer aufsteigenden Spirale aus Lichtfunken um Link. Danach wird die Fähigkeit freigeschaltet und ihre Steuerung erklärt. Bei weiteren Gesprächen sagt er:

> Ey Kollege, das hab ich doch gerne gemacht. Der Deku-Baum hat mir das neulich beigebracht, voll verschärft oder?

Der alte Kopf benötigt zwei Anpassungen an die heutige Grafik-Pipeline: der überholte Aufruf einer dynamischen Displayliste auf Segment 0D entfällt, und seine Augen verwenden das heutige Kokiri-Augensegment 0A. Seine Geometrie und Texturen bleiben erhalten. Der Körper und die anderen Kokiri behalten ihre bisherigen Köpfe.

## Schneller laufen

**Steuerkreuz links** schaltet nach der Freischaltung zwischen normalem und schnellem Laufen um. Ein gedrückt gehaltener Knopf schaltet nur einmal. Der schnelle Modus erhöht das Bewegungsziel am Boden auf **150 Prozent**. Er gilt für beide Altersstufen, verwendet die native Beschleunigung, Laufanimation und Kollisionsbehandlung und erhöht weder Schwimmtempo noch die Bewegung mit Eisenstiefeln. Während Gesprächen, Zwischensequenzen, Pausenmenüs und Übergängen wird der Schalter nicht verarbeitet.

Freischaltung und gewählter Modus verwenden zwei bisher freie, dokumentierte `infTable`-Bits: **1CC** für die Fähigkeit und **1CB** für den Schalter. Beide gehören zum normalen gespeicherten Fortschritt. Das Speicherformat wird nicht erweitert. Die bestehenden Gewand-Bits 1CD/1CE und Navis Bit 1CF bleiben getrennt. Nach der Verleihung beginnt der Modus ausgeschaltet.

**Steuerkreuz unten/oben** bleibt für Eisen- und Gleitstiefel verfügbar.

## Schild und Wachen

Der Deku-Schild im Kokiri-Laden kostet **20 statt 40 Rubine**. Preisfeld, Beschreibung und Kaufabfrage sind angepaßt.

Die Wachen im Schloßgarten reagieren auf Sichtmeldungen nur noch innerhalb von **225 Spieleinheiten**. Ihre Suchstrahlen, Hindernisprüfung, Laufwege und das Erwischtwerden bleiben erhalten. Die Gerudo-Patrouillen haben **25 Prozent weniger Sichtweite**: tagsüber 281,25 statt 375, nachts 140,625 statt 187,5 Einheiten. Ihr Blickwinkel, Geräuscherkennung und unmittelbarer Nahkontakt funktionieren weiterhin wie zuvor. Das Verhalten der Schwertkämpferinnen im Kampf wird nicht verändert.

## Prüfungen

- Normaler früher Gorone: Laden mit 4 MiB, sichtbares originales Modell und ansprechbarer Dialog. Die Todesberg-Objektbank bleibt bei 18 Slots mit 140.720 freien Bytes.
- Kokiri und Zauber in Normal und DEBUG mit 4 MiB: erster Dialog, zeitlich begrenzte Magie, Freischaltung, Erklärung und zweiter Gesprächszweig.
- Gemessen bei gleichem Stickausschlag: **5,3886 → 8,0830 → 5,3886** Spieleinheiten pro Bild. Vor der Freischaltung bleibt links wirkungslos.
- Exportierter Fortschrittsstand neu geladen: die Fähigkeit bleibt vorhanden, und der Kokiri verwendet direkt seinen zweiten Dialog. Zusätzlich als Erwachsener: Fähigkeit nutzbar, Figur nicht vorhanden, alle drei Stiefel-Umschaltungen weiterhin funktionsfähig.
- Kokiri-Laden mit 4 MiB: das tatsächliche Schild-Actor-Preisfeld beträgt 20 Rubine.
- Ausgeführte MIPS-Grenzwerttests der kompilierten Wachen-Funktionen: sechs Gerudo-Prüfungen an den Tag-/Nacht-Grenzen und zwei Prüfungen der Schloßwache bei 225 und 225,25 Einheiten. Für den isolierten Schloß-Test sind Animation, Grafik und Ton als externe Aufrufe ersetzt; die neue Entdeckungsprüfung selbst wird ausgeführt. Kein vollständiger neuer Schleichabschnitt-Durchlauf.
- Die bisherige Kakariko-Verteidigungssequenz läuft mit der endgültigen normalen Fassung und 4 MiB vollständig durch: 23 Schüsse, 23 Soundstarts, Sheik-Gespräch, Lied gelernt und Rückkehr ins steuerbare Dorf. Die ursprüngliche Objektbank-Reserve von 3.808 Bytes bleibt erhalten.
- **2.215 bisherige Texte** in allen vorhandenen Sprachfeldern verglichen; ausschließlich die beiden Schild-Preistexte sind geändert. Vier neue Text-IDs: 7230–7233.
- Beide BPS mit einem unabhängigen Patcher auf die saubere Basis angewendet und bytegenau geprüft. Kein vollständiger neuer Spieldurchlauf.

## Anwendung und Quellen

Genau einen V66-BPS-Patch auf eine **saubere europäische PAL-1.0-ROM** anwenden. Basis-MD5: `e040de91a74b61e3201db0e2323f768a`. Alle bisherigen Änderungen sind enthalten. Die neue ROM neu starten und reguläre Spielstände verwenden; alte Emulator-Savestates enthalten alten Code und RAM-Zustände.

Auf dem kumulativen V64-Quellenstand zuerst `python3 tools/build_early_goron_v65.py /pfad/oot`, dann `python3 tools/build_kokiri_speed_v66.py /pfad/oot` ausführen. Danach normal bauen/komprimieren. `build_debug_version.py` bleibt der optionale letzte Schritt für eine getrennte DEBUG-Ausgabe; `--restore` stellt die normalen Kernquellen wieder her, anschließend erneut bauen.

Das Quellenpaket enthält die Builder, Änderungen an den nativen Assets und Prüfberichte, keine ROM. Die isolierten MIPS-Prüfungen benötigen zusätzlich das Python-Paket `unicorn`; der normale Spiel-Build benötigt es nicht.
