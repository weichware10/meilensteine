CRC-Karte - Suchen
<table>
<tbody>
  <tr>
    <td>
        <a href='crc-Aendern.md'>
            ← Aendern
        </a>
    </td>
    <td>
        <a href='README.md'>
            Analyse
        </a>
    </td>
    <td>
        <a href='crc-Speichern.md'>
            Speichern →
        </a>
    </td>
  </tr>
</tbody>
</table>

# Suchen
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. Suchen nach Informationen in einer Datei oder mehreren Dateien
2. Angefragte Informationen bündeln und als ein "Paket" dem Dataclient übergeben
3. Besitzt für alle drei Funktionen die Daten liefern unterschiedliche Funktionen zum suchen der Daten

## Kollaborationen
<!-- Kann die Klasse die Verantwortlichkeiten selbstädnig erfüllen? Was benötigt sie von welcher Klasse? -->
<!-- Was weiß die Klasse? Welche anderen Klassen benötigen die Informationen? -->
1. Kollaboriert mit Klassen aus dem DataClient Modul

---
#### Notizen:
<!-- Hier Notizen zum Denkprozess, Hintergrundgedanken, Klarstellungen hinzufügen  -->
- Diese muss nur dem DataClient zur Verfügung gestellt werden
- DataClient kann speziell nach Informationen suchen
- Besitzt für alle 3 Funktionen spezielle Suchen, für die jeweiligen Daten
- Besitzt die Möglichkeit nach Dateinnamen als auch nach allen Daten von einer Funktion zu suchen
- Kann einzelne Daten (falls notwendig) als auch einen kompletten Datensatz ausgeben
#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
