# Initiale Exploration Zoom Maps

<!-- Hier alles aufschreiben, was interessant erscheint! -->

## Was sind die Ziele des Systems?
<!-- Snow Cards können bei diesem Schritt helfen! -->
- Bild anzeigen, heranzoomen
- Zoomverhalten aufzeichnen
- Probanden Funktionalität erklären

## Was ist der erwartete Input?
Input System:
- beliebiges Bild
- Zoomgeschwindigkeit (via Config File)
- haben die Probanden schon das Tutorial gesehen? (schließen, don't show me again)

Input Nutzer:
- Benutzung von Maustasten / Mausrad
- Tutorial bestätigen / überspringen / ignorieren

## Was ist der erwartete Output?
- Anzeigen des Bildes
- Anpassung des Blickfeldes unter Beachtung:
    - der Benutzerinputs
    - der Zoomgeschwindigkeit (config)
- Anzeigen des Tutorials / Nicht-Anzeige (bei vorheriger Bestätigung)
- Erhobene Daten an Speichermodul weitergeben

## Was sind Nomen Phrasen?
<!-- Alle relevanten Sachen aufschreiben, später kann aussortiert werden! -->
- "Zoom Maps" Tool
- beliebiges Bild
- Zoomgeschwindigkeit
- Möglichkeit des Zoomens
- Maustasten
- Mausrad

## Liste der Klassen:
<!-- Erstmal alle aufschreiben, dann auswählen! (Kriterien siehe Vorgehensweise) -->
<!-- Warum sind die Klassen existent? Wenn das zu beantworten ist - u good! -->
<!-- ausgewählte Klassen mit Link, andere einklammern und CRC-Karte löschen -->
<!-- - [Klassenname](crc-{klassenname}.md) -->
<!-- - (nichtAusgewählteKlasse) -->

<!-- - Zoomer (Input mit Config File zu Zoomwert konvertieren + Location + weitergeben)
- input aufnehmen (raw)
- input verrechnen (config + aktuelle position) (gibt weiter an Bild und Speichermedium) -->
<!-- - Umwandlung Benutzerinput in Zoomwert (Input -> Zoom -> Bild verändert sich -> Info Speichermedium weitergeben) -->
- [ZoomTutorial](crc-ZoomTutorial.md)
- [ZoomInput](crc-ZoomInput.md)
- [ZoomCalculator](crc-ZoomCalculator.md)
- [ZoomBild](crc-ZoomBild.md)
