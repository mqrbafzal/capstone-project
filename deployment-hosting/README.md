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
