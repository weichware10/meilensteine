CRC-Karte - ZoomCalculator
<table>
<tbody>
  <tr>
    <td>
        <a href='crc-ZoomBild.md'>
            ← ZoomBild
        </a>
    </td>
    <td>
        <a href='README.md'>
            Analyse
        </a>
    </td>
    <td>
        <a href='crc-ZoomInput.md'>
            ZoomInput →
        </a>
    </td>
  </tr>
</tbody>
</table>

# ZoomCalculator
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. Input-Daten in neue Bildposition umrechnen
2. Geschwindigkeit umsetzen (Input abweisen, cooldown)

## Kollaborationen
<!-- Kann die Klasse die Verantwortlichkeiten selbstädnig erfüllen? Was benötigt sie von welcher Klasse? -->
<!-- Was weiß die Klasse? Welche anderen Klassen benötigen die Informationen? -->
1. Bild
2. ZoomInput
3. config-Modul
4. Speicher-Modul

---
#### Notizen:
<!-- Hier Notizen zum Denkprozess, Hintergrundgedanken, Klarstellungen hinzufügen  -->
- neue Bildposition wird an Bild und Speicher-Modul weitergegeben
- ZoomInput liefert Rohdaten
- config-Modul liefert Geschwindigkeitseinstellung

#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
