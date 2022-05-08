# Testing

## Inhaltsverszeichnis
- [Testing](#testing)
  - [Inhaltsverszeichnis](#inhaltsverszeichnis)
    - [Testing Webserver](#testing-webserver)
      - [Apache Perfomancetest](#apache-perfomancetest)
    - [Testing WordPress](#testing-wordpress)
    - [Testing-Mailserver](#testing-mailserver)


### Testing Webserver 

#### Apache Perfomancetest
Beim Apache2 Webserver hat man die Möglichkeit die Auslastungskapazitäten mit ApacheBench zu testen. Dies macht man wie folgt:

```
apt-get update

apt-get install -y apache2-utils


ab -c 50 -n 50 https://njeritech.ch/
```
Danach wird die Performance unseres Webservers angezeigt. Wie man sieht hat unser Webserver zwischen 576ms und 938ms Verzögerung. Das Ziel in Zukunft wäre diese Verzögerung niedriger zu halten. 

![Performancetest](images/Performancetest.PNG)


### Testing WordPress


### Testing-Mailserver
| Testbeschreibung | Tester | Teststatus | Testbeweis |
| :---- | :--- | :--- | :--- |
| Mailserver versendet eine E-Mail and den angegebenen Empfänger und diese ist im Postausgang |  Yanis Blust | E-Mail ist im Postausgang |
| Die versendete E-Mail kommt bei dem angegebenen Empfänger an | Yanis Blust | E-Mail ist im Posteingang | 


