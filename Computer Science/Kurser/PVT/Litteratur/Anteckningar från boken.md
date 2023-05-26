#Kurs/Projektarbete_Med_Progamvaruteknik 
Från [[Ian Sommerville, 2021]]
***
***
# 1. Software Products
Det är viktigt att snabbt nå ut med en produkt till marknaden eftersom kunder ofta är ovilliga att ändra sitt val av programvara som de är van att använda, även om det finns alternativ som egenligen är bättre.

Utvecklaren - inte kunden - bestämmer vilka egenskaper ett systems ska ha. Utvecklaren fattar sitt beslut utifrån kundens behov (s. 13).

Systemutveckling kan delas in i *projektbaserad* och *produktbaserad* (s. 14).

*Product manager* (PM) är en roll som går ut på attbedöma och fatta beslut om huruvida en produkt passar kundens behov. PM fokuserar på att kundens behov uppfylls snarare än att vilka tekniska funktioner som används. På stora företag är det vanligt att det finns anställda som är specialiserade i rollen som PM, men på mindre företag är det vanligare att utvecklarna delar på rollen som PM (s.21).
***
***
# 2. Agile Software Engineering
Agila utvecklingsmetoder är viktiga för att **snabbt nå ut** med produkten till marknaden (s. 30).

Agila utvecklingmetoder togs fram som ett **alternativ till *plandrivna* utvecklingsmetoder** som ansågs vara för långsamma eftersom alldeles för mycket tid gick åt att planera och dokumentera utvecklingsarbetet innan produkten kunde börja utvecklas. Dessutom blev mycket tid bortslösad eftersom mycket av vad som hade planerats i början fick planeras om senare (s. 31).

#### Extreme programming
*Extreme programming* (XP) är en agil utvecklingsmetod som understryker vikten av att ständigt (extremt ofta) förbättra koden - ibland flera gånger per dag (s. 34).

XP förespråkar "Simple dsegin" som en av sinda ledord. *YAGNI* ("You Ain't Gonna Need It") är en princip inom XP som innebär att utvecklaren bara ska utveckla funktionalitet som är efterfrågad och inte försöka förutspå eventuella framtida situationer. Detta kan dock vara problematiskt eftersom kunderna ofta saknar kunskap om vilken funktionalitet som behövs (s.35).

XP förespråkar gemensamt ansvar för all kod skrivs ("Collective ownership"). Detta har dock ofta visat sig vara opraktiskt eftersom det är vanligt att specialister behövs för vissa delar av koden.

XP förestpråkar parprogrammering med motiveringen att två personer är kan lära sig av varandra och uppmärksamma varandra på om någon gör ett misstag. Det finns dock inte mycket empiriskt material som pekar på att dessa fördelar skulle vara starkare hos de som programmerar i par jämfört med de som programmerar enskilt (s. 37).

#### Scrum
*Product Owner* är den som ansvarar för att utvecklarna alltid fokuserar på slutprodukten snarare än tekniskt intressanta detaljer. Denna roll antas av den som normalt är product manager (s. 38).

*Scrum Master* är den som expert scurm som utvecklingsmetod och vägleder gruppen. Scrum master är inte en konventionell project manager utan bör snarare btraktas som en coach. Det är dock vanligt att Scrum master har båda rollerna (s. 38).

"Potentially shippable product increment" innebär att varje sprint bör resultera i kod som är av tillräckligt hög kvalitet så att den kan levereras till kunden. Den ska vara komplett, testad, dokumenterad och, om nödvändigt, recenserad. Kvaliten ska vara såpass hög att den kan demonsteras för kunden (s. 39).

En *sprint* är cirka två till fyra veckor innehåller flera dagliga möten (s. 39).

***
***
# 3.  Features, Scenarios and Stories
Det är tre faktorer som driver designen av mjukvaruprodukter: (1) behov som ej är tillfrdsställda, (2) missnöjdhet med befintlig produkt och (3) tekniska framsteg som möjliggör helt nya typer av rpodukter (s. 60).

***
***
# 4. Software Architecture
IEEE definition of **system architecture**:
"Architecture is the fundamental organisation of a software system embodied in its components, their relationsip to each other and to the environment, and the principles guiding its design and evolution."

A **component** can be anything like a program in a large scale or an object in a small scale.

Funktionella och synliga funktioner bör utvecklas så snart som möjligt i början. Icke-funktionella egenskaper är också viktiga, men bör implementeras i ett senare skede (s. 94).

Icke-funktionella egenskaper i ett system:
- [[Responsiveness]]
- [[Reliability]]
- [[Tillgänglighet (Availability)]] 
- [[Security]]
- [[Usability]]
- [[Maintainability]]
- [[Resiliance]]


Många webbaserade applikationer använder [[Multi-tier architecture]] med flera kommunicerande servrar där var och en har ett specifikt syfte (s. 116). T.ex:
- En webserver som kommunicerar med klienter med [[HTTP]]-protokoll.
- En applikationsserver som ansvarar för applikationsspecifika operationer
- En databasserver som hanterar och överför data till och från databasen.