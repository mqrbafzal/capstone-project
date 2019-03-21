<h1 align="center">
  <p>
    <img alt="Meteor" src="assets/img/meteor.png" width="400" />
  </p>
  Meteor JS </br>
</h1>

## Übrsicht
- [Beschreibung](#Beschreibung)
- [Einsatzgebiet](#Einsatzgebiet)
- [Vor- und Nachteile](#Vor--und-Nachteile)
- [Tutorials](#Tutorials)
- [CodeSnippets](#Code-Snippets)
- [Quellen/Links](#Quellen-und-weitere-Links)

## Beschreibung

MeteorJS ist ein Open-Source Javascript Framework serverseitig basierend auf NodeJS. Durch die einfache Trennung von Client, Server und Smartphone-App Codeteilen soll es den Programmierern das Entwickeln von Web- und Mobile-Apps vereinfachen.

Ein kleines Team aus San Francisco entwickelt die auf JavaScript basierende Full-Stack-Webentwicklungs-Plattform Meteor seit 2011. Seit 2012 hat es dafür 11,2 Millionen US-Dollar Venture Capital bekommen. Das Ziel: die Entwicklung komplexer Web-Applikationen radikal vereinfachen. Der Meteor-Programmcode selbst ist Open Source und steht unter MIT-Lizenz. Meteor ist vielmehr eine Plattform als nur ein Framework. Das Rad wird nicht neu erfunden, aber es werden eine Reihe etablierter Technologien und Konzepte geschickt zusammengeführt. Dadurch entsteht ein komplexes Standardverhalten out of the box. Die wichtigsten Meteor-Komponenten im Überblick:

* Webserver / Laufzeitumgebung auf Basis von Node.js
* NoSQL Datenbank bzw. „Document Store“ mit MongoDB
* Gespiegelte Datenbank im Client. Die Elemente aus der Datenbank, die für den aktuellen View benötigt werden, sind in einer lokalen Datenbank im Client gespiegelt. Die clientseitige Datenbank wird mit derselben API angesprochen, wie die Datenbank auf dem Server. So schreibt man den Code zum Datenbankzugriff nur einmal und Meteor kümmert sich um die Ausführung auf Client UND Server.
* WebSocket-Support / Observer für Echtzeitanwendungen
* Erweiterungen und Paket-Management mit „Smart Packages“
* Tools und Infrastruktur für das Building und Deployment
* Flexibles Frontend, für einfache Projekte kann man als Frontend-Framework das Meteor-eigene Blaze verwenden. Für komplexere Projekte fügt man  mit „einer Kommandozeile“ Unterstützung für Angular.js oder React.js zum eigenen Projekt hinzu
* Data-on-the-Wire, d.h zwischen Server und Client wird nicht serverseitig berechnetes HTML ausgetauscht, sondern typisierte Daten in Form von JSON (genauer: EJSON). Diese Daten werden auf dem Client mittels eines Template-Frameworks in HTML umgewandelt und dann am Bildschirm angezeigt


**Was bedeuted Fullstack Framework?**

Client-Server WebApps bestehen üblicherweise aus dem Backend, das auf einem Server läuft, und dem Frontend, das auf dem Client-Browser läuft. Im Backend befindet sich meist die Datenbank zur Speicherung der Daten, im Frontend die Anzeigelogik, aber auch zunehmend die Applikationslogik.

Die heutigen Browser geben mit JavaScript (ECMAScript) die clientseitige Programmiersprache vor. Auf dem Server kommen oft Frameworks für PHP, .NET oder Java zum Einsatz. Entwickler finden sich dann in der Situation wieder, nicht nur zwischen verschiedenen Programmiersprachen, sondern auch zwischen unterschiedlichen Programmierparadigmen wechseln zu müssen, wenn ihr Feature im Frontend und Backend gleichzeitig implementiert werden muss.

Das OpenSource JavaScript Framework Meteor.js geht einen anderen Weg: Als sogenanntes Fullstack JavaScript Framework kommt im Client und im Server JavaScript zum Einsatz. Hierbei kann das Build-Tool Meteor auch moderne ES 2015 Sprachfeatures oder TypeScript für ältere Browser verständlich übersetzen. Client und Server teilen sich durchgängige Programmierparadigmen. Der Entwickler schreibt den Code für sogenannte „Meteor Methods“ nur einmal, er kommt aber auf dem Client und dem Server parallel zur Ausführung. Dies wird oft gemacht, wenn Daten zu speichern sind und Konsistenz- und Rechtsprüfungen am Client ein schnelles Feedback an den Nutzer geben sollen. Die abschließende, verlässliche Prüfung findet zeitversetzt am Server statt. Auf dem Server wird node.js zur Ausführung des Codes verwendet.

### Einsatzgebiet

Meteor eignet sich aufgrund seines Fullstack-Ansatzes sehr gut, um schnell Prototypen für WebApps zu entwickeln. Während andere Teams noch ihren Web-Stack zusammenbauen, kann ein Meteor-Team nach Minuten schon loslegen. Die Tatsache, dass es Codeblöcke gibt, die auf dem Client und auf dem Server identisch zur Ausführung kommen, ist zuerst gewöhnungsbedürftig, aber dann sehr praktisch. Begeisterung erzeugt immer wieder die sogenannte Meteor Magie, wenn sich durch die Reaktivität ein Datensatz in einem Client „in Echtzeit“ ändert, weil ein anderer Client ihn gerade bei sich bearbeitet hat.

### Vor- und Nachteile

#### Vorteile
Meteor reduziert Front- , Back-End und Datenbank Programmiersprache auch durch den Einsatz von MongoDB auf eine einzige Programmiersprache, was es für Entwickler deutlich einfacher gestaltet, eine komplette Applikation zu entwickeln. Auch bei der Projektbetreuung kann man dadurch kleinere Entwickler-Teams bilden. Durch das Einsetzen von Packages erspart man sich viele Zeilen an Code, was sowohl beim Schreiben des Codes als auch in der Fehlerbehandlung Zeit spart.

#### Nachteile

Der Umstieg von der herkömmlichen Entwicklung auf die Full-Stack-Entwicklung ist gegebenenfalls problematisch. Auf der einen Seite muss jetzt nur noch eine Programmiersprache gelernt werden, jedoch müssen vormals reine Front-End-Enwickler sich nun Gedanken über die Logik einer Applikation machen, während sich vormals reine Back-End-Entwickler nun mit der Usability befassen müssen. Eine Trennung zwischen Backend- und Frontend-Entwickler ist natürlich weiterhin möglich; jedoch zeigen sich in der Praxis große Effizienzgewinne, wenn der Backend-Entwickler auch mal eine Kleinigkeit im Frontend anpassen kann oder umgekehrt. Full-Stack-Frameworks sind auch nicht für alle Arten von Applikationen einsetzbar oder man läuft Gefahr für spezielle Bedürfnisse nicht das bestmögliche Mittel zu verwenden. Würde man sich von einer Voll-Stack-Lösung distanzieren wollen und gewisse Bereiche mit anderen Sprachen oder Methoden ersetzen wollen, ist das in einem solchen Systemen manchmal etwas aufwändiger – oder zumindest ungewohnt.

## Tutorials

https://themeteorchef.com/

## Code Snippets

## Quellen und weitere Links

https://www.meteor.com/

https://github.com/meteor/meteor

http://www.404heroes.com/leitfaden/meteorjs-vor-und-nachteile-des-app-frameworks/1924

https://t3n.de/magazin/meteor-full-stack-javascript-plattform-fuer-echtzeit-web-234154/

https://www.methodpark.de/blog/meteor-das-fullstack-javascript-framework/

## Autoren

| Name         | E-Mail                          | Ã„nderungsdatum |
|:-------------|:--------------------------------|:---------------|
| Tim Dreesen | dreesen@wiso.uni-koeln.de | 20.03.2019     |
