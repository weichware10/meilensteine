CRC-Karte - Diagramm
<table>
<tbody>
  <tr>
    <td>
        <a href='crc-client.md'>
            ← Client
        </a>
    </td>
    <td>
        <a href='README.md'>
            Analyse
        </a>
    </td>
    <td>
        <a href='crc-export.md'>
            Export →
        </a>
    </td>
  </tr>
</tbody>
</table>

# Diagramm
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. Berechnung Zeitdauer der Blicke
2. Erstellen der Diagramme

## Kollaborationen
<!-- Kann die Klasse die Verantwortlichkeiten selbstädnig erfüllen? Was benötigt sie von welcher Klasse? -->
<!-- Was weiß die Klasse? Welche anderen Klassen benötigen die Informationen? -->
1. Analyse (Oberklasse)
2. Client

---
#### Notizen:
<!-- Hier Notizen zum Denkprozess, Hintergrundgedanken, Klarstellungen hinzufügen  -->
- Tabelle: zu welcher Zeit welche Bildkoordinate (in Oberklasse ausgelagert)
- Häufigkeiten zu jeder Bildkoordinate berechnen (in Oberklasse ausgelagert)
	- Einteilung Bild in Bereiche: Häufigkeit wie oft Bereiche angeschaut wurden
- Berechnung wie lange auf eine Bildkoordinate geschaut wurde bei einem Blick
	- Kategorisierung der Blicklängen (<0.5s, <1s, etc.) + dazugehörige Häufigkeiten

#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
