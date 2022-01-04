# Bericht zum Meilenstein 9

## Was ist seit dem letzten Meilenstein passiert ?
- Zoommaps GUI
- Zoommaps Funktionalitäten
- Umstellung der GUI auf FXML + Scenebuilder
- Logger + Logfenster
    - Loggen in Datei, Konsole und GUI Fenster
- Einfügen von Installern
- Rechteverwaltung in der DB 
    - Profile: Nutzer, Author, Admin, Beobachter)
    - ([UML](https://github.com/weichware10/dokumente/blob/db-users/uml-usecase/db/users.png))
- Abspeicherung neben DB auch als .json

## Was waren die Herausforderungen und Probleme ? Wie wurden sie gelöst ?
- Fehlen einer Abhängigkeit in der Installer Datei
    - Lösung: Hinzufügung fehlender Abhängigkeit in pom.xml (bei Erstellung des custom JVM image)
gefehlt haben: java.sql, java.management,java.security.sasl
- Umzüge, Hardwareversagen, andere Unpässlichkeiten
    - Schwierig zu Lösen, Updates duch Teammitglieder mit mehr Zeit.(Gegenseitiges auf dem Laufenden halten)

## Was lief gut ? Was lief nicht gut ?
| gut                        | nicht gut                                                                               |
| -------------------------- | --------------------------------------------------------------------------------------- |
| Umstellung auf FXML (langfristige Zeiterspaarniss) | Spätes Erkennen von Bugs |
| | Probleme mit 4K-Bildschirmen, muss noch gelöst werden |

## Was haben Sie gelernt ?
- Umgang mit FXML und Scenebuilder
- Erstellen von Installerdateien
- Umsetzen von Features mit JavaFX
    - Erstellen von Dialogen
    - EventHandling
    - Trennung von JavaFX-Thread und Logik-Thread 
        - siehe Abspeicherung von Test in Datenbank ([saveTestToJson() & saveTestToDataBase()](https://github.com/weichware10/toolbox/commit/848095466e8d529ff3f486a5b025b4c836f001e5#diff-c23dcfb84036703235b0fc7be1c16ccbc73a3104d74181b0f13b3d742f1fe610R66-R107]))

## Was würden sie beim nächsten Mal anders machen ?
- Arbeiten "zwischen den Jahren" ist schwierig. Da hätten Termine, ect. besser abgesprochen werden müssen.
    - Einplanen von Feiertagen / genauere Absprache über Verfügbarkeit

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
    | Logger | Joshua, Nils | Justin, Jonathan | [Logger](https://github.com/weichware10/util/pull/30) [Logger GUI](https://github.com/weichware10/toolbox/pull/16) |
    | Dokumentation | Jonathan, Nils | alle | [Dokumentation](https://github.com/weichware10/meilensteine/pull/67) 
