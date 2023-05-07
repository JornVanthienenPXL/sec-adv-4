# Sakura Room

This document describes the elaboration of the 'Sakura Room' assignment

## Table of contents

-   [Username uit afbeelding halen](#username-uit-afbeelding-halen)
-   [Volledige naam en email-adres van attacker zoeken](#volledige-naam-en-email-adres-van-attacker-zoeken)
-   [Cryptocurrency vinden](#cryptocurrency-vinden)
-   [Twitter handle en WiFi SSID and BSSID vinden](#twitter-handle-en-wifi-ssid-and-bssid-vinden)
-   [Locatie luchthavens + naam meer + geboorteplaats zoeken](#locatie-luchthavens--naam-meer--geboorteplaats-zoeken)


## Username uit afbeelding halen

Bij het openen van de link van de afbeelding was te zien dat het ging om een afbeelding van het '.svg' formaat. Dit betekent dat dit een mark-up language is over hoe een afbeelding opgesteld is. We hebben dit geopend in notepad en hier was hetvolgende in te vinden:

```xml
   ...
   sodipodi:docname="pwnedletter.svg"
   inkscape:export-filename="/home/SakuraSnowAngelAiko/Desktop/pwnedletter.png"
   inkscape:export-xdpi="96"
   ...
```

Zijn username is dus: SakuraSnowAngelAiko


## Volledige naam en email-adres van attacker zoeken

We hebben gezocht op zijn username en kwamen als eerste op zijn Twitter account uit. Hierop stond zijn naam als 'Aiko'. als we dan wat verder scrollen kwamen we zijn volledige naam uit.

![Twitter post](sakura-room/image-1.png)

Zijn volledige naam: 'Aiko Abe'

Om zijn e-mail te vinden zijn we gaan kijken in zijn GitHub repositories, hier viel ons op dat hij veel met crypto miners bezig is en vooral met 'XMR' wat Monero is. Er is ook een repository wat 'PGP' noemde. In deze repository is een public PGP key te vinden. Bij PGP zit altijd een user field. Dan hebben we een PGP decoder opgezocht en deze public GPG key als input gegeven en hier kwam het e-mailadres uit.

![PGP key decoding](sakura-room/image-2.png)

Zijn e-mailadres: 'SakuraSnowAngel83@protonmail.com'


## Cryptocurrency vinden

Op zijn GitHub account was een repository te vinden wat 'miningscript' noemt en hier was hetvolgende te vinden in de file 'miningscript'

```
stratum://ethwallet.workerid:password@miningpool:port
```

Hieruit kunnen we afleiden dat hij een Ethereum wallet heeft.

Cryptocurrency wallet: 'Ethereum'

Om het cryptocurrency wallet address te vinden keken we naar zijn vorige commits en was het al snel duidelijk dat hij eerst zijn echte gegevens had gepushed maar kort erna dit had verbeterd naar dummy waarden. Maar zijn echte gegevens zijn wel nog terug te vinden in zijn vorige commit.

Cryptocurrency wallet address: '0xa102397dbeeBeFD8cD2F73A89122fCdB53abB6ef.Aiko'

Mining Pool: 'ethermine'

Om de andere cryptocurrency te vinden hebben we zijn wallet address opgezocht en gekeken naar de transacties. Hier kwam al snel uit dat hij ook met Tether bezig is geweest.

Andere cryptocurrency: 'Tether'

![Cryptocurrency wallet transacties](sakura-room/image-3.png)


## Twitter handle en WiFi SSID and BSSID vinden

Zijn Twitter handle hadden we al gevonden bij het vinden van zijn Twitter account.

Twitter handle: '@SakuraLoverAiko'

We hebben een lange tijd gezocht via Brave browser op het Tor netwerk, maar we vonden niks. Dan hebben we gebruik gemaakt van de hint en toen zagen we dat het ging over een service genaamd 'DeepPaste V3' wat een pastebin is op het darkweb. Dan hebben we een random paste geopend en de MD5 vervangen in de URL bar met de MD5 die op zijn Twitter account staat.

![DeepPaste V3](sakura-room/image-4.png)

URL WiFi SSIDS: 'http://deepv2w7p33xa4pwxzwi2ps4j62gfxpyp44ezjbmpttxz3owlsp4ljid.onion/show.php?md5=b2b37b3c106eb3f86e2340a3050968e2'

Uit de vorige pastebin konden we zijn SSID halen van zijn Home WiFi. Dit hebben we opgezocht op de website 'wigle.net' en met de informatie van zijn Twitter over Tokyo, zijn we ook in Japan gaan zoeken en kwamen we uit op zijn BSSID

BSSID: '84:af:ec:34:fc:f8'

![BSSID](sakura-room/image-5.png)


## Locatie luchthavens + naam meer + geboorteplaats zoeken

Op zijn Twitter staat een foto met als omschrijving 'Checking out some last minute cherry blossoms before heading home!'. Op deze foto kan je in de verte een 'White Obelisk' zien. Dit hebben we op Google opgezocht en kwamen we uit in Washington US en hier het dichtsbijzijnde airport genomen 'Ronald Reagan Washington National Airport. Dan hebben we de code opgezocht van deze luchthaven en deze is 'DCA'.

Luchthaven code: 'DCA'

Om de 'last layover airport' te vinden hebben we opnieuw een post van Twitter gevonden met als omschrijving 'My final layover, time to relax!'. Op deze foto was hetvolgende te zien 'First Class Lounge Sakura Lounge'. Dit hebben we opgezocht met het woord airport en kwamen we uit op de luchthaven 'Haneda Airport' 'HND'.

Luchthaven layover code: 'HND'

Om de naam van het meer te vinden, hebben we de foto op zijn Twitter gedownload en opgezocht via Google Images. Hier kwamen we uit op Japan en keken we naar de map van Japan en zochten we naar het meer. Het was vrij snel duidelijk dat dit het meer was.

Japan meer: 'Lake Inawashiro'

Om zijn geboorteplaats te vinden hebben we de naam van de stad genomen die bij het Wi-Fi SSID hoorde en dit is 'Hirosaki'

Geboorteplaats: 'Hirosaki'