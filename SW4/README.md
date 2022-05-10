# Protokollierung / Logs

## Inhaltsverszeichnis
- [Protokollierung / Logs](#protokollierung--logs)
  - [Inhaltsverszeichnis](#inhaltsverszeichnis)
    - [Webserver Apache2 (lokal)](#webserver-apache2-lokal)
      - [Ablageort Apache2 logs](#ablageort-apache2-logs)
    - [Mailserver Postfix (TBZ-Cloud)](#mailserver-postfix-tbz-cloud)
      - [Ablageort Postifx Logs](#ablageort-postifx-logs)

### Webserver Apache2 (lokal)
Apache hat folgende Loglevels im Errorlog:

```
Level                   Description

emerg	                System is unusable
alert	                Action must be taken immediately
crit	                Critical conditions
error	                Error conditions
warn	                Warning conditions
notice	                Normal, but significant conditions
info	                Informational messages
debug	                Debugging messages
trace1 – trace8	        Trace messages with gradually increasing levels of detail
```

#### Ablageort Apache2 logs

Unser Apache2 Server protokolliert den Server mit dem Loglevel warn, da wir nicht erst bei einem Error oder höher ein Log haben möchten. Die Logfiles werden unter dem Pfad ``/var/log/apache2/error.log`` abgespeichert.

### Mailserver Postfix (TBZ-Cloud)

Unser Mailserver welcher auf der TBZ-Cloud gehostet wird, erstellt automatisch logs. In diesem Logfile wird der durchgang der versendeten Mails Protokoliert. Diese kann man im folgenden file finden.
```
cat /var/log/mail.log
```

<br>Zudem gibt es noch den syslog. In diesem Logfile werden sämtliche befehle geloggt.
```
cat /var/log/syslog
```

#### Ablageort Postifx Logs
