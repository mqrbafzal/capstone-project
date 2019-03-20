# Deployment & Hosting




# Hosting

## Grundlagen

### Rechenzentrum

### Server
Ein Server ist ein Computer, welcher meistens zusammen mit mehreren anderen Servern in einem Rechenzentrum steht.

#### vServer
KVM ?


#### Dedicated/Rootserver


## Server Software

### Betriebssysteme
Betriebssysteme bieten die Grundlage eines jeden Computers/Servers.
Im Hosting Bereich werden hauptsächlich kostenlose Linuxbasierende Systeme, wie Debian, Ubuntu, CentOS eingesetzt.
Für Hosting von Microsoft Produkten (Exchange,SharePoint,...) können fast ausschließlich Server mit dem Betriebsystem Microsoft Server eingesetzt werden.
Dafür werden einmalige oder jährliche Linzenzgebühren fällig.


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


## Anbieter
Generell kann man bei den Anbietern, anhand der Abrechnungsmodelle, in zwei Kategorien unterteilen.
- Kategorie 1:[Nutzungsbasierte Abrechnung](README.md#Nutzungsbasierte-Abrechnung) Wird immer beliebter wird (obwohl sie nicht immer die bessere/günstigere Variante ist). 
- Kategorie 2: [Monatliche Abrechnung](README.md#Monatliche-Abrechnung) für vServer/Dedicated Server.


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

## Methoden

### Kontinuierliche Integration
# Erläuterung
Continuous Integration ist ein Verfahren, bei der Entwickler alle Codeänderungen regelmäßig in einem zentralen Repository zusammenführen. Diese Änderungen werden dann automatisiert erstellt und getestet. Die Hauptziele der Continuous Integration bestehen darin, Bugs schneller zu entdecken und zu beheben, die Software-Qualität zu optimieren und den Zeitraum zu minimieren, in dem neue Software-Aktualisierungen validiert und eingeführt werden.

# Funktionsweise
Bei der Continuous Integration führen Entwickler regelmäßig einen Commit in einem gemeinsam genutzten Repository durch. Dafür wird ein Versionskontrollsystem wie Git verwendet. Vor jeder Durchführung eines Commit können Entwickler lokale Einheitstests für ihren Code durchführen. Sie erhalten dadurch eine zusätzliche Überprüfungsebene vor der Integration. Ein Continuous Integration-Dienst erstellt automatisch Einheitentests für neue Codeänderungen und führt diese aus, um ggf. vorhandene Fehler sofort aufzudecken.

# Vorteil
In der Vergangenheit haben die Entwickler eines Teams meist isoliert an ihren Aufgaben gearbeitet und ihre Änderungen erst dann an der Hauptverzweigung zusammengeführt, wenn sie abgeschlossen waren. Mit CI werden Änderungen regelmäßig und zeitnah bereitgestellt.

### Kontinuierliches Deployment

### Manuelles Deployment
Das manuelle Deployment wird von einer oder mehrerer Personen durchgeführt und überwacht. 
Dabei werden alle Update/Installations Prozesse initial von einer Person angestoßen. 
Eine Deployment Routine kann vorgegeben sein, jedoch ist diese nicht automatisiert (wie beim [Kontinuierlichen Deployment](README.md#Kontinuierliches-Deployment)).



## Software für kontinuierliche Integration/kontinuierliches Deployment

### Jenkins

### Travis


### Gitlab
Gitlab bietet im Gegensatz zu Github eine eigene Implementierung für [Kontinuierliche Integration](README.md#Kontinuierliche-Integration) und [Kontinuierliches Deployment](README.md#Kontinuierliches-Deployment).
Diese gliedert sich wie folgt in den Prozess eines Deployments ein:

<img alt="Gitlab CI&CD" src="_assets/img/cicd_pipeline_infograph.png" width="100%" />

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
|                 |                                    |                  |
