# Hosting
[<- Zurück zur Übersicht](/deployment-hosting/README.md)
# Inhaltsverzeichnis
- [1. Hosting](README.md)
    - [1.1. Grundlagen](grundlagen.md)
    - **1.2. Server Software**
        - [1.2.1. Betriebssysteme](#betriebssysteme)
        - [1.2.2. LAMP](#LAMP)
        - [1.2.3. Docker](#Docker)
        - [1.2.4. Kubernetis](#Kubernetis)
    - [1.3. Anbieter](anbieter.md)

## Software

### Betriebssysteme
Betriebssysteme bieten die Grundlage eines jeden Computers/Servers.
Im Hosting Bereich werden hauptsächlich kostenlose Linuxbasierende Systeme, wie Debian, Ubuntu, CentOS eingesetzt.
Für Hosting von Microsoft Produkten (Exchange,SharePoint,...) können fast ausschließlich Server mit dem Betriebsystem Windows Server eingesetzt werden.
Dafür werden einmalige oder jährliche Linzenzgebühren fällig.

- [Debian](https://www.debian.org/index.de.html)
- [Ubuntu](https://www.ubuntu.com/download/server)
- [CentOS](https://www.centos.org/)
- [Windows Server](https://www.microsoft.com/de-de/cloud-platform/windows-server)

>Im Oktober 2012 wurden mindestens 32 % aller Webseiten auf einem Linux-Server gehostet. Da nicht alle Linux-Server sich auch als solche zu erkennen geben, könnte der tatsächliche Anteil um bis zu 24 Prozentpunkte höher liegen. Damit wäre ein tatsächlicher Marktanteil von bis zu 55 % nicht auszuschließen.
[Wikipedia](https://de.wikipedia.org/wiki/Linux-Einsatzbereiche#Marktanteile_2)

### LAMP
LAMP steht dabei als Abkürzung für den kombinierten Einsatz der Softwareprodukte **Linux**, **Apache**, **MySQL** und **PHP** (manchmal auch Perl oder Python). Diese Kombination ermöglicht es, auf einem Computer einen Webserver zu betreiben, der beim Aufruf der Seiten mit dem Webbrowser dynamische Inhalte aus Datenbanken zu generieren, und auch Inhalte wieder in diese Datenbank zu schreiben.


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
//TODO für zukünftige

## Autoren

|      Name       |               E-Mail               |  Änderungsdatum  |
|:----------------|:-----------------------------------|:-----------------|
| Philipp Bischof | philipp.bischof@smail.uni-koeln.de |    20.03.2019    |
| Edriss Mosafer  | mmosafe1@smail.uni-koeln.de        |    20.03.2019    |
| Abdelhadi Ankoud| aankoud@outlook.de                 |    20.03.2019    |