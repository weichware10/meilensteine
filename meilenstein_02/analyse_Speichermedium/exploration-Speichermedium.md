# Initial Exploration Speichermedium

<!-- Hier alles aufschreiben, was interessant erscheint! -->
    - In Welchen Größen werden die Daten von den Funktionen geliefert ?
    - In Welchen Größen möchte der DataClient Informationen erhalten ?
    - Wie sieht die Datenstruktur für die gespeicherten Daten aus ?
    - Werden die Daten als Dateien oder in einer Datenbank gespeichert ?
    - Was passiert bei einer Unterbechung zwischen Dataclient - Speichermedium und Funktion - Speichermedium ?
    - Werden noch weitere Funktionen als die Basics benötigt ?

## Was sind die Ziele des Systems?
<!-- Snow Cards können bei diesem Schritt helfen! -->
    - Es sollen die Daten von den drei Funktionen gespeichert werden, jede Funktion speichert jeweils in einer eigenen Datei
    - Es ist möglich Dateien zu erstellen für verschiedene Datensätze der Funktionen von verschiedenen Versuchen
    - Es wird dem Dataclient eine Klasse mit Funktionen zur Verfügung gestellt, welche ihm ermöglichen nach Informationen, Dateien, als auch ganzen Datenordnern zu suchen
    - Das System ermöglicht es Datensätze auch wieder zu löschen

## Was ist der erwartete Input?
    Es werden Datensätze von den Funktionen *Zoom Maps*, *Codecharts* und *Webcam basiertes Eyetracking* erwartet. 
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
