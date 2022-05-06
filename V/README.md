# Sicherheits - und Betriebskonzept
## Inhaltsverszeichnis
- [1. Kapitel](#1-kapitel)
- [2. Kapitel](#2-kapitel)
- [Weitere Kapitel](#weitere-kapitel)

### Soll-Zustand
Es sollen 3 Virtuelle System bereitgestellt werden, diese sollen 24/7 zur Verfügung stehen. Die drei virtuelle Systeme werden von einem Externen Anbieter gehostet. Sie sollen zudem unabhängig voneinander fungieren.

### Mailserver
Unser Mailserver wird auf der TBZ-Cloud gehostet, dieser wird mittel Postfix fungieren.


### Webserver 
Der Webserver wir mittels Apache2 auf einem Ubuntu Server installiert. Dieser wird in der DMZ sein.

### CMS
Unser Onlineshop wird mit WordPress gestaltet. Dies wird dann an unseren Webserver angebunden.

### Verfügbarkeit
Grundsätzlich bieten wir unseren Webshop 24/7 an. Die Verfügbarkeit muss gewährleistet werden. Um dies zu gewährleisten wird unsere Infrastruktur mit einem Monitoring-Tool überwacht. Falls das Monitoring-Tool einen Fehler/Ausfall detektieren sollte, kommt unser Picket dienst zum Einsatz. Der Picket dienst wird für Notfälle 24/7 zur Verfügung stehen, auch während Feiertage und Ferien.

### Externer Zugriff
Das Verwalten der Infrastruktur auf der Hardwareseite wird von einem Externen-Partner übernommen. Das Verwalten und Pflegen der Serverinfrastruktur wird von Intern via Remoteanwendung realisiert. Dies hat den Vorteil, dass wir von überall aus zugreifen können. Zudem ist es für Unternehmen, welche auch auf unsere Infrastruktur zugreifen müssen angenehmer sich per Remote zu verbinden.

### Gefahren und Risiken
Um unsere Server nach aussen gut zu schützen, müssen strikte Regeln eingeführt werden. Man muss jede mögliche Angriffsstelle schliessen. Dazu gehören strikte und präzise Regeln der Firewall, nicht benötigte Ports werden geschlossen und das segmentieren in verschiedenen VLANS und DMZ.
Wichtig ist auch, regelmässige Backups durchzuführen, das in einem Ernstfall schnell reagiert werden kann. 

### Backupkonzept
Für die Sicherung der Daten, werden wir stündlich ein Backup machen. Diese Backups werden für die nächsten zwei Wochen gespeichert. Jeden Sonntagabend wird zudem ein Backup gemacht, welches für die nächsten 5 Jahre gespeichert wird. 
Zudem werden wir Jährliche ein Backup mit einem Tape durchführen. Dieses Tape wird an einen sicheren Ort gebracht, beispielsweise auf die Bank. 
