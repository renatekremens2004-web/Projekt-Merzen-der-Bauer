# Brunnen-Ergänzung und Schloßflucht – V27

Im unteren Abschnitt des Brunnens liegt eine kleine statische Anordnung der sechs hochgeladenen medizinischen DS-/PS1-Modelle auf einer vorhandenen roten Bodenfläche. Verwendet werden Leber, Lunge, Nierenpaar, Herz, beide Teile des Darms und das Auge mit seinem ursprünglichen Fortsatz. Keine neue Körper-, Wund- oder Blutgeometrie und keine Änderung der vorhandenen Raumtexturen. Größen an jungem Link orientiert: Lunge 12, Leber 8, Herz 4,5, Nierenpaar und Darm je 10 Spieleinheiten breit; Augenkugel 1,5. Jung-Link ist ungefähr 44 Einheiten hoch.

Standort: Bottom of the Well / Brunnen, Raum 1, (240, -720, -40). Alle Modell-Eckpunkte liegen über der vorhandenen roten Bodenfläche. Keine neue Kollision; Wege, Truhen und Schalter bleiben frei. Ein einziger zusätzlicher Elf_Msg2-Actor für die gesamte Anordnung, keine zusätzlichen Objektbank-Slots oder DMA-Einträge. Zusammen 1641 Dreiecke, Texturen maximal 64 Pixel, CI4 mit 16 Farben. Nur in der Kinderzeitlinie und deutscher Sprache sichtbar.

Mit Z anvisieren und C-oben Navis Kommentar aufrufen:

> Ohhh...nooooo....Lass uns bitte nicht zu viel Zeit hier unten verbringen, ja?

Eine Seite, manuell schließen, bei erneutem Anvisieren wieder abrufbar. Neue private Nachricht 71E4; alle vorhandenen Nachrichten bytegleich zu V26. Keine Veränderung der allgemeinen Textgeschwindigkeit oder Dialogabläufe.

## Pinguine während der Flucht

Skipper, Kowalski, Private und Rico samt Dynamit gehören ausschließlich zur normalen Szene INSIDE_GANONS_CASTLE (0x0D). Die Einsturz- und Fluchtszenen GANONS_TOWER_COLLAPSE_INTERIOR (0x0E), INSIDE_GANONS_CASTLE_COLLAPSE (0x0F) und GANONS_TOWER_COLLAPSE_EXTERIOR (0x1A) enthalten weder ihre Actor-Einträge noch ihre Modelle. Die Dynamit-Kulisse wird ausschließlich durch den jeweiligen Pinguin gezeichnet. Beim Wechsel in die Flucht sind daher Figuren und Dynamit weg. Keine zusätzliche Story-Markierung oder Änderung des Flucht-Timers nötig. Diese Trennung war bereits in V26 vorhanden und wurde jetzt ausdrücklich geprüft; kein vollständiger Flucht-Durchlauf als Test behauptet.

## Prüfung

Normal und DEBUG erfolgreich gebaut, N64-Prüfsummen geprüft. Beide BPS auf saubere PAL-1.0-ROM angewendet und bytegleich mit dem jeweiligen Build verglichen. ROM-Segmente gegenüber V26 geprüft, unveränderte Inhalte beziehungsweise ausschließlich erwartete Linker-Adreßänderungen außerhalb der Ergänzung. Vorhandene Actor-Einträge erhalten, native Elf_Msg2-Update-, Destroy- und Textfunktionen unverändert. Neue Nachricht paßt in den Textpuffer.

Gezielte Tests der fertigen Normal-ROM mit tatsächlich 4 MiB RAM: Kinder-Link im endgültigen Brunnenraum, Navis Kommentar zweimal anvisiert, gelesen und geschlossen, Actor danach weiterhin gültig, Spiel läuft weiter. Im geprüften Objektbereich 193456 Bytes Reserve. Erwachsener Link im selben Raum: Zusatzobjekt fehlt wie vorgesehen, Spiel läuft weiter. Keine Behauptung eines vollständigen Spieldurchlaufs. Screenshot stammt aus dem tatsächlichen Emulatorlauf und zeigt die Größen neben jungem Link.

## Anwendung

Normal ODER DEBUG auf eine unveränderte europäische PAL-1.0-ROM anwenden (MD5 e040de91a74b61e3201db0e2323f768a). Alle bisherigen Änderungen einschließlich V26 enthalten. Nicht auf bereits gepatchte ROM anwenden. DEBUG-Menü: L+R halten und Z drücken.

Quellenarchiv: nach allen bisherigen Buildern einschließlich build_penguins_v26.py und build_model_fixes_v26.py zuletzt tools/build_well_props_v27.py mit dem Decomp-Verzeichnis als Argument ausführen. Optionaler Neu-Export: tools/export_well_props_v27.py; die aufbereiteten JSON-Daten und Texturen sind bereits enthalten. PAL-1.0 mit COMPARE=0 bauen, DEBUG optional separat. Normalquellen und Normalbuild sind abschließend wiederhergestellt.

Prüfskripte und Ergebnisse in validation/well-organs-v27. Keine ROMs, Spielstände oder ausführbaren Testprogramme enthalten. Die Vorlagen stammen aus den hochgeladenen Dateien; daraus folgt keine zusätzliche Lizenz an diesen Vorlagen.
