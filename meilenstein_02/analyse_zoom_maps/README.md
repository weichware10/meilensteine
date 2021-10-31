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

---
# Analyse - Zoom Maps
<!-- Hier Notizen zum Denkprozess! -->
Nutzerinputs werden in ZoomInput aufgenommen und an ZoomCalculator weitergegeben, wo die Inputs mit Hilfe von Informationen aus dem Config-Modul verarbeitet werden. Die verarbeiteten Daten werden an das Speichermedium weitergegeben, sowie an ZoomBild, wodurch das Bild (aus Config vorgegeben) entsprechend verändert wird.
Einstellungen des Tutorials werden im Config-Modul gespeichert.

## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
- ZoomInput:
     - Input aufnehmen
- ZoomCalculator:
     - Input von ZooomInput verrechnen
- ZoomBild:
     - Errechnete Aktion von ZoomCalculator umsetzen, Bild darstellen
- ZoomTutorial:
     - Zeigen eines Tutorials, Input bezüglich wiederholter Anzeige an CFG-Modul senden


## Kollaborationen
<!-- Benutzeranfragen an Dienste, die benötigt werden um Veranwortlichkeiten zu erfüllen -->
<!-- enthüllen Kontroll- und Informationsflüsse, und somit Subsysteme -->
<!-- Können fehlende Verantwortlichkeiten offenbaren, bzw. fehlerhaft zugewiesene -->
- intern müssen rohe Daten und verarbeitete Daten weitergereicht werden

fremde Module:
- CFG-Modul:
     - Interface mit ZoomTutorial, ZoomCalculator und ZoomBild
- Speicher-Modul:
     - Interface mit Zoom-Calculator

## Finden von Abstrakten Klassen
<!-- Konkrete Klassen: Instanziierung und Vererbung
     Abstrakte Klassen: Nur Vererbung! -->
<!-- Unterklassen sollten alle geerbten Verantwortlichkeiten unterstützen, eher noch mehr -->
<!-- Gemeinsame Verantwortlichkeiten sollten so weit hoch wie möglich geschoben werden -->
<!-- Abstrakte Klassen erben nie von Konkreten Klassen! -->
<!-- Klassen die keine neue Funktionalität hinzufügen sollten eliminiert werden! -->
<!-- Letzte Folien der Vorlesung sind hilfreich hierfür! -->
- Mehrere Klassen haben Interface mit CFG-Modul, lohnt es sich eine abstrakte Oberklasse dafür einzurichten?
     - nein, da die Klassen sehr unterschiedliche Werte abfragen.
- Abstrakte Oberklasse "Bild", von der ZoomBild erbt und welche auch in anderen Modulen genutzt werden kann
- Abstrakte Oberklasse "Tutorial", von der ZoomTutorial erbt
     - hier würde sich ein Interface mit CFG-Modul schon eher lohnen, da die Abfragen ungefähr gleich sind  
       (soll das Zoom-/CodeCharts-/Eyetracking-Tutorial angezeigt werden?)
