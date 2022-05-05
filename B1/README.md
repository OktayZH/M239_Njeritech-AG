# Benutzerkonzept

## Inhaltsverszeichnis

- [Benutzerkonzept](#benutzerkonzept)
  - [Inhaltsverszeichnis](#inhaltsverszeichnis)
    - [Administratormatrix](#administratormatrix)
    - [Persönliche Administratorenmatrix](#persönliche-administratorenmatrix)
    - [Erstellen root User Web-/ Mailserver](#erstellen-root-user-web--mailserver)

### Administratormatrix 

Diese Administratorkonten werden nur in Notfällen genutzt. Bei normalem Betrieb muss mit den persönlichen Administratorkonten gearbeitet werden, um Anpassungen oder Events nachverfolgen kann. Der Zugriff auf Hostpoint ist beschränkt auf einen Administratoren.

| Dienst | Benutzername | Berechtigungslevel | Location / URL |
| :---- | :--- | :--- | :--- |
| Webserver | localadmin | root | localhost |
| Mailserver | localadmin | root | localhost |
| Hostpoint | oktay_yildiran07@hotmail.com | Administrator | https://admin.hostpoint.ch/customer/Auth/Login |
| WordPress | wordpress@localhost | Administrator | https://njeritech.ch |


### Persönliche Administratorenmatrix

Mitarbeiter erhalten immer ein persönliches Administratorenkonto. Somit stärkt man auch das Verantwortungsbewusstsein des Mitarbeitenden und vermeidet Fehler.

| Dienst | Benutzername | Berechtigungslevel | Location / URL |
| :---- | :--- | :--- | :--- |
| Webserver | sadm-oyn <br> sadm-ybt | root | localhost |
| Mailserver | sadm-oyn <br> sadm-ybt | root | localhost |
| WordPress | sadm-oyn@localhost <br> sadm-ybt@localhost | Administrator | https://njeritech.ch |

### Erstellen root User Web-/ Mailserver

Der Benutzername besteht immer aus dem ersten Buchstaben des Vor- und Nachnamens und der letzte Buchstabe vom Nachnamen. Hier ein Beispiel: Hans Peter = hpr.

**Beispiel:**
| Name | Vorname | Berechtigungslevel | Benutzername |
| :---- | :--- | :--- | :--- |
| Peter | Hans | System Administrator | sadm-hpr |
| Müller | Thomas | Benutzer | mts |