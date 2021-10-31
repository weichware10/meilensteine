CRC-Karte - Analyse
<table>
<tbody>
  <tr>
    <td>
        <a href='crc-verlauf.md'>
            ← Verlauf
        </a>
    </td>
    <td>
        <a href='README.md'>
            Analyse
        </a>
    </td>
    <td>
        <a href='crc-client.md'>
            Client →
        </a>
    </td>
  </tr>
</tbody>
</table>

# Analyse
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. Funktionen zur Analyse der Daten  
	- Berechnung der Häufigkeit pro Bildkoordinate (wie oft auf diese geschaut wurde)
	- Erstellen einer Tabelle: zu welcher Zeit welche Bildkoordinate betrachtet
2. Funktionen zur Darstellung der Daten  

## Kollaborationen
<!-- Kann die Klasse die Verantwortlichkeiten selbstädnig erfüllen? Was benötigt sie von welcher Klasse? -->
<!-- Was weiß die Klasse? Welche anderen Klassen benötigen die Informationen? -->
1. Client  
2. Heatmap
3. Diagramm
4. Verlauf
5. Export  

---
#### Notizen:
<!-- Hier Notizen zum Denkprozess, Hintergrundgedanken, Klarstellungen hinzufügen  -->
- Abstrakte Klasse
- Bekommt vom Client die benötigten Daten  
- Verantwortlich für gesamte Analyse  
	- Klasse Heatmap
	- Klasse Diagramm
	- Klasse Verlauf
- Ergebnisse an Client übermitteln  

#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
