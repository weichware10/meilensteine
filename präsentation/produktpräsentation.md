# Produktpräsentation

| Erfüllt                           | Offen       | Zusätzlich              |
| --------------------------------- | ----------- | ----------------------- |
| Zoommaps                          | Eyetracking | GUI für Konfiguration   |
| Codecharts                        |             | Anpassung Analyse-Arten |
| Konfiguration                     |             | diverse Admin/Dev-Tools |
| Datenbank (Konfiguration + Daten) |             |                         |
| JSON (Konfiguration + Daten)      |             |                         |
| Analysefunktionen                 |             |                         |

## Vorstellen der Apps
1. Laden einer vorbeiteten JSON-Konfiguration
2. Speichern in der Datenbank
3. Erstellen von 5 Trials
4. Nutzen einer Trial-ID in Toolbox
5. Analysieren der Ergebnisse in Analyse

---

## Vergleich zwischen Produkt und Spezifikation
---
### Zoom Maps
- [X] beliebiges Bild laden
- [X] an Bild heranzoomen
  - nicht beliebig nah
- [X] Zoomgeschwindigkeit anpassbar
- Zoom
  - [X] Maustasten
  - [x] Mausrad
---

### Code Charts
- [X] beliebiges Bild laden
- [X] Wechsel Bild -> Matrix -> Eingabemöglichkeit
- [X] Wechselzeiten einstellbar
- Zusätzlich
  - String-Vorschlag bei nichtvorhanden String
- Anordnung Strings im Raster
  - [X] randomisert
  - [x] geordnet
    - Sortierte Anordnung bezieht sich auf Reihenfolge der Einfügung der Strings
- [X] einstellbare Rastergröße
---

### Eye Tracking
- nicht gemacht
---

### Konfiguration
- [X] Einstellmöglichkeiten über Erstellen einer Konfiguration
- [ ] Konfigurationsdatei für alle Tools gleich
  - Ansichtssache: Dateiformat ist gleich, Struktur auch
  - spezifische Teile müssen ausgetauscht / geändert werden
  - Konfiguration ist Tool-spezifisch
- zusätzlich: Erstellen von Config und Trials über GUI
---

### Datenspeicherung
- [X] Datenbank
- [X] Datei (.json)
---

### Analyse
- [X] Daten aus Speichermedium lesen
- [X] benutzte Bild laden
- [X] zeitlicher Verlauf
  - Liniendiagramm
  - [X] Vergleich zweier Datensätze
- [X] Heatmap
- [X] relative Verteilung
  - Balkendiagramm
  - Kreisdiagramm
- Zusätzlich
  - Anpassung der Analysearten
---
