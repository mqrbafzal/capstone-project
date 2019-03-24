# Deployment
[<- Zurück zur Übersicht](/deployment-hosting/README.md)
# Inhaltsverzeichnis
- [2. Deployment](README.md)
    - [2.1. Grundlagen](grundlagen.md)
    - **2.2. Server Software**

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
Gitlab bietet im Gegensatz zu Github eine eigene Implementierung für [Kontinuierliche Integration](grundlagen.md#Kontinuierliche-Integration) und [Kontinuierliches Deployment](grundlagen.md#Kontinuierliches-Deployment).
Diese gliedert sich wie folgt in den Prozess eines Deployments ein:

<img alt="Gitlab CI&CD" src="_assets/img/cicd_pipeline_infograph.png" width="100%" />

- CI Pipeline : Hier werden [automatisierte Tests, UnitTests](grundlagen.md#testing) durchgeführt. Falls erforderlich wird vorher ein [Build der Software angefertigt](grundlagen.md#build).
- CD Pipeline : Hier wird ein letztes Review des Codes und der Test (meistens) durch eine Person/ein Team durchgeführt und dann wird der Release der Software automatisch auf die verschiedenen Systeme deployed.

## Software für manuelles Deployment

### Rsync
[Rsync](https://rsync.samba.org/) synchronisiert Dateien und Ordner eines Quellverzeichnisses mit einem Zielverzeichnis. 
Dabei können die Dateien anhand von Merkmalen, wie z.B. die Prüfsumme, zuletzt bearbeitet, Größe, Inhalt verglichen werden.
Eine Besonderheit an Rsync ist, dass ein Delta-Sync ausgeführt werden kann. 
Dabei werden nur die geänderten/hinzugefügten Bytes einer Datei neu übertragen, was bei großen Dateien viel Übertragungszeit spart.

### Filezilla
[Filezilla](https://filezilla-project.org/) ist ein populäres FTP Programm, welches über eine GUI dem Benutzer die Möglichkeit bietet Dateien per Drag&Drop von einem Quellverzeichnis 
(meistens lokal) in ein Zielverzeichnis (meistens auf dem Zielserver) zu kopieren. Als Grundlegende Übertragungsmethode kann hier FTP, FTPS und SFTP (FTP via Shell) verwendet werden. 

## Autoren

|      Name       |               E-Mail               |  Änderungsdatum  |
|:----------------|:-----------------------------------|:-----------------|
| Philipp Bischof | philipp.bischof@smail.uni-koeln.de |    20.03.2019    |
| Edriss Mosafer  | mmosafe1@smail.uni-koeln.de        |    20.03.2019    |
| Abdelhadi Ankoud| aankoud@outlook.de                 |    20.03.2019    |
