# Robert Habeck in der Halle der Weisen

14 Nachrichten in diesem Kapitel, davon zwei neu gefaßte Kakariko-Texte aus dem früheren Kapitel. Insgesamt 596 bearbeitete deutsche Nachrichten. Alle bisherigen Modell- und Dialogänderungen sind enthalten.

Rauru wird durch das vom Nutzer gelieferte Habeck-Avatar ersetzt. 72835 Quelldreiecke werden auf 2341 reduziert; 24 Hauptgelenke erhalten ihre eigenen Abstände. Die Gesamtgröße wird gleichmäßig an die native Kamera angepaßt. Kein Überziehen auf Rauros breiten Körper und keine animierte Skalierung. Die erzeugten Körperbewegungen haben die ursprünglichen 27/30/30 Frames. Gesicht und Augen sind statisch texturiert; transparente Hornhaut und Wimpernkarten entfallen. Einzelheiten und Herkunft: models/habeck/README.md und provenance.json.

Die menschliche Erscheinung erklärt den tödlichen Sturz vom Todesberg, die Presseberichte, die solarbetriebene Geistereule, örtliche Energiegrenzen und Merz' Sperren. Es folgen Hallenmagie, Stasis von Held und Navi, Kleidung, Muskelerhalt, feuchte/verschimmelte Gegenstände, feste Zeitreise-Endpunkte und die stabile Zitadelle. Die Formulierung „Friedrich Merz erzählt“ wurde im Kontext als Habecks Rede verstanden. Die vorherigen Eulenauftritte bleiben Eulen; dort wird seine Identität weiterhin nicht verraten.

## Dialogablauf

Die lange erste Rede ist 704F → 0121 → 0122 → 0123. Die drei zusätzlichen Plätze waren unbenutzte Retail-Platzhalter. Die normalen TEXTID-Fortsetzungen halten die vorhandene Cutscene auf ihrem nativen Textwartepunkt. Es werden keine Kamera-/Szenen-/Fade-Timer verlängert. Durch die ausführliche Rede gibt es mehr manuell weitergeschaltete Seiten; bestehende feste Textzeiten bleiben unangetastet.

7051 enthält weiterhin die ursprüngliche Ja/Nein-Auswahl; 7052 springt weiter auf 7051 zurück. 7053 erläutert die Aufgabe. Lichtamulett, Animation-Cues, Rückkehr und native Zeitreise-Freigabe bleiben unverändert. Auch Amulett-Text 0040 und spätere Rede 7067 verwenden Habecks Namen.

Der Mann auf dem Aussichtsturm (EnHy Typ 12) ist in Kakariko nur beim erwachsenen Link vorhanden. Deshalb übernimmt der bereits in der Kindheit vorhandene Dachbewohner En_Ani den erlaubten Ersatz: 5050 tags, 5051 nachts. Seine Erwachsenen-, Masken- und Herzteil-Zweige bleiben erhalten. Es ist kein neuer NPC nötig. Insbesondere bleibt 0124 Navis ursprünglicher Wüstenkoloss-Text; kein Überschreiben benutzter Nachrichtenplätze.

## Prüfung und Grenzen

Generator: Schriftbreiten, Namensplatzhalter und Pufferbudgets geprüft. Alle 596 funktionalen Kontrollsequenzen mit Retail-Vorlagen verglichen; ausschließlich die drei ausdrücklich vorgesehenen TEXTID-Fortsetzungen kommen hinzu. Wahlreihenfolge, Rücksprung, Event-/Itemkontrollen und alle festen Verzögerungen bleiben gleich.

Build, PAL-Prüfsumme und Kompression aller 1509 Segmente geprüft. Vergleich mit der veröffentlichten Zeitübergang-Fassung: Änderungen auf object_rl, En_Rl und die deutschen Nachrichten sowie erforderliche Adreßdaten begrenzt. En_Rl ist nach Rücktausch der vier Modell-/Animationsnamen exakt quellgleich zur vorherigen Fassung. EnHy und En_Ani bleiben quellgleich. Bean- und Thaddäus-Objekte sind bytegleich zur vorherigen Fassung. RomPatcher.js wendet den BPS mit aktivierter Originalprüfung bytegleich zum Produktionsbuild an.

Die gezielte 4-MB-Prüfung startet an der Masterschwert-Aufnahme und läuft über den nativen Übergang in die Halle. Das Modell und ausgewählte Textseiten werden mit GLideN64, EnableClipping=True und EnableCustomSettings=False aufgenommen. Erreichter Ablauf, Nachrichten und Amulett-/Rückkehrnachweise sind unter validation/habeck/runtime-checks.json dokumentiert. Der Dachbewohner wird ausschließlich für die Aufnahme zum Spieler versetzt; sein Text wird mit normalen A-/Z-Tasten angenommen. Kindheit tags/nachts, Erwachsenen-Zweig und englische Gegenprobe sind getrennte Testfälle.

Der erste Modellversuch wurde wegen abgeschnittenen Kopfes verworfen und mit einheitlich kleinerer Gesamtgröße ersetzt. Frühe Zeugenstarts ohne passenden Kindheits-NPC bzw. mit einer unbrauchbaren Dachposition zählen nicht als bestandene Tests. Keine dieser Testabkürzungen steckt in der Produktions-ROM. Keine vollständige ROM oder Spielstände im Quellenarchiv.

Kein vollständiger Spieldurchlauf, kein Hardwaretest und keine Prüfung jedes späteren Weisen-Auftritts. Die Nein-/Wiederholungsroute, Maskenreaktionen und Herzteil-Vergabe sind durch unveränderte Steuerzeichen bzw. unveränderten Quellcode abgesichert und wurden nicht separat durchgespielt. Normale Spielstände können weiterverwendet werden; ältere Emulator-Save-States enthalten alte Daten.

Original-ROM: Europa/PAL 1.0, MD5 e040de91a74b61e3201db0e2323f768a. Ergebnis-SHA256: ca6a24dd31720c61afd4b22974d0dae9314f6eae0ecbd6fa37f1d9e9a2eccb22. Den BPS-Gesamtpatch direkt auf die unveränderte ROM anwenden.
