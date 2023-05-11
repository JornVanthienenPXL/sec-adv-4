# ItsyBitsy

This document describes the elaboration of the 'ItsyBitsy' assignment

## Table of contents

-   [Opdracht 1](#opdracht-1)
-   [Opdracht 2](#opdracht-2)
-   [Opdracht 3](#opdracht-3)
-   [Opdracht 4](#opdracht-4)
-   [Opdracht 5](#opdracht-5)
-   [Opdracht 6](#opdracht-6)
-   [Opdracht 7](#opdracht-7)


## Opdracht 1

Je surft naar het IP adress van de Kibana webserver, daarna ga je naar "Discover" je ziet daar de "connection_logs" file waar je query's op kunt uitvoeren dat je door de file filtert en informatie eruit kunt halen, wij hebben de datum Maart 2022 gepakt waar we uitkwamen op '1482' events.

Antwoord: '1482'


## Opdracht 2 

Als je kijkt naar de Source IP zie je dat er 2 IP's zijn die de traffic veroorzaken, namelijk 192.166.65.52 en '192.166.65.54', de tweede IP address heeft maar 0.4 % traffic dus als je dan gaat kijken naar zijn destination IP address zie je dat die 2 keer naar deze IP address gaat, namelijk 104.23.99.190 als we die destination IP address gaan opzoeken op een threat intelligence resource 

Antwoord: '192.166.65.54'


## Opdracht 3

Bij de andere connections zie je dat de user-agent soms "Mozilla/5.0" was maar bij de source IP van 192.166.65.54 was deze "bitsadmin" na een google search van bitsadmin zie je dat het een CLI tool is dat wordt gebruikt om jobs te maken, downloaden of uploaden en om de voortgang ervan te volgen.

Antwoord: 'bitsadmin'


## Opdracht 4 

Als je kijkt naar de host van 192.166.65.54 zie je dat die verbonden is met een bekende filesharing site namelijk pastebin.com

Antwoord: 'pastebin.com'


## Opdracht 5

Als je nu kijkt naar de uri kun je de volledige url samen pasten en als je surft naar die site vind je een secret file met daarin de flag.

Antwoord: 'pastebin.com/yTg0Ah6a'


## Opdracht 6 

Als je surft naar pastebin.com/yTg0Ah6a zie je dat de filename secret.txt

Antwoord: 'secret.txt'

## Opdracht 7

In de file secret.txt zie je de flag: THM{SECRET__CODE}

Antwoord: 'THM{SECRET__CODE}'