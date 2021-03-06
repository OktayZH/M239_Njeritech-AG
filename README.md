# Einleitung Modul 239
Internetserver mit verschiedenen Diensten konfigurieren und in Betrieb nehmen und dabei Sicherheitsvorgaben und betriebliche Anforderungen beachten.

## Inhaltsverszeichnis

- [Einleitung Modul 239](#einleitung-modul-239)
  - [Inhaltsverszeichnis](#inhaltsverszeichnis)
  - [A: Anforderungen](#a-anforderungen)
  - [I: Know-How & Begriffe](#i-know-how--begriffe)
  - [V: Vorgaben (Security / Service Operation)](#v-vorgaben-security--service-operation)
  - [SW1: Webserver installieren/konfigurieren](#sw1-webserver-installierenkonfigurieren)
  - [SW2: Mailserver installieren/konfigurieren](#sw2-mailserver-installierenkonfigurieren)
  - [SW3: Weiterer Serverdienst installieren/konfigurieren](#sw3-weiterer-serverdienst-installierenkonfigurieren)
  - [SW4: Protokollierung](#sw4-protokollierung)
  - [B1: Benutzerkonzept & -Umsetzung](#b1-benutzerkonzept---umsetzung)
  - [B2: Zertifikate](#b2-zertifikate)
  - [T: Testing](#t-testing)
  - [Lizenzierung](#lizenzierung)


## [A: Anforderungen](A/README.md)
 **1. Vorstellung unserer Firma**
 
 Njeritech ist unsere Firma, welche in Zukunft im Bereich der Hardware sich fokussieren wird. Wir wollen uns im Bereich des Hardware Handel und Verkauf neu etablieren. Wir wollen stets unseren Kunden einen fairen Preis bieten.

**2. Welche Art von Hosting macht in unserem Fall am meisten Sinn?**

Wir haben uns für die Cloudlösung entschieden, da diese in unserem Fall am meisten Sinn macht. Der wichtigste Grund dafür ist die Skalierbarkeit von der Cloud. Zudem fallen die Arbeitskosten für das Betreiben der Hardware weg. Detailliertere angaben dazu finden Sie im Abschnitt "A".



## [I: Know-How & Begriffe](I/README.md)

- [Webserver](I/README.md/#Webserver)
- [Domain Name System](I/README.md/#Domain_Name_System)
- [Informationen fremder Server](I/README.md/#Informationen_fremder_Server)
- [Proxy](I/README.md/#Proxy)
- [DMZ](I/README.md/#DMZ)

## [V: Vorgaben (Security / Service Operation)](V/README.md)

- [Soll-Zustand](V/README.md/#Soll-Zustand)
- [Mailserver](V/README.md/#Mailserver)
- [Webserver](V/README.md/#Webserver)
- [CMS](V/README.md/#CMS)
- [Vefügbarkeit](V/README.md/#Verfügbarkeit)
- [Externer Zugriff](V/README.md/#Externer_Zugriff)
- [Gefahren und Risiken](V/README.md/#Gefahren_und_Risiken)
- [Backupkonzept](V/README.md/#Backupkonzept)

## [SW1: Webserver installieren/konfigurieren](SW1/README.md)

- [Webserver aufsetzen](V/README.md/#Webserver_aufsetzen)
- [Webserver Erreichbarkeit konfigurieren](I/README.md/#Webserver_Erreichbarkeit_konfigurieren)

## [SW2: Mailserver installieren/konfigurieren](SW2/README.md)

- [Voraussetzungen](SW2/README.md/#Voraussetzungen)
- [Installation Postfix](SW2/README.md/#Installation_Postfix)
- [Postfix konfigurieren](SW2/README.md/#Postfix_konfigurieren)
- [Kontrolle](SW2/README.md/#Kontrolle)

## [SW3: Weiterer Serverdienst installieren/konfigurieren](SW3/README.md)

- [Erste CMS Ambindung mit Shopify](SW3/README.md/#Erste_CMS_Anbindung_mit_Shopify)
- [Zweite CMS Anbindung mit WordPress](SW3/README.md/#Zweite_CMS_Anbindung_mit_WordPress)
- [Testing ob WordPress Anpassungen auf dem Webserver erfolgen](SW3/README.md/#Testing_ob_WordPress_Anpassungen_auf_dem_Webserver_erfolgen:)

## [SW4: Protokollierung](SW4/README.md)

- [Webserver Apache2 (lokal)](SW4/README.md/#Webserver_Apache2_(lokal))
- [Ablageort Apache2 logs](SW4/README.md/#Webserver_Apache2_(lokal)/#Ablageort_Apache2_logs)
- [Mailserver Postfix (TBZ-Cloud)](SW4/README.md/#) 
- [Ablageort Postifx Logs](SW4/README.md/#Mailserver_Postfix_(TBZ-Cloud)/#Ablageort_Postfix_Logs)   

## [B1: Benutzerkonzept & -Umsetzung](B1/README.md)

- [Administratormatrix](B1/README.md/#Administratormatrix)
- [Namensgebung Konten](B1/README.md/#Namensgebung_Konten)
- [Persönliche Administratorenmatrix](B1/README.md/#Persönliche_Administratorenmatrix)
- [Erstellen root User Web-/ Mailserver](B1/README.md/#Erstellen_root_User_Web-/_Mailserver)
- [Erstellen Administrator WordPress](B1/README.md/#Erstellen_Administrator_WordPress)
 
## [B2: Zertifikate](B2/README.md)

- [Domäne njeritech.ch](B2/README.md/#Domäne_njeritech.ch)
- [Apache konfigurieren](B2/README.md/#Apache_konfigurieren)
- [SSL-Zertifikat erstellen](B2/README.md/#SSL-Zertifikat_erstellen_mit_CertBot)
- [Hostpoint Konfiguration](B2/README.md/#Hostpoint_Konfiguration)
- [Testing](B2/README.md/#Testing)

## [T: Testing](T/README.md)

- [Testing Webserver](T/README.md/#Testing_Webserver)
- [Apache Perfomancetest](T/README.md/#Testing_Webserver/#Apache_Perfomancetest)
- [Security Tests](T/README.md/#Testing_Webserver/#Security_Tests)
- [Testing WordPress](T/README.md/#Testing_WordPress)
- [Testing-Mailserver](T/README.md/#Testing-Mailserver)




## Lizenzierung
- - -
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/ch/"><img alt="Creative Commons Lizenzvertrag" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/ch/88x31.png" /></a><br />Dieses Werk ist lizenziert unter einer <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/ch/">Creative Commons Namensnennung - Nicht-kommerziell - Weitergabe unter gleichen Bedingungen 3.0 Schweiz Lizenz</a>

- - -
