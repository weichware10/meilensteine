# Bericht zum Meilenstein 6

## Was ist seit dem letzten Meilenstein passiert ?
- Freitag 26.11.2021 Teammeeting
    - Festlegung der Programmiersprache auf Java
        - OOP
        - Verwendbare GUI über Swing 
    - Installieren und Einarbeiten in Java 
    - Installieren und Konfigurieren von Maven als Buildingtool
    - Als Testsystem wird JUnit eingesetzt
    - Einführen von Checkstyle als Linter

- Vier neue Repositories:
    - Aufteilen von Toolbox und Analyse in 2 separate Programme, daher auch 2 verschiedene Repositories
        - "analyse"
        - "toolbox"
    - "util"
        - Util benötigt ein eigenes Repository, da dieses Code für beide Programme (Toolbox und Analyse) bereitstellt.
    - "repo-utils"
        - Beinhaltet die aktuellsten Workflows und Checkstyles
        - Dokumentation von Workflow und Checkstyle wird in "repo-utils" festgehalten

- Hauptarbeit war das Ausarbeiten der Klassen und deren Tests für die zukünftige Implementation

## Was waren die Herausforderungen und Probleme ? Wie wurden sie gelöst ?
- Wegen aktueller Coronalage sind persönliche Treffen nicht mehr möglich
    - Nutzung von BigBlueButton
- Sehr aufwändiger Meilenstein, da bei allen das Setup der genannten Tools eingerichtet und konfiguriert werden musste
    - Lösung: Virtuelles Teammeeting mit Bildschirmübertragung, gegenseitige Hilfe
- Nicht alle Teammitglieder hatten Erfahrung mit Java
    - Lösung: YouTube-Tutorials, gegenseitige Hilfe

## Was lief gut ? Was lief nicht gut ?
| gut                                                 | nicht gut      |
| --------------------------------------------------- | -------------- |
| Gute Teamarbeit                                     | Späterer Start |
| Einheitlicher Code durch die Nutzung von Checkstyle |                |

## Was haben Sie gelernt ?
- Nutzung der oben genannten Tools
- Implementierung von Tests
- Java (für einige Gruppenmitglieder)

## Was würden sie beim nächsten Mal anders machen ?
- Früher mit der Arbeit am nächsten Meilenstein beginnen

---
## Teilnehmer und Rollen.

- Verteilung der Aufgaben:
    | Aufgabe              | Team        | Review        |
    | -------------------- | ----------- | ------------- |
    | Tests Analyseclient  | Philip      | Joni, Sarah   |
    | Tests CodeCharts     | David       | Philip, Joni  |
    | Tests Config         | Josh        | David, Philip |
    | Tests EyeTracking    | Nils        | Josh, David   |
    | Tests Speichermedium | Justin      | Nils, Josh    |
    | Tests ZoomMaps       | Sarah       | Justin, Nils  |
    | Dokumentation        | Joni, Sarah | alle          |
    |                      |             |               |
