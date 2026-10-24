# V67: Lila Dateimenü und kürzerer Kokiri-Hals

Das Spielstandmenü ist jetzt lila: Fenster und Datei-Schaltflächen verwenden RGB **170/85/230**, die Auswahlmarkierung ein helles Lila. Auch die farbige Sprach-Auswahl verwendet den neuen Ton. Die bestehenden Fenster beim Benennen, Kopieren und Löschen greifen auf dieselbe Fensterfarbe zurück.

Beim neuen blonden Kokiri aus V66 sitzt der Kopf tiefer: sein Kopfansatz wird ausschließlich bei dieser Figur um 300 Modelleinheiten versetzt, bei der vorhandenen Skalierung etwa drei Spieleinheiten. Damit wirkt der Hals kürzer und der Übergang zum Körper sitzt sauberer.

## Prüfung

Normale und DEBUG-Ausgabe jeweils mit 4 MiB im Emulator gestartet und bis zur tatsächlichen Spielstand-Auswahl bedient. Die aktive Menüinstanz enthält die neuen RGB-Werte; das gerenderte Menü wurde angesehen. Der Kokiri wurde im Spiel mit der kürzeren Halsposition angesehen und sein wiederholtes Gespräch erfolgreich durchgespielt. Beide BPS wurden unabhängig auf die saubere Basis angewendet und bytegenau mit den gebauten Ausgaben verglichen.

Alle bisherigen V66-Inhalte sind enthalten. Diese Ergänzung ändert die Menüfarben und den Kopfansatz der einen Kokiri-Figur. Speicherformat, Freischaltung des Lauftempos und übrige Spiellogik werden nicht geändert. Kein vollständiger neuer Spieldurchlauf.

## Anwendung

Genau einen V67-Patch auf eine **saubere europäische PAL-1.0-ROM** anwenden. Basis-MD5: `e040de91a74b61e3201db0e2323f768a`. Die ROM neu starten und reguläre Spielstände verwenden; alte Emulator-Savestates enthalten alte Menü- und Codezustände.

Auf dem V66-Quellenstand `python3 tools/build_purple_menu_v67.py /pfad/oot` ausführen und normal bauen/komprimieren. DEBUG bleibt der optionale letzte Builder. Das kumulative Quellenpaket enthält keine ROM.
