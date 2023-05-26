#Kurs/Människa-datorinteraktion 
Gemensamt språk för att prata om att utveckla användargränssnitt.

Inspration från arkitektur och stadsplanering.

[[Designprinciper|Designprinciper]] är kortfattade, medan designmönster är mer utförliga.
[[Iterativ systemutveckling|Iterativ design]] - Man rättar till [[Design|designen]] i flera iterationer.

Exempel på designmönster:
- Meny
- Sökning
- Karusell
- Formulär
- Wizard

## Meny
Kategoerier av funktioner eller information.

Används för att hjälpa användaren var den akn hitta det den letar efter.

Problem: Användaren behöver veta var det går att hitta den den letar efter.

Lösning: Placera en meny synligt jämt på samma ställe på sidna. Erbjud även andra sätt att navidera på.

Använd när: Alla websidor behöver någon typ av huvudsaklig navidering.

Tänk på att placera alternativen enligt [[Gestaltlagarna|gestaltlagarna]].

Djup och bredd: 7 +- 2 grejer i varje lager i menyn.

Kortkommandon.

Sortering: 
Kategorier
Kronologisk ordning
Alfabetisk ordning.

## Sökning
Problem: 
användaren vill hitta ett alternativ ellet en viss informtion.

Lösning: 
Erbjud en sökruta. Visa sökresultaten med en kort beskrivning.

Använd när: 
Det redan finns en huvudsaklig navigation. Användaren kan vilja söka efter ett alternativ i en kategori. Användaren kan vilja förfina en specifik sökning.

Används som komplement till annan navigering.

Anvndaren måste veta vad vad den letar efter.

Svårt att veta vilken typ av dokument som söks igenom.

Ofta ett snabbt sätt att navigera.

Stavning av sökord kan vara ett problem.

Kår att kombinera sökfunktionen med olika filter. 

## Karusell
Problem: 
Användaren behöver välja ett alternativ bland mnga

Lösning: 
Visa alternativen som bilder i en ring, eller en del av en ring.

Använd när: 
Det finns en unik bild för varje alternativ. Alternativen liknar varandra och är på samma nivå. Det finns en plats att visa max tio bilder. Alternativens namn, och annan metadata, kan visas vid varje bild.

Max 10 bilder är rekommenderat.

Alternativens namn och anna metadata visas vid varje bild. 

Egenskaper:
- Bilder på produkter som de ser ut. Inga metaforer.
- Bara ett fåtal bilder i taget.
- En del av alternativen är gömda.
- Kan inte hoppa framåt bland alternativen.

## Formulär
Problem: 
Användaren behöver ge uppgifter till den som erbjuder tjänsten.

Lösning: 
Erbjud ett formulär som samlar in de nödvändiga uppgifterna.

Använd när: 
Användaren behöver lämna uppgifter. Exempel: boka resa, göra en avancerad sökning, registrera sig på en webplats eller logga in. Måste vara del av användarens uppgift eller åtminstone vara till fördel för användaren.

 Tänk på: 
 Att bara samla in sådan information som är lagligt att samla in och som är till nytta för användaren.

Egenskaper:
- Korta ledtexter
- Gestaltlagarna
- Storlek på fälten
- Obligatoriska fält
- Hur gå vidare
- Ordning (användarens ordning!)

## Wizard
Problem:
Användaren vill nå ett bestämt mål, men flera beslut måste fattas på vägen (de kan vara okända för användaren).

Lösning:
Led användaren igenomuppgiften, ett steg i taget. Visa vilka steg och alternatv som finns.

Använd när:
En icke-expert behöver lösa en uppgift som är relativt ovanlig. Beslut behöver fattas i varje deluppgift. 3-10 deluppgifter rekommenderas. Deluppgifter kan vara beroende eller oberoende av varandra.

Egenskaper.
- Kräver ingen inlärning
- Bryter ner en avancerad process till enklare steg
- Kan uppfattas som långsamt
- Kan uppfattas som begränsande för användaren

## Direkmanipulation
Till exempel att dra ikoner i ett desktopgränssitt.

