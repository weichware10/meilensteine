# Bericht zum Meilenstein 11

## Was ist seit dem letzten Meilenstein passiert ?
- AnalyseClient
    - Fertigstellung der GUI
        - Überarbeitung des Designs
        - Konfigurator hinzugefügt
        - Trial-Ersteller hinzugefügt (TrialIDs aus KonfigID)
    - Analyse
        - Verlauf
        - Heatmap
        - CodeCharts Berechnung
- Tutorials
    - Zoommaps
    - CodeCharts

## Was waren die Herausforderungen und Probleme ? Wie wurden sie gelöst ?
- Berechnung der Zoom-Tiefe
    - Erster Berechnungsversuch lieferte keine ausgeglichene Heatmap-Verteilung
    - Lösung:
        - Normalisierungsrechnung: `10^(unnormalisierte Tiefe)`

## Was lief gut ? Was lief nicht gut ?
| gut                                              | nicht gut |
| ------------------------------------------------ | --------- |
| Arbeiten in kleinen Gruppen (Tutorials, Analyse) |           |

## Was haben Sie gelernt ?
- Bildbearbeitung in Java
- Diagramme in JavaFX

## Was würden sie beim nächsten Mal anders machen ?
- /

---
## Teilnehmer und Rollen .

- Verteilung der Aufgaben:
    | Aufgabe                                     | Team                   | Review                  | Pull-Requests                                             |
    | ------------------------------------------- | ---------------------- | ----------------------- | --------------------------------------------------------- |
    | Änderungen für AnalyseClient                | Joshua                 | Justin, David, Jonathan | [PR](https://github.com/weichware10/util/pull/33)         |
    | GUI Grundstruktur                          | Joshua, Justin, Philip | Jonathan                | [PR](https://github.com/weichware10/analyse/pull/7)       |
    | Heatmap + Verlauf                           | Joshua, Philip         | Jonathan, Justin        | [PR](https://github.com/weichware10/analyse/pull/8)       |
    | Permissions für strings-Tabelle hinzugefügt | Joshua                 | Justin, David           | [PR](https://github.com/weichware10/util/pull/36)         |
    | imgUrl for macOS                            | Justin                 | Joshua                  | [PR](https://github.com/weichware10/toolbox/pull/26)      |
    | strings in config + Verbesserungen          | Joshua                 | Justin, David           | [PR](https://github.com/weichware10/util/pull/38)         |
    | save generated images to temp               | Philip                 | Justin, Jonathan        | [PR](https://github.com/weichware10/util/pull/39)         |
    | util v3.2 + CodeCharts image URL            | Justin                 | Joshua, Philip, David   | [RP](https://github.com/weichware10/toolbox/pull/27)      |
    | Tutorials                                   | Nils, Sarah            | /                       | [PR](https://github.com/weichware10/dokumente/pull/18)    |
    | Dokumentation                               | Jonathan               | alle                    | [PR](https://github.com/weichware10/meilensteine/pull/69) |