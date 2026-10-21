# Schloß- und Wald-Dialoge V8

30 deutsche Text-IDs nach den neuen Vorgaben geändert: Eule und Wiederholungsfrage; Malon und Mario mit Milchbestellung, Eiern, fehlender Kappe und Impostor-Syndrom; Zelda mit Albtraum, Wunscherfüllmaschine und unauffälligem Spähen; Mr. Beans Kakariko-Verweis; Maskenwunsch der Bergwache; Mido-Sprüche; Salias Blutgruppen-Lied und die frühen Wald-Erklärungen.

Die beiden nachgereichten Korrekturen sind enthalten: 0101 hat den C-/Netz-Reim mit dynamischem Spielernamen und C-hoch-Symbol für den Blick. Nietzsche wird in der Schöpfungs-Erzählung nur einmal erwähnt, in 1029. In 108A steht nur noch, daß die Göttinnen die Welt verließen. FADE(90) bleibt dort erhalten.

## Zuordnung

702A ist Marios Schlaftext. Die versehentlich genannte 7024 gehört dem Bewohner mit dem Überdosis-Spruch; diese ID bleibt unverändert. In 2015 hat die Wache den Brief bereits gesehen. Daher ist die Pikachu-Maske ausdrücklich optional und er fordert keinen zweiten Brief.

Die Frage 2066 lautet jetzt, ob die Eule sich wiederholen soll. Entsprechend steht Ja auf dem nativen Wiederholen-Zweig (Index 0), Nein auf dem Weiter-Zweig (Index 1). Keine Änderung an der Auswahlmechanik.

10C0–10C7 gehören tatsächlich der Eule. Der Flug-Witz ist deshalb bei ihr geblieben. Den Feenkörper-/Lungen-Witz in 10C5 gibt sie ausdrücklich als Einwurf von Navi wieder. Keine Umstellung des Szenenablaufs oder der Sprecher-Akteure. Salias Blutgruppen-Erklärung steht in 10A8; ihr Lied behält alle bisherigen Spieleffekte und das normale Lernverfahren.

## Prüfung

Normale und DEBUG-ROM erfolgreich gebaut und mit gültiger N64-Prüfsumme versehen. Alle bearbeiteten Nachrichten passen in die nativen Rohtext- und Seitenpuffer. Namensfelder, SFX, Ereignisabschlüsse, direkte Fortsetzungen und alle festen Einblend-/Seitenverzögerungen erhalten. Nicht geänderte Seiten, alle anderen Text-IDs und alle anderen Sprachen bleiben erhalten. Keine Verlängerung der Cutscene- oder Lesezeiten. Manuell weitergeschaltete neue Texte werden nach PAL-Zeichenbreiten auf bis zu vier Zeilen je Seite verteilt.

Dekomprimierte Spielsegmente gegen V7 verglichen: eigentliche Änderungen nur deutsche Nachrichtendaten und deren Zeiger. Andere Adreßänderungen gegen explizite Linker-Relokationen geprüft. Modelle, Kollisionen, Animationen, Speicherpools, Kampflogik und die Zustandsmaschinen für Dialoge/Gegenstände bleiben erhalten.

Zwei Laufzeitproben der endgültigen normalen ROM mit tatsächlichen 4 MiB: Malon spricht den neuen Dialog und übergibt das Ei mit dem nativen Fortschrittsflag. Die Eule bietet die neue Frage zweimal an: erst Wiederholen, dann Weiter; beide Zweige funktionieren. Nur Anfangs-Spielstand/Spielerposition vorbereitet, keine NPCs versetzt und keine Textzustände oder Timer erzwungen. Kein vollständiger Kapitel- oder Spieldurchlauf.

Beide BPS mit RomPatcher.js und aktiver Quellvalidierung angewandt und byteweise mit ihren Ziel-ROMs verglichen. Downloads nach Veröffentlichung separat geprüft.

## Anwendung

Einen der kumulativen Gesamtpatches auf die unveränderte Europe/PAL-1.0-ROM anwenden. Original-MD5 e040de91a74b61e3201db0e2323f768a. Deutsch wählen. Alle bisherigen Änderungen sind enthalten. Die Debugfassung bietet dieselben Inhalte und die bisherige Steuerung (L+R halten, Z drücken).

## Quellen

Letzter normaler Builder: tools/build_castle_dialogue_v8.py nach build_kokiri_dialogue_v7.py, vor optional build_debug_version.py. Neue Vorgaben in tools/castle_dialogue_v8.json; kanonische Ersatztexte in story/*.json. Die Textfunktion unterstützt die gezielt freigegebene Neugliederung manueller Zelda-Seiten sowie der manuellen Seiten nach der unveränderten Verzögerung in 10C4. Quellarchiv enthält den kumulativen Quellenstand und Prüfungen, keine ROM/Saves/ELF/ausführbaren Programme.

Größter geänderter Rohtext: 1130 von 1280 Bytes; größte dekodierte Seite (konservative Obergrenze): 143 von 200 Bytes.
