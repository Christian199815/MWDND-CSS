# CSS To The Rescue

Een vierweekse duik in de kracht van moderne CSS zonder JavaScript.

## Week 1: Ideegeneratie & Eerste Experimenten

Deze week lag de focus op het bedenken van een concept en het uitvoeren van de eerste CSS-experimenten:

- Gekeken naar welke methoden in Css ik al bezit om op los te gaan.
- De drie verschillende opdrachten doorgenomen.
- Opzetten van de basisstructuur met semantische HTML
- Eerste experiment met masking

### Resultaten
- Gekozen concept: Ik ga een interface van een crane operator maken. Hoistin' Hank heeft een hijskraan, en de user kan ondervinden hoe het is om een dag op een kraan te werken.
- Eerste prototype met verschillende vlakken wat als achtergrond kan gaan fungeren

### Afbeeldingen Week 1

<figure>
      <img src="/doc-images/idee.JPG" style="width: 25em; aspect-ratio: 1/1;">
      <figcaption>Schets ontwerp</figcaption>
</figure>

<figure>
      <img src="/doc-images/opdrachten.JPG" style="width: 25em; aspect-ratio: 1/1;">
      <figcaption>Opdrachten onderzoek</figcaption>
</figure>

<figure>
      <img src="/doc-images/result-wk1.png" style="width: 25em; aspect-ratio: 1/1;">
      <figcaption>Resultaat week 1</figcaption>
</figure>


<hr>

## Week 2: De stad & eerste interface

Na vorgie week bezig te gaan met het initieren van het idee en al een beetje op zoek te gaan naar de verschillende onderdelen. Ben ik deze week verder gegaan om te kijken naar hoe ik deze onderdelen het beste kan uitwerken.

De onderdelen zijn als volgt:

- De stad, dit zijn de gebouwen waar de hijskraan tussen staat.
- De behuizing van de kraan machinist.
- De bedieningsknoppen van de kraanmachinist.
- (evt. de kraan arm om te simuleren dat we een hijskraan zijn)

In eerste instantie was ik van plan om mijn gebouwen te gaan maken zoals in het eerste experiment van vorige week te zien is. doormiddel van verschillende vierkanten die ik doormiddel van clip-path een vorm gaf om zo het gevoel van een gebouw te maken. Na een indruk wekkend gesprek samen met <a href="https://github.com/shooft">Sanne 't Hooft</a> ben ik erachter gekomen dat er veel meer mogelijk is in css als we het hebben over 3D. Doormiddel van een aantal slimme commando's, heb ik zomaar een doos weten te maken.

### De doos
Een doos bestaat net als een normale doos uit zes vlakken. deze vlakken hebben een zoals een vierkant elk een breedte en hoogte. Doormiddel van custom properties in css is het mogelijk om heel gemakkelijk op te slaan wat de hoogte, breedte en diepte van de doos zullen zijn.

<a href="https://codepen.io/Christian199815/pen/QwWdyQv">
<img src="/doc-images/box1.png" style="width: 25em; aspect-ratio: 1/1;">
</a>

### De joystick
Ik ben deze week ook al van start gegaan met een eerste idee voor de interface, voor het bedienings paneel is het plan om een aantal knoppen te hebben. Maar op het bedienings paneel wil ik ook een soort joysticks gebruiken waar de gebruiker de kraan mee kan bedienen. Voor de bediening heb ik gebruik gemaakt van 8 vlakken die ik van elkaar af heb gemaakt doormiddel van verschillende border radius instellingen. Om te visualiseren dat de joystick werkt heb ik een vierkant op het scherm dat beweegt naar aanleiding waar de gebruiker op de vlakken beweegt. De joystick is een cirkel die ik animeer in de richting van het vlak waar de gebruiker over heen beweegt.

<a href="https://codepen.io/Christian199815/pen/YPzZpeq">
<img src="/doc-images/joystick.png" style="width: 25em; aspect-ratio: 1/1;">
</a>

### De stad
Voor de stad ben ik begonnen met het verder ontwikkelen van de doos die ik in eerste instantie had gemaakt. In de tweede iteratie slag ben ik gaan kijken hoe ik ervoor kan zorgen dat ik de doos altijd van hoogte kan laten veranderen zodat ik het gevoel van verschillende gebouwen met verschillende hoogtes kan wekken. Hiervoor ben ik erachter gekomen dat wanneer ik de alle vlakken behalve het bovenste vlak aan de 'bottom' als transform-origin zet, deze als een soort ankers blijven zitten. Nadat het me was gelukt om de gebouwen vast te zetten kwam het moment dat ik een plane maakte waar deze gebouwen op zouden komen te staan. Doormiddel van display:grid maak ik een raster waar ik alle blokken op vast kan zetten. Waar ik tegen aan liep was dat ik de <code>transform-behaviour: 3d-perspective</code> ook op deze plane moest zetten om de gebouwen in de hoogte te kunnen zien. Uiteindelijk lukte het me om de gebouwen aan de raster te koppelen, echter wilde de gebouwen niet de gehele grootte van het grid vlak aan nemen. De oplossing was elk gebouw in een eigen container stoppen en in deze containers de custom properties voor de breedte en diepte vast zetten zoals deze uit het raster komen.

<a href="https://christian199815.github.io/MWDND-CSS/city.html">
<img src="/doc-images/city.png" style="width: 25em; aspect-ratio: 1/1;">
</a>

## Feedback deze week
empty

<hr>

## Week 3: Stad animaties, Cabine avontuur & 3d interface

Na weer een productieve week ben ik een stuk meer opgeschoten met het bouwen van mijn hijskraan experience. Vorige week was ik al weer een stuk opgeschoten met het realiseren van mijn stad. Daar ben ik deze week weer mee verder gegaan. Ook ben ik van start gegaan met de cabine waar de gebruiker als hijskraan machinist te werk zal gaan. Maar om voor de gebruiker met de wereld te interacteren & natuurlijk ook voor het doel van deze opdracht is er wel een interface nodig. Vorige week heb ik daar al een belangrijke zet mee gedaan om deze te maken, deze was toen nog in 2d.

### De Stad en haar animaties
Deze week begon met een stad die niet op zn plek stond, gebouwen die soms wel te zien waren en soms niet en een perspectief waar ik niet heel tevreden mee was. Na te hebben gespart met een aantal docenten en medestudenten, kwam ik tot het inzicht dat ik een aantal aanpassingen moest maken om de stad en hijskraan het juiste gevoel te geven. Waarempel lukt het me om de stad dit te geven, om eerlijk te zijn weet ik nog steeds niet helemaal hoe dit komt. Oke ja het heeft te maken met de perspective en hoe de gebouwen staan. Maar de werking erachter ga ik nog achter komen, misschien in dit project anders in de projecten in de toekomst die ik met preserve-3d ga doen. 
Na dat mijn stad er eindelijk goed uit begon te zien, was ik begonnen met het maken van een aantal animaties. Deze animaties zullen in de toekomst bedient gaan worden door de interface. 
Ik begon met een animatie om de hoogte van de stad te veranderen, of wel het gevoel geven dat de hijskraan in hoogte veranderd. Hierna kwam de rotatie van de hijskraan. Wat hier lastig aan was dat ik niet moest vergeten dat de standaard aanpassingen van de transform aan de stad ook weer opnieuwe geschreven moesten worden in de nieuwe animaties anders zag het er toch ineens een heel stuk anders uit. Voor volgende week zal het doel worden om deze animaties aan de interface te gaan koppelen.

### De cabine van de machinist
Naast het bouwen van een stad heb ik natuurlijk ook een plek nodig waar de gebruiker naar de mooie stad kan gaan kijken. Mijn eerste gedacht was zo als ik was begonnen aan dit project, doormiddel van een aantal clip-paths was ik van plan om de panelen van de cabine te maken. Dit is natuurlijk zeker een optie, maar ergens best gek. Ik was al mijn hele project bezig met dozen, en in feite is deze cabine ook een doos. Daarom besloot ik om een doos te maken, ik gaf het dimensies en ik zag niks. Niks? ja niks, ik dacht huh maar ik zet het wel gewoon neer toch, waarom zie ik dan niks. Dus ik begon te spelen met de translate om op zoek te gaan naar de doos. Na veel speurwerk en zelfs het herpositioneren van de hele stad zag ik eindelijk de doos. na verder te puzzelen stond ik ook eindelijk in de doos, maar ik zag niks. Wat ergens best logisch is, want de panelen waren gekleurd met een opacity van 1. Dus deze moesten aangepast worden, en toen zag ik eindelijk mijn stad weer. Waar ik nu mee bezig ben is het plaatsen van een border om de randen van de panelen, dit lijkt toch iets lastiger te gaan. Nou ja met een box-shadow lukt het wel, maar qua performance gaat er iets stuk. Hier ga ik volgende week naar kijken.

### Een interface in 3D
Vorige week was ik bezig met het maken van een interface. Hier was ik met een joystick begonnen die doormiddel van een aantal animaties er voor zorgt dat er een wit vierkant op het scherm gaat bewegen. Nu is mijn idee dat ik met 3D aan de gang ga met mijn hele project, en ja ik zou er voor kunnen kiezen om een 2D paneel te maken dat de 3D wereld bedient. Maar het zou nog leuker zijn als ik ook daadwerkelijk een 3D interface heb. Daarom ben ik deze week ook begonnen met het zetten van de joystick op een 3D box. De doos heb ik gehaald uit mijn bestaande dozen. Hier plaatste ik de joystick op en na het aanpassen van een aantal lijnen in mijn CSS had ik ook daadwerkelijk een joystick in 3D. Daarboven op wil ik een aantal knoppen op mijn interface hebben die andere dingen zullen aanpasssen in de cabine. Ik ben er nog niet helemaal over uit hoeveel knoppen en welke output het gaat bedienen. Volgende week zal ik hier mee verder gaan.

## Feedback deze week
<= nader in te vullen

<hr>

## Installatie & Gebruik

1. Clone deze repository: <a href="https://github.com/Christian199815/MWDND-CSS.git">CSS To The Rescue</a>
