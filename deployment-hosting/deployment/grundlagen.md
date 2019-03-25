# Deployment
[<- Zurück zur Übersicht](/deployment-hosting/README.md)
# Inhaltsverzeichnis
- [2. Deployment](README.md)
    - **2.1. Grundlagen**
        - [2.1.1. Building](#Building)
        - [2.1.2. Testing](#Testing)
            - [2.1.2.1 Unit Tests](#Unit-Tests)
            - [2.1.2.2 Integration Tests](#Integration-Tests)
        - [2.1.3. Kontinuierliche Integration](#Kontinuierliche-Integration)
        - [2.1.4. Kontinuierliches Deployment](#Kontinuierliches-Deployment)
        - [2.1.5. Manuelles Deployment](#Manuelles-Deployment)
    - [2.2. Server Software](software.md)

## Grundlagen

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

### Kontinuierliche Integration
#### Erläuterung
Continuous Integration ist ein Verfahren, bei der Entwickler alle Codeänderungen regelmäßig in einem zentralen Repository zusammenführen. Diese Änderungen werden dann automatisiert erstellt und getestet. Die Hauptziele der Continuous Integration bestehen darin, Bugs schneller zu entdecken und zu beheben, die Software-Qualität zu optimieren und den Zeitraum zu minimieren, in dem neue Software-Aktualisierungen validiert und eingeführt werden.

#### Funktionsweise
Bei der Continuous Integration führen Entwickler regelmäßig einen Commit in einem gemeinsam genutzten Repository durch. Dafür wird ein Versionskontrollsystem wie Git verwendet. Vor jeder Durchführung eines Commit können Entwickler lokale Einheitstests für ihren Code durchführen. Sie erhalten dadurch eine zusätzliche Überprüfungsebene vor der Integration. Ein Continuous Integration-Dienst erstellt automatisch Einheitentests für neue Codeänderungen und führt diese aus, um ggf. vorhandene Fehler sofort aufzudecken.

#### Vorteil
In der Vergangenheit haben die Entwickler eines Teams meist isoliert an ihren Aufgaben gearbeitet und ihre Änderungen erst dann an der Hauptverzweigung zusammengeführt, wenn sie abgeschlossen waren. Mit CI werden Änderungen regelmäßig und zeitnah bereitgestellt.


### Kontinuierliches Deployment
Continuous Deployment und Continuous Delivery sind beides Teile der Continuous Integration, die bereits seit vielen Jahren in der Software-Entwicklung eingesetzt wird. Grundsätzlich geht es hierbei darum, dass die Software kontinuierlich weiterentwickelt wird, dabei jedoch höchster Wert auf eine Perfektionierung der Software und vor allem eine kontinuierliche Auslieferungsfähigkeit geachtet wird.
Im Rahmen des Continuous Deployment werden alle Änderungen an der Software automatisiert und nach festen Kriterien in die aktuelle Software beziehungsweise in die Produktion überführt. Auf diese Weise wird eine kontinuierliche Auslieferung der Software ermöglicht.
Obwohl umgangssprachlich fälschlicherweise oftmals als Synonym für Kontinuierliche Auslieferung verwendet, bezeichnet der Begriff Continuous Deployment eine weitergehende Form des Continuous Delivery, bei dem auch die Auslieferung der Software auf die Produktiv-Infrastruktur durchgeführt wird. Im Gegensatz dazu wird die Software bei Continous Delivery nur in eine Staging-Area ausgeliefert, von der sie dann manuell auf die Produktivinfrastruktur veröffentlicht werden kann.

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
