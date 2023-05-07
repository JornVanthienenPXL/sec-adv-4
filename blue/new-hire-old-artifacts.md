# New Hire Old Artifacts

This document describes the elaboration of the 'New Hire Old Artifacts' assignment

## Table of contents

-   [Vraag 1](#vraag-1)
-   [Vraag 2](#vraag-2)
-   [Vraag 3](#vraag-3)
-   [Vraag 4](#vraag-4)
-   [Vraag 5](#vraag-5)


## Vraag 1

Voor vraag 1 hebben we dan in de zoekbalk gezocht op Web Browser Password Viewer en de tijd ingesteld op all time. In de logs zien we dan het pad staan naar het bestand 1111.exe. 

```
C:\Users\FINANC~1\AppData\Local\Temp\11111.exe
```


## Vraag 2

Ook de bedrijfsnaam vinden we terug in dezelfde logs.

```
NirSoft
```


## Vraag 3

Als eerste hebben we gezocht op het pad van de '1111.exe' met de pc naam in = Finance01.(C:\Users\Finance01\AppData\Local\Temp\). Hier hebben we de filter images ingesteld (via intresting fields) en zien we de meest voorkomende images in deze folder. Hierin zien we dat voor 82% van de logs IonicLarge.exe is gebruikt. We hebben dan gezocht op IonicLarge.exe. Dan hebben we bij meer fields original file name aangzet. zo hebben we de originele naam van dit bestand bekregen. = PalitExplorer.exe

```
PalitExplorer.exe, IonicLarge.exe
```

![image 1](./images/image_2.PNG)

![image 2](./images/image_1.PNG)


## Vraag 4

Ook voor deze vraag hebben we gezocht op IonicLarge.exe. Bij intresting fields hebben we dan gezocht op filter destination ip. In de vraag staat dat er 2 connecties waren. bij 1 van de ip adressen zien we dan dat er 2 connecties zijn. Dit is dus het ip adress dat we zoeken.

```
2[.]56[.]59[.]42
```

![image 3](./images/image_3.PNG)


## Vraag 5

We hebben gezocht op IonicLarge.exe. In een log hebben we gevonden dat er een targetobject parameter is. Hierop hebben we dan gezocht en zo zijn we op het pad gekomen waar de key is aangepast.

```
HKLM\SOFTWARE\Policies\Microsoft\Windows Defender\
```


## Vraag 6

We hebben via de hint in tryHackMe gezocht in Splunk op de term "taskkill /im". In de log staat dan parent command line en hier zie je dat de kill wordt uitgevoerd. Dan hebben we in intresting fields gefilterd op commandline. Nu zien we de 2 commando's staan van de programma's die ze hebben gekiled.

```
WvmIOrcfsuILdX6SNwIRmGOJ.exe,phcIAmLJMAIMSa9j9MpgJo1m.exe
```

![image 4](./images/image_4.PNG)


## Vraag 7

We hebben gefilterd op 'PowerShell Defender' daarna hebben we gezocht naar de meest recente datum.

![image 5](./images/image_5.PNG)

Dan binnen de Event zie je dat er een bepaalde commando wordt uitgevoerd via powershell namelijk: 'powershell  WMIC /NAMESPACE:\root\Microsoft\Windows\Defender PATH MSFT_MpPreference call Add ThreatIDDefaultAction_Ids=2147737394 ThreatIDDefaultAction_Actions=6 Force=True'.


## Vraag 8

Binnen dezelfde event zie je ook 4 verschillende ID's dat gezet worden door de aanvaller.

![image 6](./images/image_6.png)


## Vraag 9

Voor deze vraag hebben we gefilterd op 'AppData' en de datum gezet op All Time zo zie je namelijk het pad van malicious binary.

![image 7](./images/image_7.png)


## Vraag 10

Nu gebaseerd op de vorige antwoord moet je voor deze vraag een field geselecteerd namelijk: 'ImageLoaded'. Zo zie je dan de eerste 3 .dll file

![image 8](./images/image_8.png)
