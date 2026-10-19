# Erwachsene Zoras, Eishöhle und Eisenstiefel-Schnellwechsel

Gesamtpatch mit allen bisherigen Modellen, Kapiteln, Wallace und korrigierter Credits-Sitzpose. 15 deutsche Nachrichten gegenüber der Feuertempel-Fassung geändert, insgesamt 989 eigene Nachrichten. Native IDs, Auswahl-/Quest-/Liedsteuerung und feste Zeiten erhalten. Nur manuell weitergeschaltete Seiten verlängert; Layout mit längstem erlaubtem Spielernamen und sämtliche Textpuffer geprüft. Englisch/Französisch unverändert.

## Dialoge und Platzierung

Die Zora aus dem Hylia-See (ursprünglich EnZo-Typ 6, Kindtext 4020) ist nun als erwachsene Frau glücklich mit ihrer Identität und dankt dem Spieler. Genau eine markierte native EnZo-Instanz (7FC6) am trockenen alten Stand-Zora-Absatz in Zora-Reich-Raum 1: −786/14/−486, geprüfter Boden 14. Nur erwachsen/deutsch; die Kinder-Zora am See bleibt unverändert. Ein Actor-/Objekteintrag im regulären Erwachsenen-Header hinzugefügt (tags/nachts gemeinsam). Native Zora-Geometrie, Animationen, Kollisionsdaten und Proportionen unverändert. Im Englischen wird die zusätzliche Instanz vor ihrem Modellaufbau entfernt. Alle 72 ursprünglichen Assets des Raums und die bisherigen Einträge bleiben erhalten.

König Zora bekommt Klimaanlagen-/Fischnasen-/Ruto-Warte-/Eiszeit-Texte. Native Rüstungsübergabe 4012, Bereits-vorhanden-Variante 401F mit 4013-Fortsetzung und reguläres Tauschgeschäft bleiben erhalten. Erst nach dem nativen Dank-/Rüstungsflag 139 wird auf die Folgegespräche verzweigt: 4045 vor, private 4044 nach dem Wasseramulett. Dadurch überlagert der neue Fluch-Abschlußtext weder das Geschenk noch die Rezept-Abgabe. Nach dem Wassertempel wartet der König vergeblich aufs Auftauen; der Schauplatz wird nicht künstlich aufgetaut. Der Abfluß-Spruch steht bei König/Sheik. Die beiden optionalen Morpha-/Kloaken-Gags sind mangels weiterer vorhandener Erwachsenen-Zoras nur in planning/ZORA_GAGS_RESERVE.md vorgemerkt.

Sheik in der Eishöhle: Eis/Fleiß, Merz/Bockshorn, Erz vom Todesberg, faltbare Harfe in der Arschtasche und die Hosentaschen-Anspielung. Native Serenaden-Cues, Kamera, Vorspiel, Nachspiel und Liedfreigabe unverändert. Sonnenrätsel 021F nennt unmittelbar den Pfeilschuß auf die aufgehende Sonne; ursprüngliche Tageszeit-/Wasser-/Trefferbedingungen für Feuerpfeile bleiben erhalten.

Navi: 0180 Silberrubin-Schrott; 0189 zuerst falsche Behauptung übers Auftauen nach dem Wassertempel, dann ausdrücklicher Widerruf „nur für den Gag“ und Aufforderung, den Fischkönig wirklich aufzutauen; 01AB Wasserschlangen-Karte und übertriebene Boss-Vorfreude; 0154 zurück nach Kakariko und Mühle versauen. 0152/0153/0105/015F bleiben bytegleich. Die tatsächlichen Navi-Texte und Auslöser stehen in planning/NAVI_ZORA_EIS_WASSER_AKTUELL.md.

## Himmelblau und Steuerkreuz unten

Getragene Zora-Tunika RGB 110/195/240 (#6EC3F0), weiches helles Himmelblau unter der jeweiligen nativen Beleuchtung. Kokiri-Grün und Wallace-Orange unverändert. Keine Änderung von Inventar-ID, Unterwasserfunktion oder Tunika-Texturen. Ursprüngliche Gerudo-Renderer und Modelle unverändert; der native PAL-1.0-Farbeffekt durch geerbte Zeichenfarbe bleibt erhalten. Ein Gerudo-Sichttest mit den neuen Farben ist noch nicht durchgeführt.

Steuerkreuz unten: einmal drücken = Eisenstiefel, erneut drücken = Kokiri-Stiefel. Himmelsstiefel werden beim Einschalten ebenfalls durch Eisen ersetzt; ausgeschaltet wird auf normale Stiefel. Nur Erwachsene mit bereits besessenen Eisenstiefeln. Nur Druckflanke; Gedrückthalten wiederholt nicht. Keine Umschaltung im Dialog, Pausenmenü, Game-over, Zwischensequenz, Szenenübergang oder beim Reiten. Die native Inventory_ChangeEquipment-/Player_SetEquipmentData-/Player_SetBootData-Kette übernimmt Inventar, Modell und Physik; der normale currentBoots/prevBoots-Wechsel verarbeitet Sinken und Wiederauftauchen. Keine neuen Items oder Actor-Felder. Die Farb-/Stiefeländerung gilt sprachunabhängig.

## Prüfung

Finale ROM-SHA256: `e44dd3285ef564fce5bdec9f74ccb53ca267486afbefde0e898acb8e038858ff`. 32 MiB, CIC-6105. Alle 1509 komprimierten Segmente mit dem Neubau verglichen. 989 Textpuffer innerhalb ihrer Grenzen. 2954 Kernfunktionen, 545 native Player-Funktionen, 20 König- und 25 Zora-Funktionen abseits der dokumentierten Hooks erhalten; Originalbytes oder echte MIPS-Relokationen geprüft. Insbesondere native Ausrüstungs-/Bootsphysik-/Rüstungs-/Froschübergabefunktionen bleiben erhalten. Alle früheren anderen Modelle und Szenen unverändert oder nur neu gelinkt.

Gezielte abgeschlossene Mupen64Plus/GLideN64-Proben auf dieser finalen ROM mit tatsächlichen 4 MiB RAM:

- Eisenstiefel an Land: vier Druckflanken, erster Druck lange gehalten, nur je ein Wechsel.
- Im festen Wassertempel-Eingangsbecken: mit Eisenstiefeln Boden 620 erreicht, ohne Stiefel wieder aufgestiegen; kein direkter Physik-/Stiefelzustand im Test gesetzt.
- Negativproben ohne Besitz, als Kind mit vorbereitetem Besitz und bei offenem nativen Pausenmenü: kein Wechsel.
- Zora-Wiedersehen mit drei Gesprächsseiten und D-pad-Eingaben während des Dialogs; kein Stiefelwechsel. Englische Gegenprobe ohne zusätzliches Gespräch.
- König vor/nach Wasseramulett, alle fünf Geschenkseiten mit anschließend tatsächlich erhaltener Zora-Rüstung und gesetztem Besitz; Bereits-vorhanden-Variante samt Folgegespräch; Rezept regulär abgegeben und Augenfrosch erhalten.
- Vollständige Serenadenrede, mit normalen Tasten nachgespielt und gelernt, Abschied wieder im Spiel. D-pad während der Zwischensequenz bleibt ohne Ausrüstungswechsel.
- Nativer Blaues-Feuer-Hinweis mit vollständigem Widerruf und nativer Sonnenrätsel-Text gelesen. Die Texte 0180 (Silberrubine) und 01AB (Strudelgang) sind statisch geprüft; ihre lokalen Auslöser wurden in diesen Proben nicht erfolgreich vorgeführt.

Die gesonderte Silberrubin-Probe erreichte 0180 nicht: Der native Tag liegt in einem schmalen Höhenband (Y 9 bis unter 17), der vorbereitete Spieler stand dort auf Bodenhöhe 19. Der ursprüngliche Auslöser wurde nicht verändert; diese Probe zählt nicht als bestanden. Frühere abgebrochene/ungeeignete Vorproben werden ebenfalls nicht als bestanden gezählt. Keine vollständige Dungeon-/Tauschquest-Durchspielung und kein N64-Hardwaretest. Die PNGs sind unveränderte tatsächliche Emulatoraufnahmen. ROM, private Spielstände, Speicherabbilder und ausführbare Programme werden nicht veröffentlicht.

BPS mit RomPatcher.js und aktiver Quellprüfung auf Original-MD5 e040de91a74b61e3201db0e2323f768a angewandt; Ergebnis bytegleich zur final geprüften ROM. Direkt auf die entpackte unveränderte Europa/PAL-1.0-Original-ROM anwenden, normale Spielstände statt alter Emulator-Save-States verwenden.
