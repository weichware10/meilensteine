CRC-Karte - ChartsRaster

# ChartsRaster
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. die gegebenen Strings in Raster anzeigen

## Kollaborationen
<!-- Kann die Klasse die Verantwortlichkeiten selbstädnig erfüllen? Was benötigt sie von welcher Klasse? -->
<!-- Was weiß die Klasse? Welche anderen Klassen benötigen die Informationen? -->
1. Config-File
2. Coordinator
3. Interner Speicher

---
#### Notizen:
<!-- Hier Notizen zum Denkprozess, Hintergrundgedanken, Klarstellungen hinzufügen  -->
- bekommt die anzuzeigenden Strings und den Aufbau des Rasters von der Config-File
- bekommt von Coordinator den Aufruf das Raster mit den Strings anzuzeigen
- sendet die Koordinate des Strings an Interner Speicher

#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
