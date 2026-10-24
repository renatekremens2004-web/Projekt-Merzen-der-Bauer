# V68: Figuren und Objekte wieder laden

Enthält sämtliche bisherigen Änderungen einschließlich V66/V67. Beide BPS-Patches auf eine unveränderte europäische Ocarina-of-Time-PAL-1.0-ROM anwenden (MD5 `e040de91a74b61e3201db0e2323f768a`). Danach die ROM neu starten. Alte Emulator-Savestates enthalten den alten Speicherzustand und eignen sich nicht für diese Prüfung; reguläre Spielstände bleiben kompatibel.

## Bestätigte Probleme und Korrekturen

- Das gemeinsame `Elf_Msg2`-Overlay (Actor 0173) war über seine verfügbare zusammenhängende Speicherlücke gewachsen. Dadurch konnten mehrere völlig verschiedene Figuren gemeinsam fehlen. Das war kein ausschließliches Gaster-Problem.
- Betroffen beziehungsweise reproduziert: die fünf Ergänzungen am Hyrule-Schloß (Yellow Guy, Marty, Doc, DeLorean, Mr. Beans Mini), Starwalker und N64 in Jabu-Jabu, Grenzposten auf Hyrules Ebene, Wario und Mystery Machine in Kakariko. Bei erwachsenem Kakariko scheiterte das Laden der Panzer am selben gemeinsamen Overlay.
- Gaster erhielt Actor 01AA mit eigener kleiner Modellbank. Die Panzer verwenden Actor 0180. Das gemeinsame Overlay schrumpft auf 59.088 Bytes; seine Figurengruppen und Auftrittsbedingungen bleiben erhalten.
- Ein separates Problem betraf Darunias normale Modellbank `OBJECT_DU`. Dort war zusätzlich das große Wallace-Weisenmodell enthalten. In Darunias Feuertempel-Räumen überschritt das Paket den reservierten Bereich um 23.664 Bytes. Der normale Darunia verwendet wieder sein kleines Originalpaket; Wallace als Weiser erhält eine eigene Bank. Der Türdurchgang bleibt auf festem Boden.
- In Kakariko bleibt wie gewünscht ein Panzer, an der flachen Parkposition. Andere Panzerplätze bleiben erhalten.
- Schutzprüfungen verhindern künftig eine Objekt-DMA über den reservierten Bereich hinaus. Diagnosezähler erlauben es, auch fehlgeschlagene Actor-Zuweisungen zu erkennen.

## Zusätzliche Änderungen

- Früher Gorone als Soldat mit der gelieferten Silent-Hill-Pistole am erwachsenen Gerudotal-Grenzposten. Dialog: „Ich bin total gespannt die Gerudo zu treffen. Die sind bestimmt total nett goro goro!“
- Thaddäus sagt „Algengrütze“.
- Starwalker im Wassertempel steht auf dem trockenen oberen Absatz in Raum 6, getrennt von Pepsiman, Fanboy, Chum Chum und Thaddäus; alle drei Wasserstände geprüft.
- Aus 5077 ist ausschließlich „Vorher hab ich Zeit zum Krabbeln“ entfernt. Übrige Seiten und Text-Steuerzeichen bleiben erhalten.

## Wo die gesuchten Figuren sind

Wario: nur als Kind in Kakariko, tagsüber und nachts, Position −900 / 80 / 950. Auf der Grasfläche an der Felswand bei einem Baum. Die Mystery Machine steht nahe dem Dorfeingang, ausschließlich als Kind mit gelerntem Regenlied. Ein per Debug veränderter Wasserstand allein ersetzt diese Lied-Voraussetzung nicht.

Ben 10: als Erwachsener im Gerudo-Trainingslager, Raum 3. Er ist im neuen Build sichtbar und ansprechbar. Game Boy Color und Game Boy Advance: derselbe Tunnel zum Deku-Baum, abhängig vom Alter; beide Modelle und Navi-Reaktionen geprüft.

## Prüfung und Grenzen

Alle Tests verwenden native 4 MiB ohne Expansion-Pak-Vergrößerung. Die Objektlisten wurden für Alter und Szenenaufbau geprüft: 610 Listen, keine Überschreitung in den vorgesehenen Zuständen, keine überfüllte Objekt-Slotliste. Laufende Tests kontrollieren außerdem Actor-Zuweisungen und Grafikpuffer. Der Auftrittsabgleich protokolliert platzierte und aktive Figuren samt Modell-Zeiger; erwartete Ausblendungen wegen Alter, Ausrüstung und Gaster-Zufall werden gesondert bewertet. Eine automatische Nahaufnahme kann durch die bestehende Raumgeometrie verdeckt sein und ersetzt keine Sichtprüfung.

Die Flammenderwische starten nach regulärem Türdurchgang in beiden Räumen. Ihr Siegesablauf wurde durch einen gezielt gesetzten Besiegt-Zustand des Kerns geprüft; das ist kein vollständig manuell gespielter Kampf. Der konkrete Zustand des früheren Nutzer-Spielstands wurde nicht rekonstruiert. Ein vollständiger Durchlauf des gesamten Spiels ist weiterhin nicht erfolgt.

Abgeschlossene Raum-/Altersfälle im aktuellen Auftrittsabgleich: 83/83. Zusätzliche abgeschlossene gezielte Prüfungen: 16/16. Einzelprotokolle und Prüfskripte liegen im Quellenarchiv unter `validation/proto-soldier-v68/`.
