CRC-Karte - ChartsInternerSpeicher
<table>
<tbody>
  <tr>
    <td>
        <a href='crc-ChartsEingabefenster.md'>
            ← ChartsEingabefenster
        </a>
    </td>
    <td>
        <a href='README.md'>
            Analyse
        </a>
    </td>
    <td>
        <a href='crc-ChartsTutorial.md'>
            ChartsTutorial →
        </a>
    </td>
  </tr>
</tbody>
</table>



# ChartsInternerSpeicher
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. bringt die gegebenen Informationen in einem einheitlichen und geordneten Format zusammen
2. (erstellt eine Datei)

## Kollaborationen
<!-- Kann die Klasse die Verantwortlichkeiten selbstädnig erfüllen? Was benötigt sie von welcher Klasse? -->
<!-- Was weiß die Klasse? Welche anderen Klassen benötigen die Informationen? -->
1. Config-File
2. Coordinator
3. Speichermedium

---
#### Notizen:
<!-- Hier Notizen zum Denkprozess, Hintergrundgedanken, Klarstellungen hinzufügen  -->
- Config-File: Config File schickt Bild an den I.S.
- Coordinator: C. schickt Stringkoordinaten, String, Rasterdimension an I.S. -> I.S. schickt Infos über bisherige Durchläufe zurück
- Speichermedium: Zum Ende eines Durchlaufs werden die gesammelten Daten an das Speichermedium weitergeleitet (eventuell in Form einer Datei) und aus dem I.S. gelöscht

#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
