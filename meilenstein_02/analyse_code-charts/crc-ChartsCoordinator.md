CRC-Karte - ChartsCoordinator
<table>
<tbody>
  <tr>
    <td>
        <a href='crc-ChartsTutorial.md'>
            ← ChartsTutorial
        </a>
    </td>
    <td>
        <a href='README.md'>
            Analyse
        </a>
    </td>
    <td>
        <a href='crc-ChartsBild.md'>
            ChartsBild →
        </a>
    </td>
  </tr>
</tbody>
</table>



# ChartsCoordinator
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. Ruft andere Klassen auf (koordiniert) 
2. berechnet bei relativer Größe des Rasters, wenn nötig, die neue Rastergröße aus vorherigen Durchläufen
3. stellt eine Anfrage an die Config-File zum zur Initialisierung des Rasters + für Strings zum einlesen

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
- Bild: ruft Klasse Bild auf das Bild zu zeigen
- Raster: ruft Klasse Raster auf +  berechnet neue Rasterdimension + gibt Strings zum Einlesen weiter
- Eingabefenster: ruft Klasse eingabefenster auf + nimmt eingegebenen String zurück
- Config-File: Fragt Strings an + bekommt Strings, Wechselzeiten, Rasterdimension zum Initialisieren
- Interner Speicher: Gibt String, Stringkoordinaten, Rasterdimension, eventuell Zeit weiter, bekommt Infos über bisherige Durchläufe und Klicks (zum Berechnen neuer Rasterdimensionen bei relativer Größe)
- Generell: ruft die Klassen Bild -> Raster -> Eingabefenster automatisch nach einer zuvor festgelegten Zeit auf


#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
