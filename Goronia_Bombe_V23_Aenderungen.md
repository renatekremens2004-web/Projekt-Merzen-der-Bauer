# Goronia: CDU-Bombe V23

In der gewöhnlichen Erwachsenen-Zeitlinie steht im zentralen unteren Saal von Goronia eine große Bombe aus dem hochgeladenen Modell. Das ursprüngliche Emblem ist entfernt, vorn und hinten sitzt ein neu aufgebautes CDU-Emblem. Höhe 180 Spieleinheiten, ungefähr zweieinhalbmal ein erwachsener Link. Statische Kulisse mit fester Berührungskollision, keine Explosion oder Schadensfunktion. Wege zu Darunias Büro und den Ausgängen bleiben frei.

Vier zusätzliche native Donnerblumen stehen getrennt um die Bombe. Kleinster Abstand einer neuen Blume zu irgendeiner anderen Blume: 212,33 Spieleinheiten. Nativer maximaler Explosionsradius: 80, Zielradius einer Blume: 9. Alle neuen Positionen gegen die nach oben gerichteten Bodendreiecke geprüft. Im Emulator hat eine normale Bombe nur die nächste neue Donnerblume ausgelöst; die anderen drei blieben ruhig, die ausgelöste Blume wuchs wieder nach.

Navi reagiert auf Z-Anvisieren und C-oben. Neuer Text 71DD, genau zwei manuell umblätterbare Seiten:

1. Ich fass es nicht!
2. Die Schweine haben mir meine Idee geklaut!

Die Bombe bleibt nach dem Gespräch erhalten und kann erneut untersucht werden. Keine Questflags oder anderen NPC-Texte überschrieben.

Goronia-BGM wird nur für erwachsenen Link im deutschen normalen Spielbetrieb vor dem Feuer-Amulett auf 30 Prozent skaliert. Die native Tempo-Schnittstelle rundet auf ganze BPM: 115 → 34 BPM (etwa 29,6 Prozent). Keine Tonhöhenänderung; Geräusche und Spielgeschwindigkeit bleiben unverändert. Beginn und erneute Tempo-Befehle der Musik berücksichtigt. Mit dem Feuer-Amulett läuft das Lied wieder normal (115 BPM), auch bei einem neuen Betreten der Stadt. Die Bombe und Blumen bleiben als Kulisse erhalten. In der Kind-Zeitlinie bleibt die Stadt einschließlich Musik und großem Krug unverändert.

## Prüfung

Normal und DEBUG gebaut und mit gültigen N64-Prüfsummen versehen. Gegen V22 sämtliche bestehenden Nachrichten in allen Sprachen unverändert; nur 71DD neu. Geometrie und Spiellogik anderer Szenen gegen ihre bisherigen Segmente geprüft, sonstige Adreßänderungen auf Linker-Relokationen beschränkt. Zentrale Raumdaten und Elf_Msg2/Play-Code gezielt erweitert. Kein neuer Objektbank- oder DMA-Eintrag. Originale Schauspieler-Einträge bleiben erhalten.

Mit tatsächlichen 4 MiB RAM in Mupen64Plus/GLideN64 geprüft: Erwachsene vor/nach Feuer-Amulett, Kind, Explosion und Nachwachsen, langsames Tempo, Wiederherstellung mit kontrolliert gesetztem Feuer-Amulett sowie zwei Navi-Seiten und erneute Ansprache. Diese kontrollierten Szenentests ersetzen keinen vollständigen Durchlauf. Screenshots zeigen die tatsächliche ROM-Ausgabe. Das neue Modell hat 540 statt ursprünglich 796 Dreiecke.

## Anwendung und Quellen

Alle bisherigen Änderungen einschließlich V22 enthalten. Normal ODER DEBUG auf eine unveränderte europäische PAL-1.0-ROM anwenden (MD5 e040de91a74b61e3201db0e2323f768a). Nicht auf eine bereits gepatchte ROM anwenden. DEBUG-Menü wie bisher: L+R halten und Z drücken.

Letzter normaler Builder: `python3 tools/build_goron_bomb_v23.py /workspace/oot-burns-pal`, nach `build_wallace_dialogue_v22.py`. Optional danach `build_debug_version.py`. Normalquellen sind nach dem separaten DEBUG-Bau wiederhergestellt. Modellquelle: vom Nutzer bereitgestellte nuclear-bomb-america-reference-very-low-poly.zip / source/nuclear.fbx; keine Texturen enthalten. Umrechnung in tools/goron_bomb_source.json, neue Texturen und CDU-Emblem in models/goron_bomb. Keine Aussage über eine weitergehende Lizenz der hochgeladenen Vorlage.
