# Playwright installation

Deze handleiding is geschreven in - [markdown-it] 

Stappen plan voor het installeren van playwright
1. Node installeren - https://nodejs.org/en/download/
2. NPM installeren - https://radixweb.com/blog/installing-npm-and-nodejs-on-windows-and-mac
3. Git installeren & Git configureren - https://gitforwindows.org/
4. Installatie van playwright
5. Playwright Tips & Tricks


## 1. Node installeren
Bezoek de site: https://nodejs.org/en/download/
Ik koos voor de windows installer aan de linkerzijde. Op het moment van schrijven versie 18.13.0 
Automatische start de download nadat je hierop klikt welke in je downloads folder terecht komt. 
Ik koos bij de eerste installatie voor de traditionele next next etc finish methode. Echter kwam ik er bij stap 2 (NPM installatie) achter dat NPM ook de NPM package manager nodig heeft. 
Kies Daarom voor de npm package manager. Die installeerd ook node.js.

## 2. NPM installeren
Gedurende deze stap kwam ik er de eerste keer achter dat ik bij de Node.js installatie ipv next next finish ook de package manager had moeten selecteren.
Kortom, als je de npm package manager bij stap 1 geinstalleerd hebt. Ben je in 1x klaar. Bedankt Egstorf voor deze omweg de eerste keer! ^^

Wat we nog wel even doen zoals de site aangeeft - https://radixweb.com/blog/installing-npm-and-nodejs-on-windows-and-mac
"Check Node.js and NPM Version"
In mijn geval:
C:\>node -v
v18.13.0
C:\>npm -v
8.19.3

`Blijkbaar is de versie 16.18 de LTS (long term support) versie, mogelijk moeten we terug naar die versie. To be continued....`

## 3. Git installeren & Git configureren
We bezoek eerst even https://gitforwindows.org/ en daar druk ik op de grote blauwe download knop.
Op het moment van schrijven komt er een Git-2.39.1-64-bit.exe in mijn download folder terecht welke ik open.
Bij de installatie vraagt men welke editor je wilt gebruiken. Kevin E. the allmighty in all his wisdom geeft aan te kiezen voor "Visual Studio Code as Git's default editor". Deze voor nu alleen selecteren en dan door met de installatie. 

`Mocht je deze optie niet kunnen selecteren om door te gaan met de installatie, voer dan eerst 3.1 uit en probeer de installatie dan nog een keer`

##### 3.1. Installeer visual studio 
Klik vanuit het installatie process van Git op de blauwe tekst Visual studio code. Dit opent de website https://code.visualstudio.com/ of bezoek de website
Download VSCode voor windows. Deze zal ook in je downloads folder terecht komen.
Next next finish maar aan het einde deselecteer ik het opstarten van visual studio.

#### 3.2 Hervat de Git installatie
Indien de git installatie nog niet was afgesloten, sluit deze dan af. 
Mocht je "Visual Studio Code as Git's default editor" niet kunnen selecteren bij stap 3. Dan zou dit nu wel mogelijk moeten zijn. Deze jongen gaat weer voor de next next, Deselecteer "see release notes", finish methodiek. 

#### 3.3. Git configureren
Open de command prompt
En voer de volgende dingen uit:
- Set the username 
`git config --global user.name "user_name"`
B.v. git config --global user.name "Pietje_Puk"
- Set the user email
`git config --global user.email "user_email"`
B.v. git config --global user.name "Pietje_Puk@Pannenkoekenboot.eu"
- Set automatic command line coloring
`git config --global color.ui auto`
Je krijgt geen conformatie of het gelukt is of niet als je het bovenstaande uitvoert. Dus vertrouw erop dat het goed is gegaan ;) 

## 4. Installatie van playwright
He he we zijn eindelijk aangekomen bij de installatie van playwright.

Bepaal voor jezelf waar je playwright wilt installeren. Ik heb er zelf voor gekozen om een folder genaamd Playwright aan te maken op mijn c:schijf, user, documents\Playwright

Open opnieuw de command prompt
Ga naar je Playwright folder en voer dan de volgende code uit
'npm init playwright@latest'
Er worden een aantal vragen gesteld tijdens de installatie
Need to install the following packages:
  create-playwright@1.17.125
Ok to proceed? (y) `y`

? Do you want to use TypeScript or JavaScript? ...
> TypeScript
  JavaScript
`y en druk op enter`

Where to put your end-to-end tests? » tests
`Druk op enter`

 Add a GitHub Actions workflow? (y/N) » false
 `n`

 Install Playwright browsers (can be done manually via 'npx playwright install')? (Y/n) » true
 `Druk op enter`

Hierna begint het downloaden en installeren

Om te controleren of het werkt voeren het volgende uit
`npx playwright test`

Als het goed is krijg je dan dit te zien:
Running 6 tests using 4 workers
  6 passed (20.9s)
To open last HTML report run:
  npx playwright show-report
  
  
## 5. Playwright Tips & Tricks 
- Gebruik // om comments toe te voegen in je script
- In playwright.config.ts kunnen je browsers of device emulatie aan/uit schakelen
- Maak gebruik van de "Record new" functie om een script op te nemen
- Maak gebruik van de "Record at cursor" om b.v. gemakkelijk controle punten in te bouwen
- 





