# Navi: nach dem Waldtempel bis zum Feuertempel-Ende

Vorheriger Iststand aus der veröffentlichten Wasser-/Geisterweisen-Fassung. Gegnerbeschreibungen sind ausgenommen. {name} ist der gewählte Spielername. Als normaler Weg werden Fanghaken und Waldamulett vorausgesetzt; bei früher besorgten späteren Gegenständen kann die Hinweisfolge weiter springen.

## 0151 — Nach dem Waldamulett, vor dem Feueramulett

Normaler freiwilliger Story-Hinweis außerhalb der Dungeons. Keine feste Zahl von Zwischenrufen.

> Ey, ich werde wahnsinnig. Jetzt hat der Scheiß Friedrich Merz auch noch den Todesberg versaut!

> Das ist echt schlimm. Mann, da sieht man die Welt mit anderen Augen, was?

## 01A3 — Feuertempel: rollende Felsen, Raum 5

Freiwilliger örtlicher C-oben-Hinweis. Elf_Msg-Parameter BFA3.

> {name}, ich kann unter uns Stimmen von Goronen hören.

## 01A5 — Feuertempel: Aussicht auf Darunias Raum, Raum 10

Anvisierbarer Elf_Msg2-Hinweis, Parameter 3FA5.

> Schau hier herunter... Ist das nicht der Raum, in dem wir Darunia getroffen haben?

## 01A7 — Feuertempel: Statue, Raum 13

Freiwilliger örtlicher C-oben-Hinweis. Parameter BFA7.

> Diese Statue... Haben wir sie nicht schon an anderem Orte  gesehen?

## 01A9 — Feuertempel: verrosteter Schalter, Räume 10 und 11

Automatischer örtlicher Hinweis, zweimal derselbe Text. Beide 13A9-Akteure benutzen den Schalterindex 19; sie sind keine zwei unabhängig garantierten Gespräche.

> Der Schalter sieht verrostet aus.

## 0105 — Feuertempel: Zeitblock-Symbole, Räume 1 und 11

Zwei anvisierbare Stellen, Text auch mit dem Waldtempel geteilt.

> Na, an was erinnert Dich dieses Symbol?

## 0152 — Nach dem Feueramulett

Nächster freiwilliger Story-Hinweis, wenn die Eisenstiefel noch fehlen. Kein eigener zusätzlicher Kommentar unmittelbar bei Volvagias Tod.

> Der Wind vom Zora-Fluß ist eisig. Mit diesem Wasser stimmt etwas nicht. Ich fürchte, das ist mehr als schlechtes Wetter.

## Bedingter älterer Hinweis: 0120

Falls dieser einmalige freiwillige Erwachsenen-Hinweis bisher noch nicht abgerufen wurde, hat er Vorrang vor dem normalen Story-Hinweis. Er ist kein neuer Kommentar nach dem Waldtempel.

> Warte mal, mir fällt das jetzt erst auf, aber warum war König Zora so mega langsam?

> Gott, ich hoffe, der Typ ist in dieser neuen Zukunft tot!

Die generelle Ersatzzeile 015F ist kein zusätzlicher regelmäßiger Feuertempel-Kommentar. In der regulären Abfolge gilt vor dem Feueramulett 0151, anschließend 0152. Die Zahl der Navi-Rufe hängt von Spielzeit, Position, Fortschritt und Abrufen ab; die örtlichen Auslöser und Story-Prioritäten sind separat.

Geprüfte Quellen: src/elf_message/elf_message_field.c, QuestHint_GetNaviTextId, Elf_Msg/Elf_Msg2 und die nativen HIDAN-Raumlisten. Im Feuertempel liegen sieben Hinweis-Akteure mit fünf verschiedenen Text-IDs.
