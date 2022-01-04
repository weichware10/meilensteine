# Bericht zum Meilenstein 8

## Was ist seit dem letzten Meilenstein passiert ?
- Zoommaps Gui
- Zoommaps Funktionallität
- Umstellung der GUI auf fxml + Scenebuilder
- Logfenster
- Einfügen von Installern
- Rechteverwaltung in der DB (Profile: Nutzer, Author, Admin, Beobachter)
- Abspeicherung neben DB auch als .json

## Was waren die Herausforderungen und Probleme ? Wie wurden sie gelöst ?
- Fehlen einer Abhängigkeit in der Installer Datei
    - Lösung: Mehrere Tage pure Verzweiflung?
- Umzüge, Hardwareversagen, andere Unpässlichkeiten
    - Lösung: ?

## Was lief gut ? Was lief nicht gut ?
| gut                        | nicht gut                                                                               |
| -------------------------- | --------------------------------------------------------------------------------------- |
| Umstellung auf fxml | / |

## Was haben Sie gelernt ?
- Umgang mit fxml und Scenebuilder
- Erstellen von Installerdateien
- Erstellen von Dialogen
- EventHandling
- grundlagen Parraleles Progammingen

## Was würden sie beim nächsten Mal anders machen ?
- Arbeiten "zwischen den Jahren" ist schwierig. Da hätten Termine, ect. besser abgesprochen werden müssen.
- 

---
## Teilnehmer und Rollen .

- Verteilung der Aufgaben:
    | Aufgabe    | Team                                                  | Review                                  | Pull-Requests |
    | ---------- | ----------------------------------------------------- | --------------------------------------- | --- |
    | GUI Toolbox | Joshua, Justin, David | Jonathan, Philip| [GUI Toolbox](https://github.com/weichware10/toolbox/pull/10) |
    | SpeicherUtilities | Sarah | Philip, Joshua | [SpeicherUtilities](https://github.com/weichware10/util/pull/25) |
    | Einbindung von json | Philip, Justin | Joshua, Jonathan | [Json](https://github.com/weichware10/util/pull/23) |
    | FXML | Philip, Justin, Joshua | David, Jonathan | [FXML](https://github.com/weichware10/toolbox/pull/14) |
    | Permissions | Joshua | Philip, David | [Permissions](https://github.com/weichware10/util/pull/26) |
    | ZoomMaps(Util) | Justin, Philip, Joshua | Jonathan | [ZoomMaps](https://github.com/weichware10/util/pull/28) |
    | Logger | Joshua | Justin, Jonathan | [Logger](https://github.com/weichware10/util/pull/30) [Logger GUI](https://github.com/weichware10/toolbox/pull/16) |
    | Dokumentation | Jonathan | alle | [Dokumentation](https://github.com/weichware10/meilensteine/pull/67)