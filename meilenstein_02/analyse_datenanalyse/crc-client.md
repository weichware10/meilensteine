CRC-Karte - Client
<table>
<tbody>
  <tr>
    <td>
        <a href='crc-analyse.md'>
            ← Analyse
        </a>
    </td>
    <td>
        <a href='README.md'>
            Analyse
        </a>
    </td>
    <td>
        <a href='crc-diagramm.md'>
            Diagramm →
        </a>
    </td>
  </tr>
</tbody>
</table>

# Client
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. Abfrage der Daten (Was für Daten?, Zeitraum?, etc.)  
2. Auswahl der Analyseformen
3. Übergabe der Daten an Analyse
4. Anzeige der Darstellungen der Analyse
5. Auswahl Export

## Kollaborationen
<!-- Kann die Klasse die Verantwortlichkeiten selbstädnig erfüllen? Was benötigt sie von welcher Klasse? -->
<!-- Was weiß die Klasse? Welche anderen Klassen benötigen die Informationen? -->
1. Speicher-Modul
2. Analyse
3. Export

---
#### Notizen:
<!-- Hier Notizen zum Denkprozess, Hintergrundgedanken, Klarstellungen hinzufügen  -->
- Client besitzt zentrale Verantwortlichkeiten
- Speicher-Modul stellt Daten bereit und Client fragt/holt benötigte Daten ab
- Übermittelt Daten an Analyse
- Empfängt analysierten Daten von Analyse
	- Ausgabe im Client
	- Export


#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
