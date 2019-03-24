# Deployment & Hosting

# Inhaltsverzeichnis
- [1. Hosting](hosting/README.md)
    - [1.1. Grundlagen](hosting/grundlagen.md)
    - [1.2. Server Software](hosting/software.md)
    - [1.3. Anbieter](hosting/anbieter.md)
- [2. Deployment](deployment/README.md)


# Hosting

## Grundlagen

### Rechenzentrum
//TODO @Philipp

### Server
Ein Server ist ein Computer, welcher meistens zusammen mit mehreren anderen Servern in einem Rechenzentrum steht.

#### vServer (virtuelle Server)
Aus der Sicht des Hardware-Systems sind vServer meistens nur reine Dateiverzeichnisse. Auf diesem Server wird nun eine Software installiert, die eine Virtualisierungsschicht zur Verfügung stellt. In dieser Applikation werden dann virtuelle Rechnersysteme wiederum installiert.

Warum vServer?
Webseiten-Betreiber brauchen Flexibilität und umfangreiche Rechte. Da ist ein eigenes Serversystem nur für den eigenen Bedarf genau das Richtige. Vor wenigen Jahren noch konnte man dies nur mit der Anmietung eines Hardware-Systems realisieren. Virtuelle Server sind dafür die billigere Variante.
Ein vServer empfiehlt sich dann, wenn Kunden mit Ihrem Webspace bei Webhosting-Anbietern nicht mehr auskommen oder die Anzahl an Usern ihrer Website zu groß wird und entsprechend mehr Ressourcen benötigt. Des Weiteren kann man vServer auch als ersten Einstieg für eine größere Zahl von Websites oder als kleinen Mailserver nutzen.

Virtualisierungstechniken: Im Wesentlichen gibt es drei Methoden, welche von den Virtualsierungsapplikationen genutzt werden.
  - Xen: ist ein Hypervisor, also eine Software, die den Betrieb mehrerer virtueller Maschinen auf einem physischen Computer erlaubt.            Xen läuft auf fast jeder aktuellen Hardware, auch ohne Virtualisierungsfeatures. Die Zukunftssicherheit ist allerdings aufgrund          der Bindung an älteren Linux-Kernel fraglich.

  - KVM (kernel-based virtual machine): konvertiert Linux in einen Typ-1-Hypervisor (Bare-Metal). Alle Hypervisors benötigen die                                                 gleichen Komponenten auf Betriebssystemebene – wie zum Beispiel einen Speichermanager,                                                   Prozessplaner, Input/Output-Stack (I/O), Gerätetreiber, Sicherheitsmanager, Netzwerk-Stack und                                           mehr – um VM laufen lassen zu können. KVM verfügt über alle diese Komponenten, weil sie in den                                           Linux-Kernels integriert ist. Auf Seiten der Hardware setzt  es Intel VT / -V voraus. Es läuft                                           mit und in jew. aktuellem Standard-Linux-Kernel und besitzt daher eine hohe Zukunftssicherheit.
 
  - Virtuozzo(Containervisualiasierung): stellt keine Emulation von Hardware oder Abstraktionsschichten zum Ansprechen dieser bereit.                                            Stattdessen werden innerhalb eines laufenden Systems eigene, komplette Laufzeitumgebungen zur                                            Verfügung gestellt, die jedoch von einem gemeinsamen Kernel verwaltet werden. In der Verwendung                                          eines einzelnen Kerns liegt auch der entscheidende Nachteil dieses Lösungsansatzes: rst einmal                                          kann ein einzelner User durch die Ausnutzung von Sicherheitslücken innerhalb des                                                        Virtualisierungsprogramms gelingen, aus der eigenen Umgebung (Jail) auszubrechen. Zum anderen                                            kann auch der Kernel kompromittiert werden. Bei einer fehlerhaften Konfiguration ist es zudem                                            einem Nutzer möglich, sämtliche Ressourcen für eigene Prozesse zu nutzen. Bricht dann unter der                                          Last der Host zusammen, stürzen auch alle anderen VPS mit ab.Die Konfiguration ist wesentlich                                            einfacher als bei anderen Virtualisierungsansätzen, zudem wird durch die direkte Verwaltung der                                          Hardware eine wesentlich höhere Performance erzielt. Deshalb wird diese Technik zum Erstellen                                            virtueller Server besonders beim Webhosting gerne bevorzugt.

#### Dedicated- und Root-Server: Root-Server und Dedicated-Server sind bis auf die Hardware das selbe
Dedicated Server: 
Der Begriff Dedicated Server bezeichnet einen Server, der mit seiner gesamten Performance ausschließlich einem einzigen Kunden bzw. Websitebetreiber oder einer bestimmten Aufgabe bzw. einem Service zur Verfügung steht.

Root-Server:
Ein Root-Server ist ein Server, der eine grundlegende Funktion bei der Übersetzung eines Domain-Namens in eine IP-Adresse einnimmt. Er beantwortet Client-Anfragen (Requests) in der Root-Zone des Domain Name Systems.

Vergleich zu vServer:
Der Dedicated Server ist im Gegensatz zum vServer ein physikalischer Computer mitsamt fester IP-Adresse, der seine ganze Rechenleistung, seinen Arbeitsspeicher und die Leitungsanbindung auf nur einen Kunden oder eine Aufgabe konzentrieren kann. Der Root Server empfiehlt sich dann, wenn man viel mehr Ressourcen benötigt als ein vServer bieten kann und auf schnelle Datenzugriffe angewiesen ist. Gerade bei großen Communities oder eine Website mit vielen Datenzugriffen empfiehlt sich der Wechsel vom vServer zum Root Server. Durch die dedizierten Festplatten bei den Root Server kann der schnellere Datenzugriff im Vergleich zum vServer gewährleistet werden.
## Server Software

### Betriebsysteme

### Docker
Definition: Docker ist eine Softwareplattform zur Erstellung, zum Testen und zur Bereitstellung von Anwendungen. Hierbei verpackt Docker Software in standardisierte Einheiten, die als Container bezeichnet werden und alles enthalten, was zum Ausführen der Software erforderlich ist (Bibliotheken, Systemtools, Code und Laufzeit.)

Docker auf AWS: Das Ausführen von Docker auf AWS ermöglicht Entwicklern und Administratoren eine äußerst zuverlässige und kostengünstige Methode zum Erstellen, Versenden und Ausführen verteilter Anwendungen jeder Größe. AWS unterstützt beide Docker-Lizenzierungsmodelle: die Open-Source-basierte Docker Community Edition (CE) und die Abonnement-basierte Docker Enterprise Edition (EE).

Vorteile:
- Software kann schenller versendet werden 
    - Docker-Benutzer versenden Software im Durchschnitt siebenmal so häufig wie Benutzer, die Docker nicht verwenden. Docker ermöglicht       es Ihnen, einzelne Services so oft wie nötig zu versenden.
-Standardisiereung von Vorgängen
    - Kleine Anwendungen in Containern erleichtern das Bereitstellen, das Identifizieren und das Roll-Back zum Beheben von Problemen.
- Nahtloses Verschieben
    - Docker-basierte Anwendungen können nahtlos von lokalen Entwicklungsmaschinen zu Produktionsbereitstellungen verschoben werden.
- Einsparungen 
    - Docker-Container erleichtern die Ausführung von mehr Code auf den einzelnen Servern, wodurch die Nutzungsrate verbessert wird und       somit verbundene Kosten eingespart werden können.
    
Einsatzbereiche:
- Microservices (Vorteile von standardisierten Code-Bereitstellungen mithilfe von Docker-Containern nutzen)
- Laufende Integration und Bereitstellung (Beheben von Konflikten zwischen Sprach-Stacks und -Versionen)
- Datenverarbeitung (Big Data verarbeiten und als Service anbieten)
- "Container" als ein Service (Anwendungen mit Inhalten und Infrastruktur erstellen und vertreiben)
### Kubernetis
//TODO

## Anbieter
Generell kann man bei den Anbietern, anhand der Abrechnungsmodelle, in zwei Kategorien unterteilen.
- Kategorie 1:[Nutzungsbasierte Abrechnung](#Nutzungsbasierte-Abrechnung) Wird immer beliebter wird (obwohl sie nicht immer die bessere/günstigere Variante ist). 
- Kategorie 2: [Monatliche Abrechnung](#Monatliche-Abrechnung) für vServer/Dedicated Server.


### Nutzungsbasierte Abrechnung
#### Erläuterung
Abrechnung erfolgt nach dem Prinzip "Pay-as-you-use".
> Bei AWS bezahlen Sie nur für die Services, die Sie benötigen, so lange Sie diese nutzen und ohne langfristige Verpflichtung oder komplexe Lizenzierung.  AWS-Preise werden ähnlich wie Ihre Kosten für Wasser und Strom berechnet.  Sie zahlen nur für die Services, die Sie nutzen. Wenn Sie die Nutzung einstellen, fallen keine zusätzlichen Kosten oder Kündigungsgebühren an.

[AWS Erläuterung zu Preisen](https://aws.amazon.com/de/pricing/) - 2019

#### Anbieter

- [AWS (Amazon Web Services)](https://aws.amazon.com/de/) 
- [Google Cloud Platform](https://cloud.google.com)
- [Microsoft Azure](https://azure.microsoft.com/de-de/)
- [Heroku](https://www.heroku.com/)
### Monatliche Abrechnung
#### Erläuterung
Hier bezahlt man für Server wie für die Wohnungsmiete - monatlich oder jährlich. 
Es gibt eine Vertragslaufzeit mit entsprechender Kündigungsfrist. 
Man mietet einen Server mit einer Leistung, über welche man dann vollständig verfügt. 
Ob man diese komplett ausnutzt oder nicht bleibt einem selbst überlassen. 
Eine Preisreduktion bei geringer Nutzung gibt es nicht, man sollte dann einfachh einen Server mit geringerer Leistung buchen.

#### Anbieter
##### Deutschland
- [Strato](https://strato.de)
- [Hetzner](https://hetzner.de)
- [Ionos](https://ionos.de) (1&1, stellt um auf Nutzungsbasierte Abrechnung)
- [Netcup](https://netcup.de)
- [Domainfactory](https://df.eu)

##### Europa
- [Hosteurope](https://hosteurope.de)

# Deployment

## Grundlagen

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



## Software für kontinuierliche Integration/kontinuierliches Deployment

### Jenkins
[Jenkins](https://jenkins.io) ist ein erweiterbares, webbasiertes Software-System zur kontinuierlichen Integration.
Das Programm ist in der Programmiersprache Java geschrieben. Unterstützt werden verschiedene Build-Tools wie Apache Ant, Maven oder Gradle, Versionsverwaltungssysteme wie CVS, Subversion oder Git, automatische Testverfahren ("test tools") wie JUnit oder Emma. Durch verschiedene Zusatzmodule ("Plugins") können auch andere Compiler gesteuert werden, sodass neben Java- auch PHP-, Ruby- oder .NET-basierte Projekte verwaltet werden können. Neben CruiseControl ist Jenkins eines der am häufigsten eingesetzten Werkzeuge zur kontinuierlichen Integration.

### Travis
[Travis CI](https://travis-ci.com) ist eine freie und Open-Source-Software für kontinuierliche Integration und Deployment.
Die Software eignet sich zum Testen und Erstellen von Projekten, die auf GitHub veröffentlicht werden.
GitHub informiert Travis-CI-Projekte über Änderungen. Travis CI überprüft darauf den entsprechenden Ast und führt die Anweisungen aus der Konfigurationsdatei aus (z. B. Software aktualisieren, testen, Bericht erstellen oder E-Mail versenden).

Travis gibt es seit 2013 und hat rund 700.000 Anwender, darunter IBM, Zendesk, Heroku, Twitter und Facebook.
Als Programmiersprachen werden nahezu alle wichtigen Programmiersprachen unterstützt, darunter C, C++, C#, Clojure, D, Dart, Elixir, Erlang, F#, Go, Groovy, Haskell, Java, JavaScript, Julia, Objective-C, Perl, PHP, Python, R, Ruby, Rust, Scala, Smalltalk, Swift und Visual Basic. 

### Gitlab
Gitlab bietet im Gegensatz zu Github eine eigene Implementierung für [Kontinuierliche Integration](#Kontinuierliche-Integration) und [Kontinuierliches Deployment](#Kontinuierliches-Deployment).
Diese gliedert sich wie folgt in den Prozess eines Deployments ein:

<img alt="Gitlab CI&CD" src="_assets/img/cicd_pipeline_infograph.png" width="100%" />

- CI Pipeline : Hier werden [automatisierte Tests, UnitTests](#testing) durchgeführt. Falls erforderlich wird vorher ein [Build der Software angefertigt](#build).
- CD Pipeline : Hier wird ein letztes Review des Codes und der Test (meistens) durch eine Person/ein Team durchgeführt und dann wird der Release der Software automatisch auf die verschiedenen Systeme deployed.

## Software für manuelles Deployment

### Rsync
Rsync synchronisiert Dateien und Ordner eines Quellverzeichnisses mit einem Zielverzeichnis. 
Dabei können die Dateien anhand von Merkmalen, wie z.B. die Prüfsumme, zuletzt bearbeitet, Größe, Inhalt verglichen werden.
Eine Besonderheit an Rsync ist, dass ein Delta-Sync ausgeführt werden kann. 
Dabei werden nur die geänderten/hinzugefügten Bytes einer Datei neu übertragen, was bei großen Dateien viel Übertragungszeit spart.

### Filezilla
Populäres FTP Programm, welches über eine GUI dem Benutzer die Möglichkeit bietet Dateien per Drag&Drop von einem Quellverzeichnis 
(meistens lokal) in ein Zielverzeichnis (meistens auf dem Zielserver) zu kopieren. Als Grundlegende Übertragungsmethode kann hier FTP, FTPS und SFTP (FTP via Shell) verwendet werden. 



## Autoren

|      Name       |               E-Mail               |  Änderungsdatum  |
|:----------------|:-----------------------------------|:-----------------|
| Philipp Bischof | philipp.bischof@smail.uni-koeln.de |    20.03.2019    |
| Edriss Mosafer  | mmosafe1@smail.uni-koeln.de        |    20.03.2019    |
| Abdelhadi Ankoud| aankoud@outlook.de                 |    20.03.2019    |
