Vul onderstaande aan met de antwoorden op de vragen uit de readme.md file. Wil je de oplossingen file van opmaak voorzien? Gebruik dan [deze link](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) om informatie te krijgen over
opmaak met Markdown.

a)

Om docker te kunnen gebruiken in jenkins moeten we eerst docker installeren. We doen dit aan de hand van volgende commando's:

Hier updaten we onze ubuntu server zodat alles up-to-date is.
![alt text](images/image-10.png)

Hier installeren wij packages die het downloaden van files beveiligd. Dit is handig voor docker images te downloaden.
![alt text](images/image-16.png)

met dit commando voegen we Docker's GNU Privacy Guard key toe aan ons systeem. Dit zorgt ervoor dat de packages die we downloaden van pocker hub autentiek en niet veranderd zijn.
![alt text](images/image-15.png)

Als we dit commando uitvoeren voegen we het officiele docker repository toe.
![alt text](images/image-17.png)

Hier updaten we onog eens alles zodat alles up-to-date is voor de installatie.
![alt text](images/image-10.png)

Nu installeren we de docker community edition, de cli voor de community edition en een containerd.io runtime die docker ondersteunt.
![alt text](images/image-18.png)

Door het volgende commando uit te voeren kunnen we zien dat docker werkt met sudo.
![alt text](images/image-13.png)

Als we deze commando's uitvoeren geven we permissies aan de jenkins gebruiker om docker te gebruiken zonder sudo.                 
![alt text](images/image-9.png)

Hier testen we docker zonder sudo.
![alt text](images/image-2.png)

Deze stappen doen we nog een keer voor de productie server maar dan met de naam ubuntu i.p.v jenkins.

Nu onze servers docker kunnen gebruiken moeten we de docker image op docker hub plaatsen.

Eerst builden we de docker image van de calculator app.
![alt text](images/image.png)

Nu loggen we in op docker hub. Daarna taggen we de image met het docker hub account en pushen we deze vervolgens naar docker hub.
![alt text](images/image-3.png)

Hier is een foto van de docker image op docker hub.
![alt text](images/image-4.png)

Om de dockerfile te kunnen gebruiken moeten wij credentials aanmaken met de gebruikersnaam en het wachtwoord van docker hub zoals in onderstaande foto.
![alt text](images/image-8.png)

Voor de connectie met de production server moeten wij nog eens credentials aanmaken waarbij we de vockey kopieeren en plakken in de Private Key sectie van de credentials.
![alt text](images/image-14.png)

Nu kunnen we beginnen aan de pipeline te schrijven.

b)
