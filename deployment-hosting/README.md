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

### Betriebsysteme

### Docker

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

<img alt="Gitlab CI&CD" src="_assets/img/cicd_pipeline_infograph.png" width="150" />

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
