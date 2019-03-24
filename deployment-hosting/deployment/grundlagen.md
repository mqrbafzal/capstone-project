### Kontinuierliche Integration
#### Erläuterung
Continuous Integration ist ein Verfahren, bei der Entwickler alle Codeänderungen regelmäßig in einem zentralen Repository zusammenführen. Diese Änderungen werden dann automatisiert erstellt und getestet. Die Hauptziele der Continuous Integration bestehen darin, Bugs schneller zu entdecken und zu beheben, die Software-Qualität zu optimieren und den Zeitraum zu minimieren, in dem neue Software-Aktualisierungen validiert und eingeführt werden.

#### Funktionsweise
Bei der Continuous Integration führen Entwickler regelmäßig einen Commit in einem gemeinsam genutzten Repository durch. Dafür wird ein Versionskontrollsystem wie Git verwendet. Vor jeder Durchführung eines Commit können Entwickler lokale Einheitstests für ihren Code durchführen. Sie erhalten dadurch eine zusätzliche Überprüfungsebene vor der Integration. Ein Continuous Integration-Dienst erstellt automatisch Einheitentests für neue Codeänderungen und führt diese aus, um ggf. vorhandene Fehler sofort aufzudecken.

#### Vorteil
In der Vergangenheit haben die Entwickler eines Teams meist isoliert an ihren Aufgaben gearbeitet und ihre Änderungen erst dann an der Hauptverzweigung zusammengeführt, wenn sie abgeschlossen waren. Mit CI werden Änderungen regelmäßig und zeitnah bereitgestellt.

### Building
Beim Building handelt es sich um das Compilieren des Codes und das Linken von verwendeten Bibliotheken mit dem fertigen Release. Auch können beim Building zusätzliche Code Dateien mit Hilfe von Code-Generatoren generisch erzeugt werden. 

### Testing
Um Fehler in der Software möglichst gering zu halten sollte man ein umfangreiches Testing der Software implementieten.
Das Testing kann im Fluss der kontinuierlichen Integration automatisch angestoßen werden und benötigt keine weiteren Eingaben eines Benutzers.
Beim Testen gibt es unterschiedliche Möglichkeiten Test-Cases zu entwerfen. 

#### Unit Tests
Bei einem Unit Test wird ein einzelnes Modul (Unit) getestet. Beispiel: stellen wir uns einen Reifen eines Autos als Modul vor. 
Mögliche Unit Tests dazu wären:
- Stimmt das Profil des Reifens?
- Stimmt der Luftdruck des Reifens?
- Wenn ich mehr Luft in den Reifen pumpe befindet sich auch mehr Luftdruck im Reifen?

#### Integration Tests
Bei einem Integration Test wird meistens eine Userstory modeliert und getestet. 
Grundsätzlich wird die Zusammenarbeit zwischen unterschiedlichen Modulen der Software getestet.
Beispiel: stellen wir uns wieder das Auto vor.
Mögliche Integration Tests im Bezug zum Reifen wären:
- Fällt der Reifen ab wenn ich mit 100 durch die Kurve fahre?
- Wenn ich bei 50 km/h um 15 Grad nach links einlenke kommt der Reifen dann gegen die Achse?


### Kontinuierliches Deployment

### Manuelles Deployment
Das manuelle Deployment wird von einer oder mehrerer Personen durchgeführt und überwacht. 
Dabei werden alle Update/Installations Prozesse initial von einer Person angestoßen. 
Eine Deployment Routine kann vorgegeben sein, jedoch ist diese nicht automatisiert (wie beim [Kontinuierlichen Deployment](#Kontinuierliches-Deployment)).


## Autoren

|      Name       |               E-Mail               |  Änderungsdatum  |
|:----------------|:-----------------------------------|:-----------------|
| Philipp Bischof | philipp.bischof@smail.uni-koeln.de |    20.03.2019    |
| Edriss Mosafer  | mmosafe1@smail.uni-koeln.de        |    20.03.2019    |
| Abdelhadi Ankoud| aankoud@outlook.de                 |    20.03.2019    |
