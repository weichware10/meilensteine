CRC-Karte - ConfigClient
<table>
<tbody>
  <tr>
    <td>
        <a href='crc-ConfigWriter.md'>
            ← ConfigWriter
        </a>
    </td>
    <td>
        <a href='README.md'>
            Analyse
        </a>
    </td>
    <td>
        <a href='crc-ConfigGUI.md'>
            ConfigGUI →
        </a>
    </td>
  </tr>
</tbody>
</table>

# ConfigClient
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. Setzen von Konfigurationswerte intern und im Config File
2. Zurückgeben von einzelnen / allen Konfigurationswerten
3. eventuelles losgelöstes Auslösen des Speichervorganges (siehe ConfigWriter)
4. Lagern der internen Konfigurationsstruktur

## Kollaborationen
<!-- Kann die Klasse die Verantwortlichkeiten selbständig erfüllen? Was benötigt sie von welcher Klasse? -->
<!-- Was weiß die Klasse? Welche anderen Klassen benötigen die Informationen? -->
1. ConfigLoader
2. ConfigWriter
3. ggf. ConfigGUI
4. externe Module (Zoom Maps, Code Charts, Eye Tracking)
5. AnalyseClient zum nachträglichen Anschauen der Konfiguration

---
#### Notizen:
<!-- Hier Notizen zum Denkprozess, Hintergrundgedanken, Klarstellungen hinzufügen  -->
- Schnittstelle für andere Module
- Koordiniert und lagert interne Konfigurationsdarstellung

#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
