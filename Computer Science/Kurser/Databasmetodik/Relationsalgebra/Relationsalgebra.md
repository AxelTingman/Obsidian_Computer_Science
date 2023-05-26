#Kurs/Databasmetodik

Matematiska uttryck för [[Kurser/Databasmetodik/Relationsmodellen|Relationsmodellen]]

Finns [[Primitiva operationer]] och [[Icke-primitiva operationer]]


### Tips
• Tänk ett steg i taget (en operation i taget).  
• Kontrollera alltid (inför varje operation) vilka kolumner  
som ingår i tabellerna. Går det överhuvudtaget att  
använda en viss operation, är tabellerna  
unionskompatibla t ex? Om inte, fixa till  
unionskompatibilitet, t ex genom att använda  
tilldelning och projektion!  
• Tänk på i vilken ordning operationerna utförs. Styr  
med parenteser vid behov.  
• Använd tilldelning för att dela upp stora satser i  
mindre delar.  
• Eventuellt: Använd projektioner för att ta bort onödiga  
kolumner. Försiktigt dock så att vi inte ta bort  
kolumner som vi behöver senare.