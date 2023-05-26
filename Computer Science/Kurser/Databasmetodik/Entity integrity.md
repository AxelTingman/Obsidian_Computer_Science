#Kurs/Databasmetodik #Kurs/Databasmetodik/Föreläsning/2 

Att välja en kolumn (eller flera kolumner) till  primärnnyckel innebär att  

[[Kurser/Databasmetodik/Primärnyckel|PN]]-kolumnen (kolumnerna) unikt ska identifiera en rad

ingen del av dessa kolumner någonsin får vara  NULL (primärnyckelns roll är ju att identifiera en rad och den måste alltså alltid finnas!). Denna regel brukar kallas entity integrity. Alternativnycklar får däremot vara NULL (men måste inte vara det).