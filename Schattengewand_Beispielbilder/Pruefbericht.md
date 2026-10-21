# Schattengewand im Brunnen

Kumulativer Gesamtpatch für die unveränderte Europa/PAL-1.0-ROM. Original-MD5 `e040de91a74b61e3201db0e2323f768a`, Ziel-SHA256 `0c717a4d2b8746f749707b098a51b009014b5c0f72fb97b7d0e1c3560c635332`. Alle bisherigen Figuren, Räume, Dialoge und Schnellstiefel enthalten. Deutsche Sprache wählen und BPS mit RomPatcher.js anwenden.

## Verhalten

Eine zusätzliche große Truhe steht in Raum 3 des Brunnens, auf der festen nordwestlichen Seitenplattform im Raum mit Beamos, Fledermäusen und unsichtbaren Gruben. Position 880/0/-1230, Drehung 180 Grad für eine saubere native Fundkamera innerhalb des Raums. Sie belohnt Erkundung abseits des Eingangs und ersetzt keine vorhandene Belohnung. Auge der Wahrheit, Schlüssel, alle 13 bisherigen Truhen, Türen, Gegner, Wege und unsichtbare Gruben bleiben erhalten. Die neue Truhe hat keinen zusätzlichen Kompaßmarker.

Beim tatsächlichen Erhalt wird das Schattengewand sofort angelegt. Der vorhandene grüne Kokiri-Platz wird dauerhaft aufgewertet: Vor dem Fund grün, danach bei Kind und Erwachsenem schwarz. Beide gespeicherten Altersausrüstungen werden beim Erhalt einmal auf den normalen Gewandslot gesetzt; andere Ausrüstung und Buttons bleiben erhalten. Kein automatischer Erwerb durch Installation des Patches. Bereits bestehende normale Spielstände können die neue Truhe ebenfalls noch finden.

Die neue Schadenshalbierung gilt ausschließlich, solange das Schattengewand ausgerüstet ist. Das orange Feuer- oder hellblaue Wassergewand schaltet diesen Gewandschutz aus; Zurückwechseln aktiviert ihn wieder. Die ursprüngliche spätere Feen-Abwehr bleibt eine unabhängige Fähigkeit. Beide Schutzquellen ergeben zusammen keine Viertelung. Heilung bleibt unverändert. Die ursprüngliche Rundung erhält mindestens einen Gesundheitspunkt Schaden; sofortige native Todesfälle wie abgelaufene Ertrinkungs-/Hitzetimer bleiben tödlich. Keine neue Unverwundbarkeit und keine Änderungen an Gegnern oder deren Angriffen.

Das hochgehaltene Gewandmodell ist schwarz. Fund- und Ausrüstungsicon sind vor dem Erwerb grün und danach schwarz; auch Links Modell in der Ausrüstungsansicht verwendet die neue Farbe. Die Ausrüstungsplatz-/Namensgrafik bleibt der native Kokiri-Platz, der Fundtext nennt es Schattengewand. Feuer- und Wasserfarben sowie die gemeinsam benutzte Farbpalette anderer NPCs bleiben unverändert.

[Fundtext](../Schattengewand_Fundtext.md).

## Technische Begrenzung der Änderung

Eigener angehängter Get-Item-Eintrag 0x7E und Darstellungs-ID 0x75. Alle bisherigen 125 Gegenstandseinträge bleiben bytegleich. Die neue Belohnung verwendet die vorhandene Gewandgeometrie und zwei kleine eigene Materiallisten: zusammen 64 zusätzliche Objektbytes. Kein neues Charaktermodell, kein weiterer Raum-Objektplatz; OBJECT_BOX war bereits geladen. Fund- und Pauseicons werden nach dem nativen DMA einmal im vorhandenen 32×32-RGBA-Puffer abgedunkelt, mit unverändertem Alphakanal und Cache-Writeback. Keine zusätzliche Textur oder vergrößerten Speicherpools.

Eigenes reserviertes infTable-Bit 0x1CE für den dauerhaften Erwerb; das Nachbarbit 0x1CF bleibt Navis bereits bestehende Gehört-Markierung. Unbenutzte Brunnen-Truhenflag 0, sämtliche ursprünglichen Flags erhalten. Save-Struktur, SRAM-Slots, Sicherungskopien und Prüfsummenbereiche bleiben unverändert. Die neue Truhe ist ausschließlich in der deutschen Modfassung aktiv. Alle vorherigen Texte bleiben in allen drei Sprachen bytegleich; allein neue Nachricht 71DC ergänzt vier manuell weitergeschaltete Seiten. Insgesamt 1.155 eigene deutsche Nachrichten. Keine veränderten festen Lesezeiten.

## Nachweise

PAL-Build und Kompression erfolgreich. Differentialprüfung von 1.524 Segmenten und 4.305 bestehenden Symbolen: nur die angegebenen Truhen-/Get-Item-/Farb-/Icon-/Schadensstellen verändert. Die wenigen angepaßten GI_MAX-Grenzwerte für fangbare Flascheninhalte werden mitgeprüft. Alle übrigen Unterschiede sind echte Linker-Relokationen. Alle 1.155 eigenen Textpuffer geprüft. Native Geometrie und 13 bisherige Brunnen-Truheneinträge erhalten; 25 Punkte des neuen Truhenfußabdrucks und neun Punkte des Öffnungsstandorts liegen auf festem Boden.

Hosttests mit tatsächlich extrahierter Spielberechnung: 3.456 Schadensfälle und 40 Ausrüstungsfälle für beide Altersstufen, alle drei Gewänder, Erwerb an/aus und ursprüngliche Feen-Abwehr an/aus. Heilung, Nullschaden, Mindestschaden, tödlicher Schaden und Nichtstapeln geprüft. Nur die vorgesehenen Gewandnibbles und das eigene Erwerbsbit ändern sich; andere Ausrüstung und das Navi-Bit bleiben erhalten. Der separate Icon-Test prüft 2.048 echte/synthetische Pixel auf erhaltenes Alpha, einfarbige dunkle Werte, korrekten Cache-Writeback und unverletzte Puffergrenzen. Hosttests ersetzen keine Laufzeitprobe.

Gezielte Emulatorproben der finalen ROM mit echten 4 MiB sind im beiliegenden runtime-verification.json einzeln aufgeführt. Die Truhe wird über normale Controller-Eingaben geöffnet, alle vier Fundtextseiten laufen durch, das Gewand wird angelegt und danach ist normale Bewegung möglich. Native Pause-Speicherung wurde ausgeführt; tatsächlicher SRAM-Hauptslot und Sicherungskopie haben gültige Dateikennung, passende Prüfsumme, Erwerbsbit und gespeicherte geöffnete Truhe. Ein echter Neustart lädt diese SRAM-Datei über Titel und Dateiauswahl ohne SaveContext-Injektion; Gewand und Truhenflag bleiben erhalten. Getrennte Alters-/Gewandproben sind nachvollziehbar als Testspielstand-Forks beschrieben, die eigentliche Sieben-Jahre-Zeitreise wurde hier nicht durchgespielt. Die natürlichen Gegnerproben sind wegen abweichender Treffer-/Rückstoßabläufe kein kontrollierter 1:2-Vergleich; die exakte Berechnung wird durch die Hosttests belegt. Kleinste gemessene zusammenhängende Arena-Reserve 67,120 Byte, kleinste Objektpufferreserve 101,952 Byte. Keine fehlgeschlagenen Speicherbelegungen oder Grafikpufferüberläufe. Kein vollständiger Spieldurchlauf oder Hardwaretest.

Die Bilder sind unveränderte Emulatoraufnahmen der finalen Ziel-ROM. Keine Produktionsakteure oder Gegner wurden für Bilder entfernt oder versetzt; direkte Testspielstand-Einstiege sind im Prüftreiber dokumentiert. Die Gegner im Truhenraum bleiben aktiv und können nach der Fundszene weiter angreifen.

BPS mit RomPatcher.js und aktiver Quellvalidierung auf die Vanilla-ROM angewandt: Ergebnis bytegleich zur geprüften finalen ROM.

## Reproduzieren

Nach den bisherigen Modell-/Raum-Buildern zuletzt build_desert_guests.py, build_gerudo_dialogue.py, build_twinrova_title.py, build_doof_guests.py und build_shadow_tunic.py ausführen, anschließend normaler PAL-1.0-Build und Kompression. Der neue Builder enthält unveränderte Ausgangsdateien unter tools/originals/shadow-tunic. Quellenpaket ohne ROM, Save, Savestate, SRAM-Abzug, ELF oder ausführbare Dateien. Für Laufzeitproben eigene Testspielstände verwenden; die Prüfskripte dokumentieren deren gezielte Zustände und Eingaben.
