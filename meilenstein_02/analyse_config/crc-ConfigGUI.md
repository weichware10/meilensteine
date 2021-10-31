CRC-Karte - ConfigGUI
<table>
<tbody>
  <tr>
    <td>
        <a href='crc-ConfigClient.md'>
            ← ConfigClient
        </a>
    </td>
    <td>
        <a href='README.md'>
            Analyse
        </a>
    </td>
    <td>
        <a href='crc-ConfigLoader.md'>
            ConfigLoader →
        </a>
    </td>
  </tr>
</tbody>
</table>

# ConfigGUI

## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. Anzeigen der aktuellen Konfiguration
2. Verändern der Konfigurationswerte
3. Dokumentation der Konfiguration 

## Kollaborationen
<!-- Kann die Klasse die Verantwortlichkeiten selbständig erfüllen? Was benötigt sie von welcher Klasse? -->
<!-- Was weiß die Klasse? Welche anderen Klassen benötigen die Informationen? -->
1. ConfigClient

---
#### Notizen:
<!-- Hier Notizen zum Denkprozess, Hintergrundgedanken, Klarstellungen hinzufügen  -->
- AnalyseClient sollte keine eigene ConfigGUI Klasse besitzen, sondern Daten von ConfigClient bekommen und dann selbst anzeigen
    - Begründung: da dies ein sehr unterschiedlicher Anwendungszweck ist (keine Änderung der Einstellung, nur Anzeigen, keine Dokumentation)

#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
