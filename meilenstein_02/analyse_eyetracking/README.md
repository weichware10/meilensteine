# Initial Exploration Eyetracking

<!-- Hier alles aufschreiben, was interessant erscheint! -->
- Wie errechnet man die Koordinaten die die Pupillen ansehen?
- Wie kalibriert man am Besten?
- Gibt es einen idealen Abstand?
- Wie sychronisiert man Bild und Koordinaten um nicht riesige Videodateien anzulegen?

## Was sind die Ziele des Systems?
<!-- Snow Cards können bei diesem Schritt helfen! -->
- Ziel des Systems ist den Bereich des Bildschirms festzustellen auf den der Nutzer konzentriert ist.
- Die Koordinaten und der Zeitstempel werden weitergegeben, damit zu jedem Zeitpunkt klar ist auf welchen Teil des Bilds der Nutzer geschaut hat.

## Was ist der erwartete Input?
- Bildschirmgröße und ein Video/Bild auf dem die Augen, insbesondere die Pupillen zu sehen sind.

## Was ist der erwartete Output?
- Koordinaten auf dem Bildschirm
- ggf. Zeitstempel

## Was sind Nomen Phrasen?
<!-- Alle relevanten Sachen aufschreiben, später kann aussortiert werden! -->
- Webcam basierte Eyetracking
- Person
- beliebig geladenes Bild
- Webcam
- Videoaufnahme von Bildschirm und Person
- Augen
- Pupillen
- Kalibrierung
- Blickbereich

## Liste der Klassen:
<!-- Erstmal alle aufschreiben, dann auswählen! (Kriterien siehe Vorgehensweise) -->
<!-- Warum sind die Klassen existent? Wenn das zu beantworten ist - u good! -->
<!-- ausgewählte Klassen mit Link, andere einklammern und CRC-Karte löschen -->
- [Auge](crc-auge.md)
- [Karte](crc-karte.md)
- [Results](crc-results.md)
- [Setup](crc-setup.md)

---

# Analyse - {Thema}
<!-- Hier Notizen zum Denkprozess! -->

## Verantwortlichkeiten
<!-- Wissen, welches verwaltet und angeboten wird, Aktion die angeboten werden, öffentliche Leistung -->
<!-- "Walkthrough" -> Szenarien zur Anwendung des Systems -->
<!-- Nichts, was eine andere Klasse machen könnte -->
<!-- Die Sachen die die Klasse macht -> keiner anderen Klasse geben -->
<!-- zentrale Verantwortlichkeiten vs verteilt -->

## Kollaborationen
<!-- Benutzeranfragen an Dienste, die benötigt werden um Veranwortlichkeiten zu erfüllen -->
<!-- enthüllen Kontroll- und Informationsflüsse, und somit Subsysteme -->
<!-- Können fehlende Verantwortlichkeiten offenbaren, bzw. fehlerhaft zugewiesene -->

## Finden von Abstrakten Klassen
<!-- Konkrete Klassen: Instanziierung und Vererbung
     Abstrakte Klassen: Nur Vererbung! -->
<!-- Unterklassen sollten alle geerbten Verantwortlichkeiten unterstützen, eher noch mehr -->
<!-- Gemeinsame Verantwortlichkeiten sollten so weit hoch wie möglich geschoben werden -->
<!-- Abstrakte Klassen erben nie von Konkreten Klassen! -->
<!-- Klassen die keine neue Funktionalität hinzufügen sollten eliminiert werden! -->
<!-- Letzte Folien der Vorlesung sind hilfreich hierfür! -->
