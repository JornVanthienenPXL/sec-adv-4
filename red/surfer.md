# Surfer

This document describes the elaboration of the 'Surfer' assignment

## Table of contents

-   [Title 1](#Title-1)
-   ...


## Title 1

Eerste gepinged naar het gekrgen ip om te zien of deze beschikbaar was. 

Daarna een nmap uitgevoerd om te kijken welke poorten open stonden. Dit waren poort 22 en 80. Dit wilt zeggen dat er een webserver op dit ip gehost word en er een open ssh connectie staat.

Hierna hebben we gesurfd naar de website en kwamen we uit op een login pagina. Hier hebben dan gekeken of de robots.txt path verbergd was wat niet het geval was. 

Hierin zagen we een pad genaamd /backup/chat.txt. Door naar dit pad te surfen ip/backup/chat.txt. Zagen we een chat log met katie en de admin en hier werd in gemeld dat de admin moest stoppen met het gebruiken van naam als wachtwoord. Er werd ook vermeld dat er een export2pdf server geinstalleerd was en deze voorlopig alleen een flag weergeeft. Dus dit kan een mogelijke exploit zijn.

Daarna hebben we gekeken of de admin wel degelijk zijn login veranderd had maar dat was niet het geval. Dus hebben we zo kunnen inloggen op de webiste met admin admin. 
Na het bestuderen van de website zagen we verschillende dingen zoals de export to pdf optie, een link naar /internal/admin.php als we op deze link klikten kregen we het bericht "....".

Eerste hebben we gezocht naar exploits doormiddel van php of request te veranderen kwamen we op burpsuite uit. Door burpsuite te gebruiken konden we de request onderscheppen die de webserver naar de export2pdf server deed en konden we de request veranderen et burpsuite naar het pad /internal/admin.php. Door daarna op forward te klikken en het process te doorlopen krijgen we de /internal/admin.php export2pdf terug op onze website en zagen we hier de flag op staan.

via burp de request aangepast en dat de url '%2Finternal%2admin.php'

flag{6255c55660e292cf0116c053c9937810}
