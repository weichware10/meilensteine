# Initial Exploration Speichermedium

<!-- Hier alles aufschreiben, was interessant erscheint! -->
- In Welchen Größen werden die Daten von den Funktionen geliefert ?
- In Welchen Größen möchte der DataClient Informationen erhalten ?
- Wie sieht die Datenstruktur für die gespeicherten Daten aus ?
- Werden die Daten als Dateien oder in einer Datenbank gespeichert ?
- Was passiert bei einer Unterbechung zwischen Dataclient - Speichermedium und Funktion - Speichermedium ?
- Werden noch weitere Funktionen als die Basics benötigt ?
- Eventuell muss sich das Speichermedium noch um die Aufnahme der Configs für die Funktionen in den Dateien kümmern

## Was sind die Ziele des Systems?
<!-- Snow Cards können bei diesem Schritt helfen! -->
- Es sollen die Daten von den drei Funktionen (sowie ihre eingestellte Config-Daten) gespeichert werden, jede Funktion speichert jeweils in einer eigenen Datei
- Es ist möglich Dateien zu erstellen für verschiedene Datensätze der Funktionen von verschiedenen Versuchen
- Es wird dem Dataclient eine Klasse mit Funktionen zur Verfügung gestellt, welche ihm ermöglichen nach Informationen, Dateien, als auch ganzen Datenordnern zu suchen
- Das System ermöglicht es Datensätze auch wieder zu löschen

## Was ist der erwartete Input?
Es werden Datensätze von den Funktionen *Zoom Maps*, *Codecharts*, *Webcam basiertes Eyetracking* und DataClient erwartet. 

## Was ist der erwartete Output?
Es wird erwartet, dass der DataClient nach Dateien, Ordnern, als auch einzelnen Informatione fragt und diese ihm dann ausgegeben werden müssen.

## Was sind Nomen Phrasen?
<!-- Alle relevanten Sachen aufschreiben, später kann aussortiert werden! -->
- Speicher/Schreiben
- Lesen/Suchen
- Löschen/Aendern
- Sortieren

## Liste der Klassen:
<!-- Erstmal alle aufschreiben, dann auswählen! (Kriterien siehe Vorgehensweise) -->
<!-- Warum sind die Klassen existent? Wenn das zu beantworten ist - u good! -->
<!-- ausgewählte Klassen mit Link, andere einklammern und CRC-Karte löschen -->
- [Suchen](crc-{Suchen}.md)
- [Speichern](crc-{Speichern}.md)
- [Aendern](crc-{Aendern}.md)
- (Sortieren)

---

# Analyse - Speichermedium
<!-- Hier Notizen zum Denkprozess! -->
Das Modul/Der Client "Speichermedium" kümmert sich um die Verwaltung der Daten, welche die drei Funktionen dokumentieren/analysieren. Diese werden dann auf Anfrage vom DataClient wieder ausgegben, im gewünschten Format (einzelne Informationen oder Datensätze).
     
## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->
- Speichern:
     - Die Daten aus den Funktionen, sowie der ConfigFile in einem Speichermedium sichern
- Suchen:
     - Informationen dem DataClient auf Anfrage zur Verfügung stellen
- Löschen:
     - Daten entfernen

## Kollaborationen
<!-- Benutzeranfragen an Dienste, die benötigt werden um Veranwortlichkeiten zu erfüllen -->
<!-- enthüllen Kontroll- und Informationsflüsse, und somit Subsysteme -->
<!-- Können fehlende Verantwortlichkeiten offenbaren, bzw. fehlerhaft zugewiesene -->
- DataClient:
     - Gibt ihm mit der Klasse Suchen, die Informationen weiter
- Drei Funktionen:
     - Greifen auf die Klasse Speichern zu und können somit die Daten abspeichern
- Alle vier:
     - können auf die Klasse löschen/ändern zugreifen


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
**Gedanken von Anfang bis Ende über das Speichermedium**
1. Welche Aufgaben hat das Speichermedium/soll es zur Verfügung stellen?
- ***Es muss zuerst die Art des Speichermediums entschieden werden***.. (Datenbank oder Datei) ..
***Da dies noch in Besprechung ist, gehe ich aktuell von einer Datei aus.***
- Neben dem **Als was** etwas abgespeichert werden soll gibt es noch andere Anforderungen
- Es existiert eine Oberklasse **SpeicherClient**, die in Verbindungen mit den Funktionen an sich steht
- Die Funktionen die zum aktuellen Zeitpunkt zur Verfügung gestellt werden sollen, sind **Speichern/Schreiben**, **Suchen/Lesen** und **Ändern**
- Damit ist gemeint, dass die Funktion **Suchen** dem *DataClient* zur Verfügung stehen soll und die Funktionen **Speichern** und **Löschen/Aendern**, den Funktionen *Zoom Maps*, *Codecharts und *Webcam basiertes Eyetracking*
- Da die 3 großen Funktionen aus mehreren Unterfunktionen besteht, werden diese zu jeweils 3 Klassen
2. Was macht die Klasse ***Suchen*** ?
- Diese muss nur dem DataClient zur Verfügung gestellt werden
- DataClient kann speziell nach Informationen suchen
- Besitzt für alle 3 Funktionen spezielle Suchen, für die jeweiligen Daten
- Besitzt die Möglichkeit nach Dateinnamen als auch nach allen Daten von einer Funktion zu suchen
- Kann einzelne Daten (falls notwendig) als auch einen kompletten Datensatz ausgeben
3. Was macht die Klasse ***Speichern***
- Diese Klasse steht den drei Funktionen zur Verfügung
- Es wird für jede Funktion eine eigene Datei erstellt in der die Informationen gespeichert werden, dadurch wird verhindert das es zu "Vermischungen" der Daten kommt
- durch das getrennte Speichern wird auch die Klasse *Suchen* leichter zu implementieren
- Stellt jeder Funktion eine einheitliche Speicherung der Infromationen in der Datei sicher
- muss in Absprache mit den Funktionen erstellt werden
- besitzt die Möglichkeit den Dateien Namen zu geben, ansonsten standard -> Datum der Erstellung
4. Was macht die Klasse ***Löschen/Aendern***
- Sie ermöglicht es alte Datensätze zu löschen
- Steht dem Dataclient zur Verfügung (Falls gewünscht ist, das nach der Analyse die Daten gelöscht werden sollen (oder weil nur die graphische Information von interesse ist))  

- In der Zukunft, könnte je nach Wahl des Speichermediums, eine Kollaboration mit dem Config-Modul nötig sein, damit der Datenanalyseclient auf die benutzte Konfiguration zugreifen kann.
