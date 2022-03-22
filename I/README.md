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
(Wenn ein rekursiver Resolver eine Antwort von einem TLD-Nameserver erhält, verweist ihn die Antwort auf einen autoritativen Nameserver. Der autoritative Nameserver ist für gewöhnlich die letzte Station auf der Reise zu einer IP-Adresse. Der autoritative Nameserver enthält Informationen, die dem Domainnamen (z. B. google.com), für den er zuständig ist, eigen sind. Er kann einem rekursiven Resolver die IP-Adresse des Servers, die im DNS-A-Eintrag enthalten ist, liefern.)

- Rekursiv
(Rekursive DNS-Anfragen sind Standardanfragen von Benutzern oder von DNS-Servern, die so konfiguriert sind, dass sie ungelöste IP-Anfragen an einen anderen DNS-Server weiterleiten; auf diese Weise kann der erste Server verfügbar bleiben. Rekursive DNS-Anfragen und rekursive DNS-Server werden verwendet, um einen Teil der enormen Arbeitslast zu verteilen, die mit der Auflösung der Namen von Webseiten in URLs verbunden ist.)

- Iterativ 
(Eine iterative DNS-Query ist eine Anfrage nach einem Webseitennamen oder einem Uniform Resource Locator (URL), auf die der DNS-Server (Domain Name System) mit der IP-Adresse aus seinem Zonendatei-Cache antwortet, sofern möglich. Wenn der Server nicht über die angeforderte IP-Adresse verfügt, leitet er die Anfrage an einen anderen DNS-Server weiter. Iterative DNS-Anfragen werden auch als nicht-rekursive DNS-Anfragen bezeichnet.)

### Information fremder Server

**Wie können Angaben über einen beliebigen fremden Server herausgefunden werden?**
In der Welt der Informatik gibt es zu viele Möglichkeiten um an Informationen eines fremden Servers zu gelangen. Zum Beispiel kann man zuerst versuchen eine Verbindung über eine IP-Adresse aufzubauen. Dann kann man einen Portscan machen und schauen welche Protokolle genutzt werden. Die Beschaffung von Informationen die nicht für die Öffentlichkeit gedacht sind ist jedoch illegal.

Auch könnte man sich z.B. einen Zugriff verschaffen mit DNS Poisoning. Dabei wird ein Zielbenutzer auf eine falsche Website weitergeleitet und wird aufgefordert sich anzumelden. Sobald er dies tut kann man die gesammelten Informationen nutzen, um sich Zugriff auf den fremden Server zu verschaffen.

### Proxy
**Was ist ein Proxy?**
Ein Proxy Server ist eine Relaisstation zwischen einem Client wie Deinem Computer und einem Webserver, von dem Du Daten anfordern willst. Der Proxy Server kann als Programm auf Deinem Gerät realisiert sein oder auch auf einem eigenen Server installiert werden. Das wird besonders dann der Fall sein, wenn der Proxy Server den Datenverkehr für mehrere Clients überwachen soll.

**Welche Funktionen übernimmt er?**
Die Hauptfunktionen eines Proxies sind Verschleiern, Absichern und Beschleunigen von Datenübertragungen.

Eine Anfrage an einen Server wird vom Proxy Server unter Angabe der eigenen IP-Adresse gestellt. Deine IP-Adresse bleibt bei einer solchen Anfrage vor dem Webserver verborgen. Damit kannst Du zum Beispiel Geoblocking umgehen und Webseiten aufrufen, die für Nutzer in Deinem Land gesperrt sind.

Proxy Server haben oft einen Cache, in dem sie die zuletzt geladenen Daten speichern. Werden diese Daten von anderen Clients aufgerufen, können die Anfragen vom Proxy Server selbst beantwortet werden, ohne eine neue Anfrage an den auswärtigen Webserver richten zu müssen. Das spart Bandbreite, Kosten und vor allem Zeit. Ein Proxy kann so auch die Last verteilen und das Überlasten des Internetzugangs durch einen Client verhindern.

Der Proxy Server kann die ankommenden Datenpakete untersuchen und Schadprogramme herausfiltern. Die entsprechenden Regeln lassen sich auf die Erfordernisse Deines Netzwerks individuell anpassen.

### DMZ
**Was ist eine DMZ?**
Text

**Wozu dient sie?**
Text

### Weitere-Kapitel 
Text