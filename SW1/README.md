# Anforderungen

## Inhaltsverszeichnis

- [Know-How & Begriffe](#know-how--begriffe)
  - [Inhaltsverszeichnis](#inhaltsverszeichnis)
    - [Webserver](#webserver)
    - [Domain Name System](#domain-name-system)
    - [Information fremder Server](#information-fremder-server)
    - [Proxy](#proxy)
    - [DMZ](#dmz)

### Webserver aufsetzen

loginname: localadmin
PW: Admin123

**Schritt 1: Installieren von Apache**

```
sudo apt-get update

sudo apt-get upgrade

sudo apt install apache2
```

**Schritt 2: Firewall anpassen**

```
sudo ufw app list
```

Zeigt die Anwendungsprofile an. Der Ouput sollte wie folgt aussehen:

```
Output
Available applications:
    Apache
    Apache Full
    Apache Secure
```

Die drei Anwendungsprofile öffnen verschiedene 