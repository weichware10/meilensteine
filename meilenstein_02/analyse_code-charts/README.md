# Initial Exploration Code Charts
<!-- Eyetracking von Wish! -->

<!-- Hier alles aufschreiben, was interessant erscheint! -->

## Was sind die Ziele des Systems?
<!-- Snow Cards können bei diesem Schritt helfen! -->
- Bild, String & Location des Strings müssen erfasst & gemeinsam an den Datenanalyse Client gegeben werden 

## Was ist der erwartete Input?
Input vom System:
- Zeiteinstellung zwischen Bild und String-Raster
- Zeiteinstellung zwischen String-Raster und Eingabefenster
- Umstellen zwischen fester und relativer Größe
- Bild
- Sammlung von Strings
- wenn relative Größe eingestellt, muss nach vorherigen Imputs geschaut werden
  (oder Abrufen an welcher Stelle das Raster wie klein sein muss)
- Tutorial
Input vom Benutzer:
- String in das Eingabefenster
- Eingabe in das Tutorialfenster (don't show again / schließen)
## Was ist der erwartete Output?
- welches Bild
- welcher String 
- Location des Strings


## Was sind Nomen Phrasen?
<!-- Alle relevanten Sachen aufschreiben, später kann aussortiert werden! -->
- (Code Charts Tool)
- Bild
- (Zeit)
- Matrix -> Raster
- Eingabemöglichkeit
- (Punkt)
- (String)
- Eingabefenster
- (Zeiten des Wechselns)
- (zweidimensionales Raster von Strings)
- (Einstellung)
- (Größe der Raster)
- (feste oder relative Größe)
- (vorhandene Daten)
- (Eingaben dieselbe Stelle)


## Liste der Klassen:
<!-- Erstmal alle aufschreiben, dann auswählen! (Kriterien siehe Vorgehensweise) -->
<!-- Warum sind die Klassen existent? Wenn das zu beantworten ist - u good! -->
<!-- ausgewählte Klassen mit Link, andere einklammern und CRC-Karte löschen -->
- [ChartsCoodinator](crc-ChartsCoordinator.md)
- [ChartsBild](crc-ChartsBild.md)
- [ChartsRaster](crc-ChartsRaster.md)
- [ChartsEingabefenster](crc-ChartsEingabefenster.md)
- [ChartsInternerSpeicher](crc-ChartsInternerSpeicher.md)
- [ChartsTutorial](crc-ChartsTutorial.md)

----

# Analyse - CodeCharts
<!-- Hier Notizen zum Denkprozess! -->
Das Interner Speicher Modul erfasst die Daten der Klassen Bild, Eingabefenster und Raster, bearbeitet sie und gibt die weiter an die Klassen Coordinator und das Speichermedium. Die Config File bestimmt sämtliche Einstellungen und gibt sie an die entsprechenden Klassen weiter. Die Klassen Bild, Raster und Eingabefenster sind für die Anzeige und Eingabe verantwortlich. Die Coordinator Klasse steuert die Klassen Bild, Raster und Eingabefenster und berechnet die Rastergröße.

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
     - zeigt das Raster mit Strings
- ChartsEingabefenster:
     - zeigt das Eingabefenster
     - nimmt den Nutzerinput entgegen
- ChartsInternerSpeicher:
     - fasst die Daten geordnet zusammen
     - (verpackt die Daten in eine Datei)
- ChartsTutorial:    
     - zeigt das Tutorial (auch mehrfach möglich)
     - sendet eventuellen Nutzerinput an Config-File

## Kollaborationen
<!-- Benutzeranfragen an Dienste, die benötigt werden um Veranwortlichkeiten zu erfüllen -->
<!-- enthüllen Kontroll- und Informationsflüsse, und somit Subsysteme -->
<!-- Können fehlende Verantwortlichkeiten offenbaren, bzw. fehlerhaft zugewiesene -->
- Daten werden intern weitergereicht

Fremde Module:
- Config-File:
     - interface mit den Klassen Tutorial, Bild, Coordinator und InternerSpeicher
- Speichermedium:
     - interface mit der Klasse InternerSpeicher

## Finden von Abstrakten Klassen
<!-- Konkrete Klassen: Instanziierung und Vererbung
     Abstrakte Klassen: Nur Vererbung! -->
<!-- Unterklassen sollten alle geerbten Verantwortlichkeiten unterstützen, eher noch mehr -->
<!-- Gemeinsame Verantwortlichkeiten sollten so weit hoch wie möglich geschoben werden -->
<!-- Abstrakte Klassen erben nie von Konkreten Klassen! -->
<!-- Klassen die keine neue Funktionalität hinzufügen sollten eliminiert werden! -->
<!-- Letzte Folien der Vorlesung sind hilfreich hierfür! -->
- abstakte Oberklasse "Bild", von der die Klasse ChartsBild erbt und welche auch in anderen Modulen verwendet werden kann
- abstakte Oberklasse "Tutorial", von der die Kalsse ChartsTurtorial ebrt und welche auch in anderen Modulen verwendet werden kann
- eine abstrakte Oberklasse für das Config-FIle Modul lohnt sich nicht, da die Klassen des CodeCharts Moduls sehr unterschiedliche Werte abfragen
