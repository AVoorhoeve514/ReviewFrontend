# Dit is de github repository van mijn UVC herkansing! 
Mijn pagina is de review\[reviewId] pagina waar je reviews kan posten. Om op deze pagina te komen moet je eerst naar een recept gaan en op de onderste knop klikken. Deze stuurt je dan naar de reviewpagina die dezelfde id heeft als het recept. Op deze pagina kun je andere reviews zien of zelf een review posten. Dat is mijn CRUD pagina. Het bevat een GET, POST en een DELETE. 

Voor de backend heb ik supabase gebruikt, maar voordat ik aan supabase begonnen ben heb ik eerst zelf een eigen backend gemaakt waar ik een GET van heb gekregen en die ook met docker werkt. Dit is de link naar die repository als u die ook wilt zien: https://github.com/AVoorhoeve514/ReviewBackend . Deze heeft alleen nu niets te maken met mijn CRUD pagina, want mijn database staat op supabase. 

Om mijn CRUD goed te laten runnen heeft u ook de oude backend nodig. Hier staan namelijk de recipes en de users in die nodig zijn om de applicatie goed te laten runnen.  Als deze niet aan staat krijg je een 500 error op een heleboel pagina's en werkt niets. Voor het geval dat u deze nog niet had is hier een link naar de repo van die backend: https://github.com/HugovandeVelde/UVCNLgroep3-backend. Ik gebruik de users table om de userId en naam van de ingelogde gebruiker te laten zien op mijn pagina. Dus wanneer ik een review post op het account van Bob staat er bij dat de review is gepost door Bob.

Nog een dingetje dat ik tegen ben gekomen is als je op de pagina zit en je inspect hem zodat je de mobile view krijgt, krijg je bij sommige dimensions niet de hele pagina te zien. Ik heb de pagina altijd op de Iphone SE afmetingen bekeken.


## Dit is de figma prototype die ik gemaakt heb voordat ik aan deze pagina begon.
![Untitled](https://github.com/AVoorhoeve514/ReviewFrontend/assets/123942665/56b420cd-5ead-4e33-b49d-82c5fb798e4e)
![Untitled 2](https://github.com/AVoorhoeve514/ReviewFrontend/assets/123942665/4e9bf204-5f7d-40cf-b02d-982f525c03e8)
![Untitled 1](https://github.com/AVoorhoeve514/ReviewFrontend/assets/123942665/322642b1-64d5-4c7d-9c81-877d74aca0db)
Ik vind dat het best redelijk hetzelfde is gebleven, het enige verschil is dat de reviews op een aparte pagina komen te staan zodat het wat overzichtelijker is. Ook is het duidelijker dat de review over de kok gaat (omdat dat er dit keer bij staat).

![image](https://github.com/AVoorhoeve514/ReviewFrontend/assets/123942665/ce1759cf-8e34-470c-81e3-d4831692624e)
Dit is een screenshot van wat er nu op de receptenpagina staat. De tekst geeft duidelijker aan waar de review voor is en wat je op de volgende pagina kunt doen.


Use Case (Front-end):
Use Case
Use Case Name Post review
Actor Gebruiker
Summary
Een gebruiker wilt zijn/haar mening geven over
een kok/recept waar zij van gegeten hebben
kunnen posten zodat andere gebruikers deze
kunnen lezen.
Priority Must have
Status In progress.
Pre-Condition De gebruiker moet zijn ingelogd in een account
Post-Condition
De geposte review is zichtbaar in de app en in
de database
Basic Path 1. De gebruiker gaat naar de pagina van een
recept
Herkansing UVC (Alwyn Voorhoeve) 3
Use Case
2. De gebruiker klikt op de ‘Add Review’ knop
3. De gebruiker beland op de ‘Add Review’
pagina
4. De gebruiker vult alles in wat er op de pagina
staat
5. De gebruiker drukt op de ‘Post Review’ knop
om de review te posten.
Alternative Paths
De gebruiker kan ervoor kiezen om de review
niet te posten en dus niet op te slaan.
De gebruiker kan de review niet posten omdat
niet alle benodigde velden zijn ingevuld.
Business Rules:
Het posten van reviews is alleen mogelijk
wanneer de gebruiker is ingelogd in een
account.
Non-Functional Requirements
De gebruiker moet eerlijk zijn/haar mening
geven.
De gebruiker moet gemakkelijk en snel de
review kunnen posten
Use Case (Back-end):
Use Case
Use Case Name Post review
Actor Back-end systeem
Summary
De back-end moet ervoor zorgen dat wanneer
de user een request stuurt om een review te
posten, deze ook toegevoegd word aan de
database
Priority Must have
Status In progress.
Herkansing UVC (Alwyn Voorhoeve) 4
Use Case
Pre-Condition
De gebruiker heeft het proces van het posten
gevolgd en alle benodigde gegevens zijn
aanwezig
Post-Condition De review word opgeslagen in de database en
is zichtbaar in de app.
Basic Path
1. Er komt een request van de front-end binnen
bij de back-end voor het toevoegen van een
review
2. De back-end checked of alle benodigde
gegevens aanwezig zijn
3. Zodra de controle af is word er een in het
systeem een id aangemaakt voor de review
4. De review word door het systeem
opgeslagen in de database
5. De review wordt verstuurd naar de front-end.
Alternative Paths
Als niet alle benodigde informatie aanwezig is
word er een foutmelding naar de front-end
verstuurd.
Business Rules: Alle velden moeten worden ingevuld.
Non-Functional Requirements Gebruikers mogen geen toegang hebben tot de
back-end API.
