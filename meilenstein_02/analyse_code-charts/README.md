# Analyse - CodeCharts
<!-- Hier Notizen zum Denkprozess! -->
Das Interner Speicher Modul erfasst die Daten der Klassen Eingabefenster und Raster, bearbeitet sie und gibt die weiter an die Klassen Coordinator und das Speichermedium. Die Config File bestimmt sämtliche Einstellungen und gibt sie an die entsprechenden Klassen weiter. Die Klassen Bild, Raster und Eingabefenster sind für die Anzeige und Eingabe verantwortlich. Die Coordinator Klasse steuert die Klassen Bild, Raster und Eingabefenster und berechnet die Rastergröße.

## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
- ChartsCoordinator:
     - steuert die Anzeige von Bild, Raster und Eingabefenster
     - berechnet die Rastergröße bei variabler Größe
- ChartsBild:
     - zeigt das Bild
- ChartsRaster:
     - zegt das Raster mit Strings
- ChartsEingabefenster:
     - zeigt das Eingabefenster
     - nimmt den Nutzerinput entgegen
- ChartsInterner Speicher:
     - fasst die Daten geordnet zusammen
     - verpackt die Dten in eine Datei
- ChartsTutorial:    
     - zeigt das Tutorial (auch mehrfach möglich)

## Kollaborationen
<!-- Benutzeranfragen an Dienste, die benötigt werden um Veranwortlichkeiten zu erfüllen -->
<!-- enthüllen Kontroll- und Informationsflüsse, und somit Subsysteme -->
<!-- Können fehlende Verantwortlichkeiten offenbaren, bzw. fehlerhaft zugewiesene -->
- Daten werden intern weitergereicht

frende Module:
- Config-File:
     - interface mit Bild, Raster, Tutorial und Coordinator Klasse
- Speichermedium:
     - interface mit Interner Speicher Klasse

## Finden von Abstrakten Klassen
<!-- Konkrete Klassen: Instanziierung und Vererbung
     Abstrakte Klassen: Nur Vererbung! -->
<!-- Unterklassen sollten alle geerbten Verantwortlichkeiten unterstützen, eher noch mehr -->
<!-- Gemeinsame Verantwortlichkeiten sollten so weit hoch wie möglich geschoben werden -->
<!-- Abstrakte Klassen erben nie von Konkreten Klassen! -->
<!-- Klassen die keine neue Funktionalität hinzufügen sollten eliminiert werden! -->
<!-- Letzte Folien der Vorlesung sind hilfreich hierfür! -->
- abstakte Oberklasse "Bild", von der die Klasse ChartsBild erbt und welche auch in anderen Modulen verwendet werden kann
-abstakte Oberklasse "Tutorial", von der die Kalsse ChartsTurtorial ebrt und welche auch in anderen Modulen verwendet werden kann
- eine abstrakte Oberklasse für das Config-FIle Modul lohnt sich nicht, da die Klassen des  CodeCharts Moduls sehr unterschiedliche Werte abfragen
