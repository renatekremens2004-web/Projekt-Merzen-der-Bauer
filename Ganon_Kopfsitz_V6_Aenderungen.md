# Ganon-Kopfsitz V6

Der große Burns-Kopf der Ganon-Bestienform sitzt jetzt tiefer und weiter hinten am Hals/Kragen. Er wurde als starrer Teil um [0, -1235, -533] Einheiten im nativen Kopfknochen verschoben. In der neutralen Referenzhaltung entspricht das ungefähr neun Spieleinheiten nach unten und zehn zum Körper hin. Kopfgröße, Proportionen, Polygone, Texturen und Beleuchtung bleiben unverändert.

Ausschließlich die XYZ-Positionen der vorhandenen 1080 Eckpunkte dieses einen Kopfes geändert. Keine Änderung an Skalierung, UVs, Normalen, Displaylisten-Befehlen, Skeletten, Animationen, Kollision oder Boßlogik. Ganondorfs menschliche Form und der vollständige Burns in der Kindheit bleiben unverändert.

## Prüfung

Beide PAL-Builds mit gültiger N64-Prüfsumme. Die erzeugten Eckpunktdaten im kompilierten Objekt mit V5 verglichen: ausschließlich die drei Positionswerte pro Vtx sind verschoben. Der gesamte Rest von OBJECT_GANON2 und alle anderen dekomprimierten Spielsegmente sind bytegleich; lediglich ROM-Prüfsumme und komprimierte DMA-Adressen ändern sich zusätzlich. Speicherbedarf und bestehende Puffer bleiben gleich.

Laufzeitprobe der finalen normalen ROM mit tatsächlichen 4 MiB und Grafik-Clipping: native Verwandlung, gebeugte Haltung nach dem Wachstum, anschließende Kampfhaltung und 180 freie Spielbilder im Ganon-Kampf. Seitliche und vordere Aufnahmen zur Kontrolle des Hals-/Kragenanschlusses gesichtet. Keine Objektpufferüberläufe, ungültigen Grafikkommandos, Vertexfehler oder Abstürze in dieser Probe. 19520 Bytes Reserve im Objektpuffer wie zuvor. Nur Spieler-/Fortschrittsdaten zum Einstieg vorbereitet; keine Figuren für das Bild versetzt und keine Boßaktionen/Animationszustände injiziert. Die MP4 enthält 600 durchgehende Spielbilder der Verwandlung, 36 Sekunden bei PAL 50/3 Bildern pro Sekunde, ohne Ton. Kein vollständiger Spieldurchlauf oder Hardwaretest.

Beide BPS mit RomPatcher.js und aktiver Quellvalidierung auf die unveränderte Vanilla-ROM angewandt und byteweise mit ihren Ziel-ROMs verglichen.

## Anwendung

Je einen kumulativen Gesamtpatch auf die unveränderte Europe/PAL-1.0-ROM anwenden, nicht auf eine bereits gepatchte Datei. Original-MD5 e040de91a74b61e3201db0e2323f768a. Deutsch wählen. Alle bisherigen Änderungen enthalten; normal und DEBUG haben denselben Spielinhalt, Debugsteuerung unverändert.

## Quellen

Letzter normaler Builder: tools/build_ganon_neck_fit.py nach build_finale_burns.py und vor optional build_debug_version.py. Verschiebung in tools/ganon_neck_fit.json; der Builder arbeitet idempotent auf der gesicherten V5-Vorlage. Archiv enthält vorherigen Quellenstand, Ergänzung und Prüfungen; keine ROM, Saves, SRAM, Savestates, ELF oder ausführbaren Programme.

normal Ziel-SHA256: 56379c68b8ac334dbafc60114295d6a8be7f6a3ebf47eb4ca92e4030a38fab75

debug Ziel-SHA256: 733b1ee419c94fb151a88b1778269580376d5c6ea2601b2b7ff20024cce1549e
