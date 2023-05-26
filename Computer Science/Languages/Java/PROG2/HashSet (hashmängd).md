#Kurs/Programmering_2/Föreläsning/4 
Kallas även för *hashmängd*.

- Hashtabellsimplementering
- Håller alla element osorterade (eftersom det är en mängd)
- Innehåller inga dubletter
- Mycket snabb sökning, tillägg och borttag.
- Använder HashCode() som index.

Elementen i ett HashSet tilldelas en slumpmässig plats som baseras på deras [[hashCode]]. Om ett element som ska läggas till i listan kolliderar med ett element som redan finns på den plats som tilldelades måste listan itereras igenom för att kontrollera att objektet inte redan är tillagt (eftersom dubletter inte är tillåtna). Varje gång detta sker minskar prestandan för programmet betydligt.
![[f4_hashset.PNG]]