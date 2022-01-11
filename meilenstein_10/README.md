# Bericht zum Meilenstein 10

## Was ist seit dem letzten Meilenstein passiert ?
- Hauptsächlich:
    - Code Charts
        - Überarbeitung von Code Charts Configuration
        - GUI
        - Funktionen
    - AnalyseClient 
        - allgemeine GUI
        - Eigentlich war hier für diesen Meilenstein wirklich nur die GUI geplant,
        es ist dann aber doch viel mehr fertig geworden (einen Teil der Funktionen)
        - Anbindung an Datenbank
            - Datenbankverbindung
            - Datenbankabfrage
        - analyse konfiguration
        - Dieser PR ist allerdings noch nicht gemerged, Fertigstellung dann in Meilenstein 11
    - viele Fehlerbehebung 
        - das Log Fenster hat sich nicht mit dem Hauptfenster geschlossen
        - uneinheitliche Sprache (Englisch <> Deutsch)
        - Bilder wurden nicht angezeigt
        - Sonderzeichen haben Probleme mit SQL verursacht

## Was waren die Herausforderungen und Probleme ? Wie wurden sie gelöst ?
- Bei dem Versuche ein Raster für CodeCharts aufzubauen war GridPlane nicht dynamisch genug
    - Lösung: Erweiterung der AnchorPane Klasse, Anordnung mittels HBoxen und VBoxen (Klasse CodeChartsPane ist dafür zuständig)

## Was lief gut ? Was lief nicht gut ?
| gut  | nicht gut  |
| ---- | ---- |
| Erstellung der GUI ist einfach und schnell (FXML zahlt sich aus) | / |

## Was haben Sie gelernt ?
- Umgang mit dynamischen graphischen Elementen

## Was würden sie beim nächsten Mal anders machen ?
- /

---
## Teilnehmer und Rollen .

- Verteilung der Aufgaben:
    | Aufgabe             | Team                   | Review    | Pull-Requests                     |
    | ------------------- | ---------------------- | --------------- | ---------------------------------------------- |
    | Code Charts (toolbox) | Joshua, Justin, David  | Jonathan, David | [PR](https://github.com/weichware10/toolbox/pull/23) |
    | Code Charts (util) | Joshua | Justin, David | [PR](https://github.com/weichware10/util/pull/35) |
    | Analyse Client (analyse) | Joshua, Justin, David | / | [PR](https://github.com/weichware10/analyse/pull/7) |
    | Analyse Client (util) | Joshua | David | [PR](https://github.com/weichware10/util/pull/33) |
    | handshake fix | Philip | Joshua, Jonathan | [Issue](https://github.com/weichware10/toolbox/issues/18), [PR](https://github.com/weichware10/toolbox/pull/20) |
    | zoomMapsBild -> zoomMapsImage | Jonathan | Joshua, David | [Issue](https://github.com/weichware10/toolbox/issues/24), [PR](https://github.com/weichware10/toolbox/pull/25) |
    | Probleme mit Sonderzeichen | Philip | Joshua | [Issue](https://github.com/weichware10/util/issues/31), [PR](https://github.com/weichware10/util/pull/32) |
    | Log schließt sich nicht | Josh | Philip, Jonathan | [Issue](https://github.com/weichware10/toolbox/issues/19), [PR](https://github.com/weichware10/toolbox/pull/21) |
    | Datenbank Änderungen | Josh | Nils, Sarah | [PR](https://github.com/weichware10/util/pull/34) |
    | Dokumentation | Sarah, Jonathan | alle | [PR](https://github.com/weichware10/meilensteine/pull/68) |
