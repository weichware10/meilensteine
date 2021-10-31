CRC-Karte - ConfigWriter
<table>
<tbody>
  <tr>
    <td>
        <a href='crc-ConfigLoader.md'>
            ← ConfigLoader
        </a>
    </td>
    <td>
        <a href='README.md'>
            Analyse
        </a>
    </td>
    <td>
        <a href='crc-ConfigClient.md'>
            ConfigClient →
        </a>
    </td>
  </tr>
</tbody>
</table>

# ConfigWriter
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. schreibt interne Struktur in Config File

## Kollaborationen
<!-- Kann die Klasse die Verantwortlichkeiten selbständig erfüllen? Was benötigt sie von welcher Klasse? -->
<!-- Was weiß die Klasse? Welche anderen Klassen benötigen die Informationen? -->
1. ConfigClient

---
#### Notizen:
<!-- Hier Notizen zum Denkprozess, Hintergrundgedanken, Klarstellungen hinzufügen  -->
- schreibt einzelne Werte oder gesamte Konfiguration? 2 Optionen:
    1. bei jeder Änderung einzelnen oder mehrere Werte schreiben (ständiger Speicheraufwand)
    2. erst bei Klicken auf "Speichern" oder beim Schließen der Anwendung alle Werte schreiben (Fehleranfällig?)
- bekommt Auftrag von ConfigClient

#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
