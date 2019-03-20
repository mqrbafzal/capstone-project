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
# Erläuterung
Continuous Integration ist ein Verfahren, bei der Entwickler alle Codeänderungen regelmäßig in einem zentralen Repository zusammenführen. Diese Änderungen werden dann automatisiert erstellt und getestet. Die Hauptziele der Continuous Integration bestehen darin, Bugs schneller zu entdecken und zu beheben, die Software-Qualität zu optimieren und den Zeitraum zu minimieren, in dem neue Software-Aktualisierungen validiert und eingeführt werden.

# Funktionsweise
Bei der Continuous Integration führen Entwickler regelmäßig einen Commit in einem gemeinsam genutzten Repository durch. Dafür wird ein Versionskontrollsystem wie Git verwendet. Vor jeder Durchführung eines Commit können Entwickler lokale Einheitstests für ihren Code durchführen. Sie erhalten dadurch eine zusätzliche Überprüfungsebene vor der Integration. Ein Continuous Integration-Dienst erstellt automatisch Einheitentests für neue Codeänderungen und führt diese aus, um ggf. vorhandene Fehler sofort aufzudecken.

# Vorteil
In der Vergangenheit haben die Entwickler eines Teams meist isoliert an ihren Aufgaben gearbeitet und ihre Änderungen erst dann an der Hauptverzweigung zusammengeführt, wenn sie abgeschlossen waren. Mit CI werden Änderungen regelmäßig und zeitnah bereitgestellt.

### Manuelles Deployment

## Software für kontinuierliche Integration

### Jenkins

### Travis


### Gitlab

## Software für manuelles deployment


## Autoren

|      Name       |               E-Mail               |  Änderungsdatum  |
|:----------------|:-----------------------------------|:-----------------|
| Philipp Bischof | philipp.bischof@smail.uni-koeln.de |    20.03.2019    |
|                 |                                    |                  |
