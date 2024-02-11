# Dit is de github repository van mijn UVC herkansing! 
Mijn pagina is de review\[reviewId] pagina waar je reviews kan posten. Om op deze pagina te komen moet je eerst naar een recept gaan en op de onderste knop klikken. Deze stuurt je dan naar de reviewpagina die dezelfde id heeft als het recept. Op deze pagina kun je andere reviews zien of zelf een review posten. Dat is mijn CRUD pagina. Het bevat een GET, POST en een DELETE. 

Voor de backend heb ik supabase gebruikt, maar voordat ik aan supabase begonnen ben heb ik eerst zelf een eigen backend gemaakt waar ik een GET van heb gekregen en die ook met docker werkt. Dit is de link naar die repository als u die ook wilt zien: https://github.com/AVoorhoeve514/ReviewBackend . Deze heeft alleen nu niets te maken met mijn CRUD pagina, want mijn database staat op supabase. 

Om mijn CRUD goed te laten runnen heeft u ook de oude backend nodig. Hier staan namelijk de recipes en de users in die nodig zijn om de applicatie goed te laten runnen.  Als deze niet aan staat krijg je een 500 error op een heleboel pagina's en werkt niets. Voor het geval dat u deze nog niet had is hier een link naar de repo van die backend: https://github.com/HugovandeVelde/UVCNLgroep3-backend. Ik gebruik de users table om de userId en naam van de ingelogde gebruiker te laten zien op mijn pagina. Dus wanneer ik een review post op het account van Bob staat er bij dat de review is gepost door Bob.

Nog een dingetje dat ik tegen ben gekomen is als je op de pagina zit en je inspect hem zodat je de mobile view krijgt, krijg je bij sommige dimensions niet de hele pagina te zien. Ik heb de pagina altijd op de Iphone SE afmetingen bekeken.


## Prototype

Dit is het figma prototype dat ik voor het beginnen gemaakt heb:

![Untitled](https://github.com/AVoorhoeve514/ReviewFrontend/assets/123942665/56b420cd-5ead-4e33-b49d-82c5fb798e4e)
![Untitled 2](https://github.com/AVoorhoeve514/ReviewFrontend/assets/123942665/4e9bf204-5f7d-40cf-b02d-982f525c03e8)
![Untitled 1](https://github.com/AVoorhoeve514/ReviewFrontend/assets/123942665/322642b1-64d5-4c7d-9c81-877d74aca0db)

Ik vind dat het best redelijk hetzelfde is gebleven, het enige verschil is dat de reviews op een aparte pagina komen te staan zodat het wat overzichtelijker is. Ook is het duidelijker dat de review over de kok gaat (omdat dat er dit keer bij staat).

![image](https://github.com/AVoorhoeve514/ReviewFrontend/assets/123942665/ce1759cf-8e34-470c-81e3-d4831692624e)

Dit is een screenshot van wat er nu op de receptenpagina staat. De tekst geeft duidelijker aan waar de review voor is en wat je op de volgende pagina kunt doen.


## Testing

Ik heb wat mensen laten testen en zij hebben mij een aantal verschillende feedbackpunten gegeven. Tijdens de testing was de pagina zo goed als klaar, alleen moest er nog wat polish overheen. Een feedbackpunt was dat de reviews allemaal aan elkaar vast zaten en er geen ruimte tussen zat, wat er niet echt mooi uitzag. Dit heb ik meteen opgelost door een <br> tag onder de <div> van de review. Nog een feedbackpunt dat ik op dezelfde manier heb opgelost is dat de navigatiebalk over de onderste review stond en dus wat informatie blokkeerde. Ook dat heb ik met een paar <br> tags opgelost. Een laatste feedback punt was dat het invullen van de score eerst gedaan werd door een nummer in te typen, wat minder handig was dan de score gewoon kunnen selecteren. Nu kan je de score gewoon aanklikken.
