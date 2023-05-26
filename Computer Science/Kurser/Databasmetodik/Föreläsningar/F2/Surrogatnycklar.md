#Kurs/Databasmetodik #Kurs/Databasmetodik/Föreläsning/2 

Vanliga användardefinierade [[Nyckel|nycklar]] kan vara bristfälliga på olika sätt:
- De förändras över tid.
- Olika användargrupper kan använda olika kolumner för att identifiera en ch samma tabell.
- Nycklar bestående av "riktiga" attribut an bli mycket långa.

Exempel kan vara ID-nummer. Dessa nummer har ingen representation i den "riktiga" världen. 

Surrogatnycklar är vanligen inte synliga i användargränssnitt mot databasen. 




Vanliga användardefinierade nycklar kan vara bristfälliga  på olika sätt:
- De förändras över tid. T ex kan verksamhetsreglerna ändras, det attribut som en gång var unikt kanske inte längre är det 
- Olika användargrupper kan använda olika kolumner för att identifiera en och samma tabell  
- Nycklar bestående av “riktiga” attribut kan bli mycket långa (i värsta fall alla kolumnerna i tabellen)

En surrogatnyckel är en konstgjord identifierare, genererad av databashanteringssystemet som garanterar att den alltid är unik.  


- Användarna behöver inte vara medvetna om  surrogatet  
- Surrogatnycklar är vanligen inte synliga i användargränssnitt mot databasen. Fortfarande har man alltså behov av att kunna använda ‘naturliga’ attribut (som Namn, Från, Till, etc.) i sökningar mot databasen  
- Analys av vilka naturliga kolumner som eventuellt identifierar en rad skall alltså alltid göras oberoende av om surrogatnyckel används eller ej  
- Surrogatet används dock internt som en unik identifierare och även i främmande nyckel-referenser