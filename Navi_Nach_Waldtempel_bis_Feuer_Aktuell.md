# Navi: nach dem Waldtempel bis zum Feuertempel-Ende

Aktuelle Nutzerfassung: 01A3, 01A5, 01A7, 01A9, 0105 und 0152 überarbeitet. 0151 und 0120 unverändert. Gegnerbeschreibungen sind ausgenommen. {name} ist der gewählte Spielername. Als normaler Weg werden Fanghaken und Waldamulett vorausgesetzt; bei früher besorgten späteren Gegenständen kann die Hinweisfolge weiter springen.

## 0151 — Nach dem Waldamulett, vor dem Feueramulett

Normaler freiwilliger Story-Hinweis außerhalb der Dungeons. Keine feste Zahl von Zwischenrufen.

> Ey, ich werde wahnsinnig. Jetzt hat der Scheiß Friedrich Merz auch noch den Todesberg versaut!

> Das ist echt schlimm. Mann, da sieht man die Welt mit anderen Augen, was?

## 01A3 — Feuertempel: rollende Felsen, Raum 5

Freiwilliger örtlicher C-oben-Hinweis. Elf_Msg-Parameter BFA3.

> {name}, boah Junge, hörst Du diese Musik im Hintergrund? Ich weiß jetzt nicht genau, was das hier implizieren soll.

## 01A5 — Feuertempel: Aussicht auf Darunias Raum, Raum 10

Anvisierbarer Elf_Msg2-Hinweis, Parameter 3FA5.

> Hey, haben wir hier in der Nähe nicht den Alten da getroffen?

## 01A7 — Feuertempel: Statue, Raum 13

Freiwilliger örtlicher C-oben-Hinweis. Parameter BFA7.

> Oh Junge, nicht schon wieder eine von diesen beschissenen häßlichen Statuen.

> Wenn ich Augen hätte, bräuchte ich jetzt Bleichmittel, um die zu reinigen.

> Ich habe übrigens Augen. Man sieht sie nur nicht.

> Ich habe eine ganz interessante Feengestalt. Auch wenn Du mich vor allem als leuchtenden Ball wahrnimmst.

> Aber ich habe so was wie Fotorezeptoren. Ich sehe schon, was hier abgeht, ne?

> Ich bin jetzt nicht blind oder so. Das wollte ich nur mal klargestellt haben.

## 01A9 — Feuertempel: verrosteter Schalter, Räume 10 und 11

Automatischer örtlicher Hinweis, zweimal derselbe Text. Beide 13A9-Akteure benutzen den Schalterindex 19; sie sind keine zwei unabhängig garantierten Gespräche.

> Ja Junge, warum überrascht mich das nicht, daß hier auch wieder alles kaputtgespart wurde?

> Der Schalter ist ja komplett hinüber. Toll, Alter.

## 0105 — Feuertempel: Zeitblock-Symbole, Räume 1 und 11

Zwei anvisierbare Stellen, Text auch mit dem Waldtempel geteilt.

> Hey, da ist mal wieder einer von diesen Minecraft-Blöcken.

## 0152 — Nach dem Feueramulett

Nächster freiwilliger Story-Hinweis, wenn die Eisenstiefel noch fehlen. Kein eigener zusätzlicher Kommentar unmittelbar bei Volvagias Tod.

> So, alles klar. Schätze, als Nächstes müssen wir dann zu den Zoras.

> Da wird bestimmt alles in bester Ordnung sein. Ich wüßte nicht, warum dort irgendein Problem lauern sollte.

> Oder irgendeine Gefahr. Wir gehen da hin und kriegen dieses Amulett wahrscheinlich einfach direkt geschenkt.

> Ich glaube nicht, daß das in irgendeiner Form schiefgeht.

## Bedingter älterer Hinweis: 0120

Falls dieser einmalige freiwillige Erwachsenen-Hinweis bisher noch nicht abgerufen wurde, hat er Vorrang vor dem normalen Story-Hinweis. Er ist kein neuer Kommentar nach dem Waldtempel.

> Warte mal, mir fällt das jetzt erst auf, aber warum war König Zora so mega langsam?

> Gott, ich hoffe, der Typ ist in dieser neuen Zukunft tot!

Die generelle Ersatzzeile 015F ist kein zusätzlicher regelmäßiger Feuertempel-Kommentar. In der regulären Abfolge gilt vor dem Feueramulett 0151, anschließend 0152. Die Zahl der Navi-Rufe hängt von Spielzeit, Position, Fortschritt und Abrufen ab; die örtlichen Auslöser und Story-Prioritäten sind separat.

Geprüfte Quellen: src/elf_message/elf_message_field.c, QuestHint_GetNaviTextId, Elf_Msg/Elf_Msg2 und die nativen HIDAN-Raumlisten. Im Feuertempel liegen sieben Hinweis-Akteure mit fünf verschiedenen Text-IDs.
