# V60: Goronen verteidigen Kakariko

Drei Soldaten-Goronen stehen während Bongo Bongos Befreiung aus dem Brunnen in Kakariko. Sie tragen die bereits vorhandenen Helme und Gewehre, verfolgen mit ihrer Ausrichtung den Schatten und feuern versetzte kurze Salven mit sichtbarem Rückstoß. Zwei stehen gut sichtbar rechts vom Brunnen, ein weiterer sichert den westlichen Bereich. Das gilt für den deutschen erwachsenen Nocturne-Auftritt.

## Downloads und Anwendung

Genau einen der beiden V60-BPS-Patches auf eine **saubere europäische PAL-1.0-ROM** anwenden, nicht auf eine ältere Mod-Version. Die unveränderte Basis hat MD5 `e040de91a74b61e3201db0e2323f768a`. Alle bisherigen V59-Inhalte sind enthalten. Vorhandene Spielstände können weiterverwendet werden; alte Emulator-Savestates laden noch den alten ROM-/RAM-Zustand und sollten hierfür nicht benutzt werden.

- `Mr_Burns_Mr_Bean_DE_PAL10_Kakariko_Verteidigung_V60.bps`: normale Ausgabe.
- `Mr_Burns_Mr_Bean_DE_PAL10_DEBUG_Kakariko_Verteidigung_V60.bps`: zusätzliche bekannte DEBUG-Menüs.
- `Kakariko_Verteidigung_V60.mp4`: 41,4 Sekunden aus der tatsächlichen PAL-Kamerafahrt, mit originalem Spielton einschließlich der Schüsse. PAL-Tempo 50/3 Spielbilder pro Sekunde.
- `Merzen_Kakariko_Verteidigung_V60_Quellen_Patch.zip`: kumulative Quellen, Builder, Prüfungen und beide Patches; keine ROM.

Der reguläre Auslöser der Nocturne-Sequenz ist unverändert. Ein DEBUG-Spielstand, dessen Ereignis bereits als erledigt markiert ist, startet sie nicht durch bloßes Betreten Kakarikos erneut. Die Testaufnahme verwendet einen passenden vorherigen Ereigniszustand und läßt beide Teile anschließend normal durchlaufen.

## Technische Umsetzung

Es wird **kein Arwing und kein gegnerischer Schuß-Actor** geladen. Wiederverwendet werden nur die kleine Arwing-Lasergrafik und ihre 16×16-Textur. Die Schußspuren kommen aus der transformierten Gewehrhand und haben keine Kollision, keinen Schaden und keine Spielereignisse. Ein fester Pool begrenzt sie auf sechs gleichzeitig, mit zwölf Spielbildern Lebensdauer. Die tatsächliche Staffelung erreicht im Test höchstens zwei gleichzeitig.

Die drei stehenden Sonderrollen `7F5D` bis `7F5F` gehören ausschließlich zum Kakariko-Raumheader der ersten Nocturne-Sequenz. Sie rollen nicht, nehmen keine Gespräche an und registrieren keine zusätzlichen Treffer- oder Bewegungskollisionen. Beim Wechsel zu Sheiks zweiter Sequenz werden sie mit dem Raum abgebaut. Andere Soldaten, deren Dialoge und die Credits verwenden weiterhin ihre bisherigen Rollen.

Kein neuer Modell-Objektbank-Eintrag: die vorhandenen Goronen und Soldatenausrüstungen werden gemeinsam geladen. Der erste Teil nutzt mit 4 MiB RAM 14 Objekt-Slots und läßt 3.808 Bytes im Objektbank-Bereich frei. Der zweite Teil bleibt bei elf Slots und 140.800 Bytes frei. Das ist gezielt auf diese Szene zugeschnitten; weitere Modelle sollten hier nicht ungeprüft ergänzt werden.

Die Körper verfolgen eine kleine, zur bestehenden Schatten-Sequenz passende Zielbahn. Der Schatten benutzt animierte Szenengeometrie; seine Actor-Weltposition entspricht nicht dem sichtbaren Flug. Deshalb wird diese ungeeignete Position nicht als Ziel übernommen.

## Prüfung

- Normale und DEBUG-Ausgabe auf nativer 4-MiB-Konfiguration: beide Nocturne-Teile, alle drei schießenden Soldaten, Sheiks Dialog, erfolgreiches Nachspielen des Liedes und Rückkehr ins steuerbare Kakariko.
- Pro Durchlauf 53 Schüsse, verteilt auf 18 / 18 / 17; höchstens zwei gleichzeitig. Links Lebensenergie bleibt durch diese Schüsse unverändert.
- Nach dem Wechsel zu Sheiks Lied und nach der Rückkehr sind keine der drei zusätzlichen Cutscene-Rollen mehr geladen.
- Alle bisherigen Textdaten und Sprachen, sämtliche Musik, Szenen einschließlich Kameras und Credits sowie die übrigen Objektbanken, Räume und Overlays mit V59 verglichen. Nur der betroffene Kakariko-Raumheader und `ovl_En_Go2` werden erweitert; ROM-Adressen in Raumlisten werden beim Vergleich normalisiert.
- Beide BPS unabhängig auf die saubere Basis angewendet und bytegenau mit der jeweiligen gebauten Ausgabe verglichen; N64-Prüfsummen kontrolliert.
- Kein vollständiger neuer Spieldurchlauf.

## Wiederaufbau

Nach dem vollständigen V59-Stand `python3 tools/build_defenders_v60.py /pfad/oot` ausführen, dann wie bisher mit `VERSION=pal-1.0 COMPARE=0` bauen und komprimieren. Für die DEBUG-Ausgabe anschließend optional `build_debug_version.py` anwenden. Dessen `--restore` stellt die normalen Produktionsquellen wieder her; danach erneut bauen.

Das Quellenpaket enthält weiterhin die bisherigen Quellen, Assets und Prüfberichte. Automatisch erzeugbare historische Linker-Maps und vollständige Symbol-Dumps unter `validation/` sind zur Begrenzung der Paketgröße weggelassen. Die Quelltexte und Prüfskripte bleiben erhalten; die Dumps lassen sich mit `mips-linux-gnu-nm` aus dem jeweils neu gebauten ELF erzeugen.
