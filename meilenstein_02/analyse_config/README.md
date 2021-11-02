# Initial Exploration Config
<!-- Hier alles aufschreiben, was interessant erscheint! -->

## Was sind die Ziele des Systems?
<!-- Snow Cards können bei diesem Schritt helfen! -->
- Speicherung und Abrufen von Einstellungen
- Anpassung der Einstellungen über GUI (mit Dokumentation)
- Einspielen eines Config Files per GUI

## Was ist der erwartete Input?
- Config File (entweder schon im working directory / per GUI hochgeladen)
- Benutzerinput per GUI

## Was ist der erwartete Output?
- Informationen über einzelne Einstellungen auf Abruf durch andere Module

## Was sind Nomen Phrasen?
<!-- Alle relevanten Sachen aufschreiben, später kann aussortiert werden! -->
- Tools
- Einstelungsmöglichkeiten
- Config-Datei
- Format
## Liste der Klassen:
<!-- Erstmal alle aufschreiben, dann auswählen! (Kriterien siehe Vorgehensweise) -->
<!-- Warum sind die Klassen existent? Wenn das zu beantworten ist - u good! -->
<!-- ausgewählte Klassen mit Link, andere einklammern und CRC-Karte löschen -->
<!-- - [Klassenname](crc-{klassenname}.md)
- (nichtAusgewählteKlasse) -->

- [ConfigLoader](crc-ConfigLoader.md)
- [ConfigWriter](crc-ConfigWriter.md)
- [ConfigGUI](crc-ConfigGUI.md)
- [ConfigClient](crc-ConfigClient.md)

---
# Analyse - Config
<!-- Hier Notizen zum Denkprozess! -->
Das Config-Modul stellt nach außen hin 2 Funktionen zur Verfügung: Das Setten und Getten von Einstellungen. Intern wird dies über einen Writer und Loader geregelt, die die Kommunikation mit dem Config File regeln.  
Außerdem werden die Einstellungen intern gespeichert, um nicht bei jedem Aufruf das Config File neu zu parsen.
Die ConfigGUI wird in 2 Fällen benutzt und kommuniziert  mit dem ConfigClient:
- standalone Client zur Konfiguration
- integrierte GUI zum Verändern der Konfiguration

## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
- ConfigClient:
     - stellt zentrale Schnittstelle zu anderen Modulen und GUI dar
     - koordiniert Arbeit von Loader und Writer
- ConfigLoader:
     - Laden aus Config File in interne Struktur
- ConfigWriter:
     - Speichern aus interner Struktur in Config File
- ConfigGUI:
     - Visualisierung, Interface zum Anpassen, Anzeige der Dokumenation


## Kollaborationen
<!-- Benutzeranfragen an Dienste, die benötigt werden um Veranwortlichkeiten zu erfüllen -->
<!-- enthüllen Kontroll- und Informationsflüsse, und somit Subsysteme -->
<!-- Können fehlende Verantwortlichkeiten offenbaren, bzw. fehlerhaft zugewiesene -->
- ConfigClient zentrale Verbindungsstelle, alle anderen Klassen kommunizieren nur mit ConfigClient
- ConfigClient kommuniziert mit anderen Modulen
## Finden von Abstrakten Klassen
<!-- Konkrete Klassen: Instanziierung und Vererbung
     Abstrakte Klassen: Nur Vererbung! -->
<!-- Unterklassen sollten alle geerbten Verantwortlichkeiten unterstützen, eher noch mehr -->
<!-- Gemeinsame Verantwortlichkeiten sollten so weit hoch wie möglich geschoben werden -->
<!-- Abstrakte Klassen erben nie von Konkreten Klassen! -->
<!-- Klassen die keine neue Funktionalität hinzufügen sollten eliminiert werden! -->
<!-- Letzte Folien der Vorlesung sind hilfreich hierfür! -->
- keine Abstrahierung gefunden

---

## Notizen
- In der Zukunft wird eine Kollaboration mit dem Speichermedium nötig sein, damit der AnalyseClient die Konfiguration aus dem Speichermedium ablesen kann / wengistens eine ID. Das ist aber noch sehr unklar, da dies sehr von der Entscheidung Datei / Datenbank abhängt.
- Sollte man sowohl die Konfiguration als auch das Speichermedium als Datenbank realisieren, wäre es einfach, im Speichermedium eine ID der Konfiguration abzuspeichern, und so eine Verbindung herzustellen
