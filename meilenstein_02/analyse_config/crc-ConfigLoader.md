CRC-Karte - ConfigLoader
<table>
<tbody>
  <tr>
    <td>
        <a href='crc-ConfigGUI.md'>
            ← ConfigGUI
        </a>
    </td>
    <td>
        <a href='README.md'>
            Analyse
        </a>
    </td>
    <td>
        <a href='crc-ConfigWriter.md'>
            ConfigWriter →
        </a>
    </td>
  </tr>
</tbody>
</table>

# ConfigLoader
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. Liest gesamtes Config File in interne Struktur

## Kollaborationen
<!-- Kann die Klasse die Verantwortlichkeiten selbständig erfüllen? Was benötigt sie von welcher Klasse? -->
<!-- Was weiß die Klasse? Welche anderen Klassen benötigen die Informationen? -->
1. ConfigClient

---
#### Notizen:
<!-- Hier Notizen zum Denkprozess, Hintergrundgedanken, Klarstellungen hinzufügen  -->
- liest immer gesamte Konfiguration, für Rückgabe einzelner Werte ist Client zuständig
- bekommt Anfrage von ConfigClient (gegebenenfalls "Configuration-ID") und gibt interne Struktur zurück

#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
