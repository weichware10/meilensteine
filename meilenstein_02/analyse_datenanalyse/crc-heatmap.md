CRC-Karte - Heatmap
<table>
<tbody>
  <tr>
    <td>
        <a href='crc-export.md'>
            ← Export
        </a>
    </td>
    <td>
        <a href='README.md'>
            Analyse
        </a>
    </td>
    <td>
        <a href='crc-verlauf.md'>
            Verlauf →
        </a>
    </td>
  </tr>
</tbody>
</table>

# Heatmap
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. Erstellen der Heatmap
2. Überlagerung der Heatmap mit dem benutzten Bild
3. Vergleich zweier Heatmaps

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
- Heatmap auf Grundlage dieser Häufigkeiten erstellen
- Erstellte Heatmap kann über Bild gelegt werden
- Es werden für zwei Datensätze jeweils eine Heatmap erstellt und diese miteinander verglichen bsp. durch Überlagerung

#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
