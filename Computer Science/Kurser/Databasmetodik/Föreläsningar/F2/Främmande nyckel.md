#Kurs/Databasmetodik #Kurs/Databasmetodik/Föreläsning/2 

En främmande [[Nyckel|nyckel]] i en tabell  flera atribut som refererar till primärnyckeln *i en annan* tabell.

Alla kolumnvärden som förekommer i främmande nyckel-kolumnerna måste motsvaras av värden i den tabell som en främmande nyckeln refererar till ... (se föreläsning)

Främmande nycklar kan specificeras grafiskt med pilar. Pilen utgår från den/de kolumner som utgör främmande nyckel och pekar på motsvarande primärnyckel-kolumner.

Främmande nycklar kan specificeras grafiskt, som ovan, via pilar.  
Pilen utgår från den (de) kolumn (-er) som utgör främmande  
nyckel och pekar på motsvarande primärnyckel-kolumner.  

Ett annat sätt är att skriva ut vilka främmande nyckel-kolumner  
som svarar mot vilka primärnyckel-kolumner. I fallet ovan har `PERSON` en sammansatt främmande nyckel mot `STAD` och `STAD` har en främmande nyckel mot `LAND`:  

`PERSON. (Stad, Land) utgör FN mot STAD. (Stadsnamn, Landsnamn)` 

`STAD. Landsnamn utgör FN mot LAND. Landsnamn`

”En främmande nyckel är en eller flera kolumner i en tabell som refererar till primärnyckeln en annan tabell.” 

STAD har två kolumner i PN – då måste alla tabeller som vill referera till STAD också har två kolumner i FN.

![[främmande_nyckel.png]]

![[främmande_nyckel_syntax.png]]

![[Pasted image 20230520223713.png]]

### Felexempel
![[främmande_nyckel_felexempel.png]]