# PS Eclipse

This document describes the elaboration of the 'PS Eclipse' assignment

## Table of contents

-   [Opdracht 1](#opdracht-1)
-   [Opdracht 2](#opdracht-2)
-   [Opdracht 3](#opdracht-3)
-   [Opdracht 4](#opdracht-4)
-   [Opdracht 5](#opdracht-5)
-   [Opdracht 6](#opdracht-6)
-   [Opdracht 7](#opdracht-7)


## Opdracht 1

Door de naam van de lab wist je dat het te maken had met powershell dus als je zoekt naar 'powershell' en je filtert op 'commandline' zie je dat er een van de resultaten een verdachte binary file was.

Antwoord: 'OUTSTANDING_GUTTER.exe'


## Opdracht 2 

Als je kijkt binnen diezelfde commandline output zie je een heel lange base64 encoded string, als je die decode met behulp van een tool like 'cyberchef' kom je op de URL als je daarna die URL defanged krijg je het antwoord.

Antwoord: 'hxxp[://]886e-181-215-214-32[.]ngrok[.]io'


## Opdracht 3

Binnen dezelfde log zie je dat in de commandline powershell.exe wordt gebruikt en binnen de parent image een powershell.exe path is.

Antwoord: 'C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe'

## Opdracht 4

Weer binnen dezelfde log zie je welke commando er wordt uitgevoerd in de commandline.

Antwoord: 'C:\Windows\system32\schtasks.exe" /Create /TN OUTSTANDING_GUTTER.exe /TR C:\Windows\Temp\COUTSTANDING_GUTTER.exe /SC ONEVENT /EC Application /MO *[System/EventID=777] /RU SYSTEM /f'


## Opdracht 5

Als je searched voor 'OUTSTANDING_GUTTER.exe' en je zet je selectedfields op commandline de eerste zoekresultaat zie je bij 'User' welke user gebruikt wordt, Als je binnen de task zelf kijkt zie je dat je de hint krijgt van dat je de 'User' gevolgd door een ';' en wat er wordt uitgevoerd in de commandline.

Antwoord: 'NT AUTHORITY\SYSTEM;"C:\Windows\system32\schtasks.exe" /Run /TN OUTSTANDING_GUTTER.exe'

## Opdracht 6

Als je weer searched voor 'OUTSTANDING_GUTTER.exe' en je zet je filtert deze keer op 'QueryName' zie je een bepaalde URL dan moet je deze nog defangen, maar zoals vermeld in de opdracht zelf moet je er nog 'http://' aan toevoegen.

Antwoord: 'hxxp[://]9030-181-215-214-32[.]ngrok[.]io'

## Opdracht 7

Sinds je naar een powershell script/bestand zoekt, zoek je naar de extensie van powershell namelijk '.ps1' en kom je op het antwoord.

Antwoord: 'script.ps1'

## Opdracht 8

Binnen dezelfde log zie je allemaal hashes, als je de eenderwelke decode kom je op het antwoord.

Antwoord: 'BlackSun.ps1'


## Opdracht 9

Baseerd op het vorig antwoord zoek je naar 'blacksun' als je scrolt door de logs zie je uiteindelijk een log met een .txt bestand.

Antwoord: 'C:\Users\keegan\Downloads\vasg6b0wmw029hd\BlackSun_README.txt'

## Opdracht 10

Als je nu 2 logs naar boven scrolt zie je een image.

Antwoord: 'C:\Users\Public\Pictures\blacksun.jpg'