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

## Doelen voor volgende week
empty

<hr>

## Installatie & Gebruik

1. Clone deze repository: <a href="https://github.com/Christian199815/MWDND-CSS.git">CSS To The Rescue</a>
