# Pepsiman im Wassertempel

Kumulativer Gesamtpatch, ROM-SHA256 `dfa18e3c0db488033ebc9254e12725901a0a56e5dbea420263ce4730e5d9ce71`. Alle bisherigen Änderungen einschließlich hellblauer Zora-Tunika und Eisenstiefel-Schnellwechsel enthalten. Zwei neue deutsche Nachrichten 3072/3073 (zuvor unbenutzte Platzhalter), insgesamt 991 eigene Nachrichten. Alle früheren deutschen Texte sowie Englisch/Französisch bleiben erhalten. Alte Rechtschreibung, normale manuelle Weiter-Tasten, keine geänderten festen Zeiten.

## Platzierung und Verhalten

Pepsiman steht im Inneren des Tempels, Raum 16 in der ruhigen kleinen Schatzkammer, rechts neben der normalen Route bei −1160/108/−2790. Er steht weder im Eingangsraum noch im Hauptknoten. Native verschlossene Tür, Truhe und beide Krüge bleiben an ihren ursprünglichen Stellen. Ruhige Kopf-/Armbewegung, Gesprächsgeste, Z-Anvisieren und A-Gespräch, beliebig wiederholbar. Nativer OC-Körperzylinder Radius 14/Höhe 94 verhindert Durchlaufen; keine Treffer-/Angriffskollision, keine Gegnerkategorie und kein Raum-Clear-Einfluß. Nur erwachsen/deutsch. Collider auch vor frühen Löschungen gültig initialisiert.

Sechs Dosen an festen Originalböden in fünf Räumen:

| Raum | Modell | Position X/Y/Z |
| --- | --- | --- |
| 7 | normal | −3330 / 1060 / −4050 |
| 9 | normal | −1265 / 60 / −1540 |
| 16 | normal | −1390 / 108 / −2820 |
| 16 | zerdrückt | −1380 / 108 / −2990 |
| 17 | normal | 1060 / 780 / 75 |
| 19 | normal | 1730 / 780 / −55 |

Dosen haben gar keine Kollision oder Physik, schalten keine Flags und gehören nicht zu Gegnern oder Rätseln. Z + C-Up nutzt den ursprünglichen wiederholbaren Elf_Msg2-Navi-Prüfpunkt. Gegner erhalten im Kampf weiterhin normalen Anvisier-Vorrang; nach dem Kampf können die Dosen geprüft werden. Die Dose auf dem oberen Absatz von Raum 17 liegt über dem höchsten Wasserstand; der erste Thaddäus-Auftritt bleibt unverändert. Wasserstand, Türen, Schalter, bewegliche Plattformen und Fluchtwege werden nicht angepaßt.

## Aufwand und Prüfungen

Pepsiman: PS1-Vorlage mit 562 Ursprungsdreiecken, 707 nach Schnitt an Texturkachelgrenzen; eigene vier starre Matrixgruppen, 95 Spieleinheiten hoch. Keine Dehnung auf ein anderes NPC-Skelett. Vier 64×64-CI4-Kacheln werden nacheinander geladen und bewahren das Brustlogo. Die Dosen nutzen 88/102 Dreiecke und sind 6,5 Einheiten hoch beziehungsweise breit. In Raum 16 zusammen höchstens 897 zusätzliche Dreiecke und drei zusätzliche Actors; in den anderen vier Räumen je eine kleine Dose.

Keine zusätzlichen Objekt-Slots. Größte feste Raum-Pufferanforderung bleibt exakt 131.728 Bytes, unverändert gegenüber dem vorherigen Gesamtpatch. Raum 16 wächst als Datei um 53.072 Bytes, bleibt mit Nachbarraum unter dem bereits benötigten Maximum. Die übrigen vier Räume wachsen je um 5.184 Bytes. Die Darstellung setzt Raumsegment 03 und Matrixsegment 0D lokal und stellt sie anschließend wieder her. Native Beleuchtung, Schatten und Nebel bleiben wirksam.

Alle 1509 komprimierten ROM-Segmente mit dem unkomprimierten Neubau verglichen, CIC-6105-Prüfsumme korrekt, ROM weiter 32 MiB. 2954 Kernfunktionen und sechs unveränderte native Elf_Msg2-Funktionen anhand von Originalbytes/echten MIPS-Relokationen geprüft. Sechs bestehende statische Helfer für Wallace, Nintendo 64 und Majoras Maske im Quelltext unverändert. 127 Original-Assets der fünf Räume geprüft, ursprüngliche Actor-Einträge und sämtliche anderen Räume, Kollisionsdaten, Objektlisten, Türen und Boßakteure erhalten. Alle 991 Textpuffer einschließlich längstem erlaubtem Spielernamen geprüft.

14 gezielte abgeschlossene Mupen64Plus/GLideN64-Proben mit echten 4 MiB: vollständiger wiederholter Pepsiman-Dialog bei allen drei Wasserständen; alle sechs Dosen/Varianten mit wiederholter nativer Navi-Reaktion (Kampfzimmer im regulären Zustand nach dem Kampf, Raum 17 nach Begegnung); normale englische Fassung ohne zusätzliche Figuren; nativer Türdurchgang Raum 16 nach 12; bisheriger Wallace in Dodongos Höhle, Nintendo-64-Prüfpunkt in Jabu und Majoras-Masken-Prüfpunkt im Waldtempel. Die ersten Kampf-/Thaddäus-Proben erreichten statt der Dose die nativen Gegner-/Storytexte; gesondert als solche dokumentiert. Keine vollständige Durchspielung des Wassertempels und kein Hardwaretest behauptet. PNGs unveränderte echte Emulatoraufnahmen.

BPS in RomPatcher.js mit aktiver Quellvalidierung auf die Original-ROM mit MD5 e040de91a74b61e3201db0e2323f768a angewandt: Ergebnis bytegleich zur geprüften Produktions-ROM. Direkt auf die entpackte unveränderte Europa/PAL-1.0-ROM anwenden. Keine ROM, Teststarts, Saves, Speicherabbilder oder ausführbaren Programme veröffentlicht.
