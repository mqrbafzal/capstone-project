# Hosting
[<- Zurück zur Übersicht](/deployment-hosting/README.md)
# Inhaltsverzeichnis
- [1. Hosting](README.md)
    - **1.1. Grundlagen**
    - [1.2. Server Software](software.md)
    - [1.3. Anbieter](anbieter.md)
## Grundlagen

### Rechenzentrum (RZ)

<img max-width="400px" alt="Rechenzentrum CERN" src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d7/CERN_Server_03.jpg/640px-CERN_Server_03.jpg" width="100%">

> Rechenzentrum in CERN von Florian Hirzinger - <a rel="nofollow" class="external text" href="http://www.fh-ap.com">www.fh-ap.com</a> - Own work (Florian Hirzinger), <a href="https://creativecommons.org/licenses/by-sa/3.0" title="Creative Commons Attribution-Share Alike 3.0">CC BY-SA 3.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=6212692">Link</a>

Ein Rechenzentrum ist ein Gebäude, in dem mehrere Server betrieben werden und mit einer entsprechenden Infrastruktur versorgt werden. 
Dazu zählt meistens:
- Schnelle & Redundante Internet Anbindung
- Redundante Stromversorgung
- Erweitertes Sicherheitskonzept mit Zutrittskontrolle, Alarmanlage, usw.
- Besondere Brandschutzmaßnahmen
- Kühlungs-/Lüftungssystem


### Server

<img max-width="400px" width="100%" src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/69/Wikimedia_Foundation_Servers-8055_35.jpg/640px-Wikimedia_Foundation_Servers-8055_35.jpg">

>Mehrere Server in einem Server-Rack von <a href="//commons.wikimedia.org/wiki/User:Victorgrigas" title="User:Victorgrigas">Victorgrigas</a> - <span class="int-own-work" lang="de">Eigenes Werk</span>, <a href="https://creativecommons.org/licenses/by-sa/3.0" title="Creative Commons Attribution-Share Alike 3.0">CC BY-SA 3.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=20348454">Link</a>

Ein Server ist ein Computer, welcher meistens zusammen mit mehreren anderen Servern in einem Rechenzentrum steht.

#### vServer (virtuelle Server)
Aus der Sicht des Hardware-Systems sind vServer meistens nur reine Dateiverzeichnisse. Auf diesem Server wird nun eine Software installiert, die eine Virtualisierungsschicht zur Verfügung stellt. In dieser Applikation werden dann virtuelle Rechnersysteme wiederum installiert.

Warum vServer?
Webseiten-Betreiber brauchen Flexibilität und umfangreiche Rechte. Da ist ein eigenes Serversystem nur für den eigenen Bedarf genau das Richtige. Vor wenigen Jahren noch konnte man dies nur mit der Anmietung eines Hardware-Systems realisieren. Virtuelle Server sind dafür die billigere Variante.
Ein vServer empfiehlt sich dann, wenn Kunden mit Ihrem Webspace bei Webhosting-Anbietern nicht mehr auskommen oder die Anzahl an Usern ihrer Website zu groß wird und entsprechend mehr Ressourcen benötigt. Des Weiteren kann man vServer auch als ersten Einstieg für eine größere Zahl von Websites oder als kleinen Mailserver nutzen.

Virtualisierungstechniken: Im Wesentlichen gibt es drei Methoden, welche von den Virtualsierungsapplikationen genutzt werden.
  - Xen: ist ein Hypervisor, also eine Software, die den Betrieb mehrerer virtueller Maschinen auf einem physischen Computer erlaubt.            Xen läuft auf fast jeder aktuellen Hardware, auch ohne Virtualisierungsfeatures. Die Zukunftssicherheit ist allerdings aufgrund          der Bindung an älteren Linux-Kernel fraglich.
<img style="max-width: 150px" alt="KVM Logo" src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/70/Kvmbanner-logo2_1.png/640px-Kvmbanner-logo2_1.png"/>

> By <a href="//commons.wikimedia.org/w/index.php?title=User:O.T.S.U.&amp;action=edit&amp;redlink=1" class="new" title="User:O.T.S.U. (page does not exist)">O.T.S.U.</a> - <a rel="nofollow" class="external free" href="http://openvirtualizationalliance.org/downloads/kvm-logo_300dpi.png">http://openvirtualizationalliance.org/downloads/kvm-logo_300dpi.png</a>, <a href="https://creativecommons.org/licenses/by-sa/3.0" title="Creative Commons Attribution-Share Alike 3.0">CC BY-SA 3.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=24109871">Link</a>

  - KVM (kernel-based virtual machine): konvertiert Linux in einen Typ-1-Hypervisor (Bare-Metal). Alle Hypervisors benötigen die                                                 gleichen Komponenten auf Betriebssystemebene – wie zum Beispiel einen Speichermanager,                                                   Prozessplaner, Input/Output-Stack (I/O), Gerätetreiber, Sicherheitsmanager, Netzwerk-Stack und                                           mehr – um VM laufen lassen zu können. KVM verfügt über alle diese Komponenten, weil sie in den                                           Linux-Kernels integriert ist. Auf Seiten der Hardware setzt  es Intel VT / -V voraus. Es läuft                                           mit und in jew. aktuellem Standard-Linux-Kernel und besitzt daher eine hohe Zukunftssicherheit.
 <img style="max-width: 150px" alt="Virtuozzo Logo" src="https://upload.wikimedia.org/wikipedia/en/a/a6/Virtuozzo_company_logo.png" />

> By <a href="//en.wikipedia.org/wiki/Virtuozzo_(company)" title="Virtuozzo (company)">Virtuozzo</a> - <a rel="nofollow" class="external free" href="https://www.virtuozzo.com/">https://www.virtuozzo.com/</a>, Public Domain, <a href="https://en.wikipedia.org/w/index.php?curid=50973431">Link</a>
  - Virtuozzo(Containervisualiasierung): stellt keine Emulation von Hardware oder Abstraktionsschichten zum Ansprechen dieser bereit.                                            Stattdessen werden innerhalb eines laufenden Systems eigene, komplette Laufzeitumgebungen zur                                            Verfügung gestellt, die jedoch von einem gemeinsamen Kernel verwaltet werden. In der Verwendung                                          eines einzelnen Kerns liegt auch der entscheidende Nachteil dieses Lösungsansatzes: rst einmal                                          kann ein einzelner User durch die Ausnutzung von Sicherheitslücken innerhalb des                                                        Virtualisierungsprogramms gelingen, aus der eigenen Umgebung (Jail) auszubrechen. Zum anderen                                            kann auch der Kernel kompromittiert werden. Bei einer fehlerhaften Konfiguration ist es zudem                                            einem Nutzer möglich, sämtliche Ressourcen für eigene Prozesse zu nutzen. Bricht dann unter der                                          Last der Host zusammen, stürzen auch alle anderen VPS mit ab.Die Konfiguration ist wesentlich                                            einfacher als bei anderen Virtualisierungsansätzen, zudem wird durch die direkte Verwaltung der                                          Hardware eine wesentlich höhere Performance erzielt. Deshalb wird diese Technik zum Erstellen                                            virtueller Server besonders beim Webhosting gerne bevorzugt.

#### Dedicated- und Root-Server: Root-Server und Dedicated-Server sind bis auf die Hardware das selbe
Dedicated Server: 
Der Begriff Dedicated Server bezeichnet einen Server, der mit seiner gesamten Performance ausschließlich einem einzigen Kunden bzw. Websitebetreiber oder einer bestimmten Aufgabe bzw. einem Service zur Verfügung steht.

Root-Server:
Ein Root-Server ist ein Server, der eine grundlegende Funktion bei der Übersetzung eines Domain-Namens in eine IP-Adresse einnimmt. Er beantwortet Client-Anfragen (Requests) in der Root-Zone des Domain Name Systems.

Vergleich zu vServer:
Der Dedicated Server ist im Gegensatz zum vServer ein physikalischer Computer mitsamt fester IP-Adresse, der seine ganze Rechenleistung, seinen Arbeitsspeicher und die Leitungsanbindung auf nur einen Kunden oder eine Aufgabe konzentrieren kann. Der Root Server empfiehlt sich dann, wenn man viel mehr Ressourcen benötigt als ein vServer bieten kann und auf schnelle Datenzugriffe angewiesen ist. Gerade bei großen Communities oder eine Website mit vielen Datenzugriffen empfiehlt sich der Wechsel vom vServer zum Root Server. Durch die dedizierten Festplatten bei den Root Server kann der schnellere Datenzugriff im Vergleich zum vServer gewährleistet werden.


## Autoren

|      Name       |               E-Mail               |  Änderungsdatum  |
|:----------------|:-----------------------------------|:-----------------|
| Philipp Bischof | philipp.bischof@smail.uni-koeln.de |    20.03.2019    |
| Edriss Mosafer  | mmosafe1@smail.uni-koeln.de        |    20.03.2019    |
| Abdelhadi Ankoud| aankoud@outlook.de                 |    20.03.2019    |