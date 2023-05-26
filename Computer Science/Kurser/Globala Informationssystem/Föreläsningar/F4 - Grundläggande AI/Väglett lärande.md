#Kurs/Globala_Informationssystem #Kurs/Globala_Informationssystem/Föreläsning/4 
***
**Träningsfas**: Systemet lär sig från träningsdata - dataexempel som tillhör ett antal dataklasser (t.ex djurarter).

**Testfas**: Systemet tillämpar kunskaper skapande under träningsfasen och sparade i den prediktiva modellen.
	- Systemet frå nya dataexempel, kollar i den prediktiva modellen och gör en bedömning vilket av de nya dataexemplen tillhör vilken dataklass (t.ex. vilken djurart som syns på den nya bilden).

#### Dataklasser och dess särdrag
Det finns ett antal fördefinierade dataklasser, t.ex. *hund* och *katt* samt fördefinierade *särdrag* som karakteriserar detaexempel som tillhör varje klass.


## Använding av träningsdata
[[Kluster|Datakluster]] är grova dataklasser.
	- Särdragsextraktion
	- Val av dataexempel som träningsdata T.ex:
		- [[Kluster|Klustring]] man upptäcker avvikande betalkortstransaktioner som möjliga bedrägeriförsök
		- [[Träningsdata|Träningsdata]]: man tränar systemet med upptäckta exempel för att känna igen bedrägeriförsök ännu bättre. 

## Skillnader från icke-väglett lärande
- Affärsmässiga är automatiskt beslutsfattande.
- Klassificering av data, d.v.s. olika automatiska beslut motsvarar placering av olika dataexempel i olika dataklasser.
- Systemet i drift är alltid självgående.