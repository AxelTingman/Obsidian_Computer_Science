#Kurs/Databasmetodik #Kurs/Databasmetodik/Föreläsning/1  #Modelling/UML

Multipliciteten eller kardinaliteten för ett attribut eller en roll i en association visar hur många objekt som associationen måste kan/måste minst/mest referera till eller hur många värde attributen kan eller måste anta.

Multipliciteten för rollerna i en association placeras närmast den klass som rollen refererar till.

***
Kallas även för *kardinalitet*, *avbildningsregler* eller *min- och maxvärden* 

Multipliciteten för ett [[Kurser/Databasmetodik/Attribut|attribut]] eller en roll i en association visar hur många objekt som associationen måste kan/måste minst/mest referera till eller hur många värde attributen kan eller måste anta.

Multipliciteten för rollerna i en association placeras närmast den klass som rollen refererar till.

Det är viktigt att ange multipliciteten när databaser avbildas, även om man är osäker på dessa. Anledningen är att det är bättre att alla tolkar UML-schemat på samma felaktiga sätt än att olika personer tolkar UML-schemat på olika (felaktiga) sätt.

1..1 -> "minst en och högst en"
1..* -> "minst en och obegränsat övre antal"
0..* -> "noll eller obegränsat övre antal"
0..1 -> "noll och högst en" (nollor bör undvikas som minimumvärde!)