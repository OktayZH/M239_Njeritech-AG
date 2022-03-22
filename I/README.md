# Know-How & Begriffe

## Inhaltsverszeichnis
- [Know-How & Begriffe](#know-how--begriffe)
  - [Inhaltsverszeichnis](#inhaltsverszeichnis)
    - [Webserver](#webserver)
    - [Domain Name System](#domain-name-system)
    - [Information fremder Server](#information-fremder-server)
    - [Proxy](#proxy)
    - [DMZ](#dmz)
    - [Weitere-Kapitel](#weitere-kapitel)

### Webserver

**Wie kann derselbe Webserver unterschiedliche Websites hosten (Virtual Hosts)?**
Durch Virtual Hosting kann man mehrere Websites hosten, da die Webserver auf einer gemeinsamen Hardware konfiguriert und installiert sind. Jeder dieser Webserver kann individuell konfiguriert werden. Dadurch, dass die Webserver individuell konfiguriert werden können, kann man auch unterschiedliche Internetdienste anbieten. Zum Beispiel kann eine API Schnittstelle installiert werden, um mit einem externen System zu interagieren.

Es gibt jeweils zwei Arten von Virtual Hosting: 

Eins davon ist das ***IP-basierte Virtual Hosting***. Die virtuellen Server erhalten eine oder mehrere unabhängige IP-Adressen. Somit ist aus der Sicht eines Clients die virtuellen Maschinen unabhängig voneinander.

Die andere Methode ist das ***Namensbasierte Virtual Hosting***. Dadurch kann man verschiedene Domains einem virtuellen Server zuordnen. Auf der Anwendungsebene wird die Domain dem passenden Dienst zugewiesen. Dadurch werden weniger IP-Adressen benötigt.


### Domain Name System

**Wie funktioniert DNS?**
Das DNS-System funktioniert ähnlich wie ein Telefonbuc. Es verwaltet die Zuweisung zwischen Namen und Nummern. DNS-Server übersetzen Namensanforderungen in IP-Adressen oder auch umgekehrt. Dabei steuern Sie welchen Server ein Endbenutzer erreicht, wenn er in seinen Webbrowser einen Domänen-Namen eingibt.

**Welche "Ressource Record" -Typen gibt es? Wozu dienen Sie?**
Um eine Namensauflösung durchzuführen, muss in den Datenbanken der DNS- bzw. Nameserver nach DNS-Einträgen gesucht werden, den sogenannten DNS-Records oder Resource Records. Hier ist jeder (dem Server bekannten) IP-Adresse ein Domain-Name zugeordnet.

Hier eine Aufzählung der wichtigsten DNS Records:

- A (Host address)
- AAAA (IPv6 host address)
- ALIAS (Auto resolved alias)
- CNAME (Canonical name for an alias)
- MX (Mail eXchange)
- NS (Name Server)
- PTR (Pointer)
- SRV (location of service)

Resource Records sind nach einem einfachen System aufgebaut und in ASCII kodiert. Für jeden DNS-Record existiert eine eigene Zeile. 
Die Einträge folgen in der Regel folgendem Format:

    <name> <ttl> <class> <type> <rdlength> <radata>

- name: Der Name der Domain ist das, was der Nutzer z. B. in seinen Browser eingibt.
- ttl: TTL steht für „Time to live“ und bezeichnet die Zeit (in Sekunden), die ein Eintrag im Cache zwischengespeichert werden darf. Nach Ablauf der Zeit kann nicht sichergestellt werden, dass der Resource Record noch aktuell ist. Die Angabe ist optional.
- class: Theoretisch gibt es verschiedene Klassen für DNS-Records, praktisch beziehen die Einträge sich aber immer auf das Internet (als IN gekennzeichnet), weshalb auch diese Angabe optional ist.
- type: In einer Zonendatei kommen verschiedene Typen von Resource Records vor (mehr dazu s. u.).
- rdlength: Dieses optionale Feld gibt an, welchen Umfang das anschließende Datenfeld hat.
- rdata: Resource Data sind die Informationen, nach denen man den Namen der Domain auflösen möchte, beispielsweise die IP-Adresse.

Bei einer DNS-Anfrage kann nach drei verschiedenen Verfahren beantwortet werden.

- Autoritativ 
()

- Rekursiv
()

- Iterativ 
(Eine iterative DNS-Query ist eine Anfrage nach einem Webseitennamen oder einem Uniform Resource Locator (URL), auf die der DNS-Server (Domain Name System) mit der IP-Adresse aus seinem Zonendatei-Cache antwortet, sofern möglich. Wenn der Server nicht über die angeforderte IP-Adresse verfügt, leitet er die Anfrage an einen anderen DNS-Server weiter. Iterative DNS-Anfragen werden auch als nicht-rekursive DNS-Anfragen bezeichnet.)

### Information fremder Server

**Wie können Angaben über einen beliebigen fremden Server herausgefunden werden?**
In der Welt der Informatik gibt es zu viele Möglichkeiten

### Proxy
**Was ist ein Proxy?**
Text

**Welche Funktionen übernimmt er?**
Text

### DMZ
**Was ist eine DMZ?**
Text

**Wozu dient sie?**
Text

### Weitere-Kapitel 
Text