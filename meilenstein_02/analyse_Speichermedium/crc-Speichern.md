CRC-Karte - Speichern
<table>
<tbody>
  <tr>
    <td>
        <a href='crc-Suchen.md'>
            ← Suchen
        </a>
    </td>
    <td>
        <a href='README.md'>
            Analyse
        </a>
    </td>
    <td>
        <a href='crc-Aendern.md'>
            Aendern →
        </a>
    </td>
  </tr>
</tbody>
</table>

# Speichern
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
1. Kann Dateien erstellen und Informationen in diesen abspeichern
2. Es wird pro Funktion eine eigene Datei angelegt mit einer vorher festgelegten Struktur
3. Speichert Standardmäßig das Datum + Funktion woher die Informationen kommen, ansonsten auch mit selbst eingegebenen Namen

## Kollaborationen
<!-- Kann die Klasse die Verantwortlichkeiten selbstädnig erfüllen? Was benötigt sie von welcher Klasse? -->
<!-- Was weiß die Klasse? Welche anderen Klassen benötigen die Informationen? -->
1. Steht im Kontakt mit den Modulen *Zoom Maps*, *Codecharts* und *Webcam basiertes Eyetracking*
2. Es muss in den Klassen der Funktionen möglich sein auf diese zuzugreifen um ihre Informationen abzuspeichern

---
#### Notizen:
<!-- Hier Notizen zum Denkprozess, Hintergrundgedanken, Klarstellungen hinzufügen  -->
- Diese Klasse steht den drei Funktionen zur Verfügung
- Es wird für jede Funktion eine eigene Datei erstellt in der die Informationen gespeichert werden, dadurch wird verhindert das es zu "Vermischungen" der Daten kommt
- durch das getrennte Speichern wird auch die Klasse *Suchen* leichter zu implementieren
- Stellt jeder Funktion eine einheitliche Speicherung der Infromationen in der Datei sicher
- muss in Absprache mit den Funktionen erstellt werden
- besitzt die Möglichkeit den Dateien Namen zu geben, ansonsten standard -> Datum der Erstellung
#### Changelog:
<!-- Hier eventuelle Abänderungen dokumentieren -->
