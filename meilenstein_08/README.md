# Bericht zum Meilenstein 8

## Was ist seit dem letzten Meilenstein passiert ?
- Anfang Toolbox GUI
- Datenbank Package ([Setup](https://weichware10.github.io/dokumente/setup.html) - vorläufig)

## Was waren die Herausforderungen und Probleme ? Wie wurden sie gelöst ?
- Datenbank Package größer als erwartet - dafür ersetzt es aber das Speichermedium Package
- Toolbox GUI größtenteils fertig, jedoch auf Meilenstein 8,5 (nächste Woche, interner Meilenstein) verschoben

## Was lief gut ? Was lief nicht gut ?
| gut                        | nicht gut                                                                               |
| -------------------------- | --------------------------------------------------------------------------------------- |
| Implementierung db-Package | Aufteilung der Aufgaben, da es schwierig ist an einzelnen Features zusammen zu arbeiten |

## Was haben Sie gelernt ?
- toString() von Float-Typ werden abhängig von Systemsprache formatiert (`3.0`/`3,0`)
    - dadurch sind Tests bei manchen fehlgeschlagen, bei Anderen nicht
- Datenbanken, Aufbau, Kommunikation mit Java, Abfragen, SQL, etc.
- Erstellen einer GUI mit JavaFX
- Arbeit mit .env Files
- Änderungen der Struktur bei Implementierung eines Features können sehr weitgreifend sein, da man noch nicht von Anfang an die richtige Struktur festgelegt hat (Lernen und Verbessern der Softwarestruktur)

## Was würden sie beim nächsten Mal anders machen ?
- Mehrere Pull-Requests anstelle von einem rießigen Pull-Requests mit einer Vielzahl von veränderten Dateien
    - Schwierig, wenn man bestimmte Sachen erst während der Arbeit innerhalb eines PRs feststellt

---
## Teilnehmer und Rollen .

- Verteilung der Aufgaben:
    | Aufgabe    | Team                                                  | Review                                  | Pull-Requests |
    | ---------- | ----------------------------------------------------- | --------------------------------------- | --- |
    | Toolbox    | Justin, Sarah, David                                  | Nächste Woche (interner Meilenstein 8,5) | [GUI ToolBox](https://github.com/weichware10/toolbox/pull/10) |
    | db-Package | Größtenteils Philip und Joshua, Zuarbeit durch Andere | Die restlichen Teammitglieder            | [DataBaseClient](https://github.com/weichware10/util/pull/20) |                   |
    | Dokumentation | Joshua, Sarah | Alle | [Dokumentation](https://github.com/weichware10/meilensteine/pull/66) |