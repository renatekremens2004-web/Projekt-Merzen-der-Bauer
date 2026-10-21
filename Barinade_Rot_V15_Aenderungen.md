# Barinade: rote Spritzer – V15

Barinades bestehende VA_BLOOD-Partikel und ihre Flecken am Boden sind rot statt grün: Environment-Farbe (0,100,0) → (100,0,0), Primärfarbe (0,150,0) → (150,0,0). Das betrifft auch dieselben vorhandenen Spritzer, wenn der Effekt außerhalb der finalen Explosion benutzt wird. Elektrische Effekte, übrige Effekttypen und andere Gegner bleiben unverändert.

Keine zusätzlichen Partikel, Texturen, Modelle oder Speicherbelegungen. Anzahl, Bewegung, Transparenz, Lebensdauer, Kampf und Todessequenz unverändert. Beide Builds geprüft: genau zwei Farbkonstanten-Instruktionswörter im Barinade-Overlay geändert, dessen Größe identisch bleibt. Sämtlicher übriger Code, Dialogtexte und Objektdaten bleiben bytegleich; nur ROM-Kopf/Kompressionstabelle können zusätzlich abweichen. Beide BPS mit RomPatcher.js gegen die geprüften Builds bytegleich verglichen. Reine Farbänderung; keine zusätzliche Emulatorprobe.

Alle bisherigen Änderungen inklusive V14 enthalten. Normal ODER DEBUG auf unveränderte europäische PAL 1.0 anwenden. DEBUG-Menü: L+R halten und Z drücken.
