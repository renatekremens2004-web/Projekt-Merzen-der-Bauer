# Wüstengäste, Jimmy und Mr. Mackey

Kumulativer Gesamtpatch auf unveränderte Europa/PAL 1.0. Vanilla-MD5 `e040de91a74b61e3201db0e2323f768a`; Ziel-SHA256 `55d2d55989441ef99221df41a7fcc34429c303bbb6d61e91dfe8fb7444488066`. Alle bisherigen Änderungen einschließlich Mystery Inc., Mystery Machine, Kenny und Naboo-Starfighter enthalten. BPS mit RomPatcher.js anwenden, normale Spielstände statt alter Emulator-Savestates laden. Deutsche Sprachfassung.

## Marty, Doc und Zeitreise

**Wüste ausschließlich als Erwachsener, Schloß ausschließlich als Kind.** Aus ihrer eigenen Perspektive treffen Marty und Doc Link zuerst als Erwachsenen am Geistertempel. Beide nennen ihn im neuen gemeinsamen Dialog Fremder. Marty schimpft über Merz, Doc beruhigt ihn und erinnert an die Mission. Am Schloß erkennt Marty später den jungen Link wieder, obwohl er bis dahin dessen ältere Version getroffen hatte. Der vorhandene Schloßdialog 71B4–71B7 bleibt in allen Sprachen bytegleich.

In der Wüste stehen Marty bei −100/−32/−200 und Doc bei 20/−32/−200, der DeLorean parkt seitlich bei −160/−31/−430. Alle vier Radpunkte liegen auf dem flachen Sandboden bei Y=−32. Tempelzugang und Warpstelle bleiben frei. Eine Ansprache beider Gesprächspartner startet dieselbe manuell bestätigte vierteilige Unterhaltung 71BF–71C2; kein Zeitreise-Auslöser und keine Quest-Funktion. Die Wüstenszene verwendet das bereits vorhandene OBJECT_BTTF, keine doppelten Marty-/Doc-/Autogeometrien.

An **beiden** Auftritten haben die drei Modelle jetzt gleichmäßig 85 Prozent ihrer bisherigen Größe: Marty rund **69,9**, Doc **77,5** Spieleinheiten hoch; DeLorean **170** lang und **51,4** hoch. Originale Körperproportionen bleiben erhalten. Fokus, Zylinder und Bodenschatten entsprechend angepaßt. Eigene Kopf-, Schulter- und Handgesten: versetzte Leerlaufphasen, kleine Gewichtsverlagerung, Nicken und unterschiedlich starke Armgesten beim jeweiligen Sprecher. Sanfte Wendung zu Link im Gespräch. Keine Skalierungsanimation, keine fremde Figur als Skelettvorlage.

## Neue Figuren

**Mauzi:** Pokémon Stadium 2 (N64), 699 Dreiecke, 24 Einheiten hoch. Nur als Erwachsener in Geistertempelraum 19, am freien Rand der unteren Treppenplattform bei 2050/843/510. Später Erwachsenenabschnitt, abseits von Truhen und Treppenweg. Kopf, Ohren/Münze/Schnurrhaare und Pfoten bleiben original; Arme einmal um eigene Schultern abgesenkt, danach kleine starre Gesten. Kein Gegnerverhalten, kein tatsächliches Stehlen von Rubinen.

**Jimmy:** Jimmy Neutron: Boy Genius (PC), originale 802 Dreiecke, 47 Einheiten einschließlich Haarlocke. Erwachsener äußerer Farmhof bei 850/0/−2850, außerhalb der Pferderennbahn. Tags und nachts vorhanden; keine Änderungen an Rennen, Epona, Toren, Luigi, Talon oder Malon. Besser aufgelöster Ausschnitt des eigenen Gesichtsatlasses; entspannte eigene Arme und kleine neugierige Kopf-/Handbewegungen. Die Erfindungen sind Dialoggags.

**Mr. Mackey:** South Park (N64), 266 Dreiecke, 74 Einheiten hoch. Nur als Erwachsener im Gästehaus in Kakariko bei −140/0/60. Originaler großer Kopf bleibt proportional, Arme abgesenkt, kleine nickende Gesten und sanfte Wendung zu Link. Normales Ansprechen; Kinderinstanz wird sauber entfernt. Die Figur steht abseits der zentralen Drehkamera und erscheint sowohl in der normalen Drehansicht als auch nach C-oben in der festen Hausansicht.

Drei eigene Objektdateien, jeweils nur im eigenen Raum bzw. den beiden Erwachsenen-Farmheadern geladen. Neue IDs am Ende der Objekttabelle, vorhandene IDs unverändert. Native Beleuchtung, Nebel und Tiefentest, kleine Bodenschatten. Zylinderradien 7/10/13, keine Gegner-/Angriffskollision. Die Körperhöhe wird mit dem erwachsenen Link und normalen NPCs im Spiel verglichen; Jimmy und Mauzi bleiben sichtbar kleiner als Erwachsene. Vier eigene starre Gruppen je Figur, ohne dynamische Netzstreckung.

## Dialoge

Neue private IDs 71BF–71C5; normale A-bestätigte Seiten, keine festen Lesezeiten. Alle bisherigen Nachrichten in allen drei PAL-Sprachen als Quelle und kompiliert unverändert.

**71BF**

Marty: Hey, Fremder! Bist Du auch wegen Friedrich Merz hier?

Marty: Der Typ ist ein ganz mieser Kerl. Und eine feige Sau! Mann, das ist doch der reinste Albtraum!

**71C0**

Doc: Ruhig, Marty! Unserem fremden Freund hilft es wenig, wenn Du hier die ganze Wüste anschreist.

**71C1**

Marty: Schon gut, Doc. Aber der Kerl macht dieses ganze Land fertig! Das ist echt stark... im übelsten Sinne.

**71C2**

Doc: Grundgütiger, Marty! Denk an unsere Mission. Wir werden das Ganze schon wieder ins Lot bringen.

Doc: Und Du, Fremder: Sei vorsichtig. Bei diesem Mann ist selbst die Zukunft keine sichere Sache.

**71C3**

Ich bin Mauzi! In diesem Tempel gibt's bestimmt große Beute!

Diese goldenen Statuen! Die ganzen Schatztruhen! Da kribbelt mir das Münzchen auf der Stirn!

Du kümmerst Dich um Friedrich Merz, ich mich um den Reichtum. Ein genialer Plan, miuaz genau!

**71C4**

Ich bin Jimmy Neutron, junges Genie! Ich hatte einen GEDANKENBLITZ!

Jetzt helfe ich Luigi auf dieser Farm mit meinen neuesten Erfindungen!

Mein automatischer Milchsortierer erkennt Vanillemilch, Schokomilch und... normale Milch. Noch bevor man sie hergestellt hat!

Das mit der explosionsfreien Inbetriebnahme krieg ich auch noch hin. Wissenschaft braucht eben Zeit!

**71C5**

Ich bin Mr. Mackey, mhhkay? Und ich bin NICHT Friedrich Merz!

Nur weil jemand einen großen Kopf und wenig Haare hat, ist er doch nicht gleich dieser Kerl, mhhkay!

Gestern hat mich einer nach Steuersenkungen gefragt. Ich bin Schulberater, mhhkay!

Dieses ständige Verwechseln ist nicht okay. Also wirklich nicht okay, mhhkay.

## Prüfungen

Zwölf gezielte Emulatorproben mit echten 4 MiB: Wüstengespräch aus zwei Annäherungsrichtungen bis zum normalen Ende, unveränderte Schloßunterhaltung mit neuer Bewegung/Größe, Mauzi, Jimmy und Mackey bis zur letzten Seite, Jimmy nachts, kein Wüstenauftritt als Kind, kein Mackey als Kind, speicherkritischster Schattentempelraum 9 sowie beide nativen Kameraperspektiven des Gästehauses und eine zusätzliche seitliche Aufnahme von Mackey. Altersgrenzen aller drei neuen Figuren zusätzlich im gemeinsamen Init geprüft; Jimmy steht ausschließlich in den Erwachsenen-Tag-/Nachtlisten. Reale Controller-Eingaben, keine verschobenen Produktions-Actors oder nachbearbeiteten Screenshots. Testspielstände überspringen nur den Weg zu den Szenen. Keine fehlgeschlagenen nativen Speicherbelegungen, Grafikpufferüberläufe oder beschädigten GfxPool-Marken. Mindestreserve in diesen Proben: größte freie zusammenhängende Arena-Fläche 54,960 Byte; Objektpuffer 27,680 Byte. Kein vollständiger Durchlauf oder echter Hardwaretest.

Statischer Objekt-Audit der betroffenen Header mit ihrem tatsächlich benutzten Link-Alter und nativen Keep-Modellen: alle innerhalb des unveränderten 1.019.904-Byte-Puffers und maximal 19 Slots. Nicht benutzte Erwachsenen-/Kind-Kombinationen sowie unveränderte Credits-Header werden nicht als spielbare Räume bewertet. Die größte geprüfte Objektliste bleibt der frühere Schloßauftritt mit 992.224 Byte; Wüste 956.928 Byte. Keine Vergrößerung von Spiel-/Raumspeicherzuteilungen. Nur zusätzliche Actor-/Objekt-Einträge, native Kollision und Rätsellogik unverändert.

1.520 komprimierte Segmente gegen den unkomprimierten Build und CIC-6105-Prüfsumme geprüft, 3.664 Kernsymbole unverändert oder ausschließlich durch echte Linker-Relokationen verschoben. ElfMsg2: vier neue streng auf die neuen Szenen begrenzte Funktionen, Init/Update/Destroy-Zweige und überarbeitete BTTF-Helfer; sämtliche anderen bisherigen Sonderfunktionen unverändert. Alle 1.049 eigenen Texte passen in die nativen Textpuffer. Neue Nachrichten besitzen korrekte Folge-DMA-Zeiger in allen drei Sprachen. BPS mit RomPatcher.js und aktiver Quellvalidierung angewandt: bytegleich zur geprüften Ziel-ROM.

**Letzter Builder:** `python3 tools/build_desert_guests.py /pfad/zur/oot-decomp` nach `build_mystery_machine.py`. Anschließend regulärer PAL-1.0-Bau und Kompression. Vorbereitete JSONs und models-Texturen genügen. Optionaler Original-Export `python3 tools/export_desert_guests.py WORK`, Nutzerdateien unter WORK/input/meowth, jimmy, mackey. Sichere Originalmodelle und Quellenhinweise unter models/KEY/source; Builder-Ausgangszustände unter tools/originals/desert-guests. Quellenpaket enthält keine ROMs, Saves, Savestates, RAM-Abzüge oder ausführbare Programme. Bilder sind unveränderte echte Emulatoraufnahmen der angegebenen Ziel-ROM.
