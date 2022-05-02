# Zertifikat für Webserver

## Inhaltsverszeichnis
- [1. Kapitel](#1-kapitel)
- [2. Kapitel](#2-kapitel)
- [Weitere Kapitel](#weitere-kapitel)

### Domäne njeritech.ch

Wir haben uns die Domäne beim Provider ``Hostpoint`` gekauft. Somit hatten wir eine gültige Domäne die wir für unsere Seite nutzen können, damit sich zukünftig Kunden einfacher unsere Seite besuchen können. 


### Zertifikat erstellen mit Certbot

Wir haben uns das Tool Certbot zur Hilfe genommen, um automatisiert ein SSL-Zertifikat zu erhalten welches auch automatisch erneuert wird. 

Zuerst muss man wie folgt zwei Pakete installieren im Terminal:

```
sudo apt install certbot python3-certbot-apache
```

Als nächstes müssen wir in der Apache Virtual Host-Konfiguration eine Änderung vornehmen. Folgendes wurde gemacht:

```
sudo nano /etc/apache2/sites-available/njeritech.ch-le-ssl.conf
```
In dieser Konfigurationsdatei sollte es ca. wie folgt aussehen:

![Konfig-Datei](images/Konfig.PNG)

Nun testen wir den Syntax der Konfigurationsdatei und laden den Dienst Apache neu. 

```
sudo apache2ctl configtest

sudo systemctzl reload apache2
```

Als nächstes sollte man auf der Firewall HTTPS zulassen. Dies hatten wir in einem vorherigen Schritt schon gemacht aber hier noch als wiederholugn:

```
sudo ufw allow 'Apache Full'

sudo ufw delete allow 'Apache'
```

Mit dem Befehl ```sudo ufw status``` kann man nun die Einstellungen überprüfen. Es sollte wie folgt aussehen:

![UFW-HTTPS](images/UFW-HTTPS.PNG)

### Weitere-Kapitel 
Text