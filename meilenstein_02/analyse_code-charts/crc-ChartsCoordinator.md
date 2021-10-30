CRC-Karte - ChartsCoordinator

# ChartsCoordinator
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. berechnet bei relativer Größe des Rasters, wenn nötig, die neue Rastergröße aus vorherigen Durchläufen
2. stellt eine Anfrage an die Config-File zum Ändern des Rasters
3. gibt die Befehle für Bild, Raster und Eingabefenster zum Wechsel

## Kollaborationen
<!-- Kann die Klasse die Verantwortlichkeiten selbstädnig erfüllen? Was benötigt sie von welcher Klasse? -->
<!-- Was weiß die Klasse? Welche anderen Klassen benötigen die Informationen? -->
1. Bild
2. Raster
3. Eingabefenster
4. Config-File
5. Interner Speicher

---
#### Notizen:
<!-- Hier Notizen zum Denkprozess, Hintergrundgedanken, Klarstellungen hinzufügen  -->
- bekommt vorweg eingestellten Wechselzeiten für Bild zu Raster zu Eingabefenster von Config-File
- ruft Klasse Bild auf das Bild zu zeigen
- wechselt nach Ablauf der Zeit zum Raster über den Aufruf der Klasse Raster
- wechselt nach Ablauf der Zeit zum Eingabefenster über den Aufruf der Klasse Eingabefenster
- bekommt die Daten der Vorherigen Durchläufe von Interner Speicher zur Berechnung der Rastergröße, bei relativer Größe-Modus
- sendet eine Änderung des Rasters, bei relativer Rastergröße, an die Config-File


#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
