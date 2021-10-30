# Analyse - Datenanalyse Client
<!-- Hier Notizen zum Denkprozess! -->
Der Datenanalyse Client ruft die benötigten Daten vom Speicher-Modul ab und nach Auswahl der Analyseformen (Heatmap, Diagramme, zeitlicher Verlauf), erfolgt die Analyse der abgerufenen Daten und Erzeugung der Darstellungsformen. Die Ergebnisse der Analyse werden an den Client zur Anzeige übermittelt, indem die Möglichkeit zum besteht Export der Darstellungsformen als PDF besteht.

## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
- Client
     - Abfrage der Daten
     - Auswahl der Analyseformen
     - Anzeige der Darstellungen der Analyse
     - Auswahl Export
- Analyse
     - Berechnung der Häufigkeit pro Bildkoordinate (wie oft auf diese geschaut wurde)
     - Erstellen einer Tabelle (zu welcher Zeit welche Bildkoordinate beatractet wurde)
     - Funktionen zur Darstellung der Daten
- Heatmap
     - Erstellen der Heatmap
     - Überlagerung der Heatmap mit dem benutzen Bild
     - Vergleich zweier Heatmaps
- Diagramm
     - Ermittlung der Zeitdauer der Blicke
     - Erstellen der Diagramme
- Verlauf
     - Erstellen einer Übersicht über den zeitlichen Verlauf der Blicke
- Export
     - Erstellen einer PDF mit ausgewählten Darstellungen
     - Export dieser PDF

## Kollaborationen
<!-- Benutzeranfragen an Dienste, die benötigt werden um Veranwortlichkeiten zu erfüllen -->
<!-- enthüllen Kontroll- und Informationsflüsse, und somit Subsysteme -->
<!-- Können fehlende Verantwortlichkeiten offenbaren, bzw. fehlerhaft zugewiesene -->
- Übertragung interner Daten zwischen den Klassen notwendig  
fremde Module:  
- Speicher-Modul:
	- Interface mit Client

## Finden von Abstrakten Klassen
<!-- Konkrete Klassen: Instanziierung und Vererbung
     Abstrakte Klassen: Nur Vererbung! -->
<!-- Unterklassen sollten alle geerbten Verantwortlichkeiten unterstützen, eher noch mehr -->
<!-- Gemeinsame Verantwortlichkeiten sollten so weit hoch wie möglich geschoben werden -->
<!-- Abstrakte Klassen erben nie von Konkreten Klassen! -->
<!-- Klassen die keine neue Funktionalität hinzufügen sollten eliminiert werden! -->
<!-- Letzte Folien der Vorlesung sind hilfreich hierfür! -->
- Abstrakte Oberklasse "Analyse", von der Heatmap, Diagramm und Verlauf erbt
	- benötigen alle Grundfunktionen zur Darstellung
