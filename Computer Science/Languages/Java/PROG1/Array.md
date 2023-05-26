#Programming/Java #Kurs/Programmering_1

En [[Samlingar| samling]] som har en bestämd storlek och [[Variabel#^3260b2| datatyp]] som den kan lagra.

Skrivs på följande sätt:

int[]  siffror;
	siffror[0] = 456;
	siffror[1] = 735;

#### Egenskaper
F4:
-  Sammanhängande minnesutrymme, befintlig array kan inte utökas eller minskas
- Ofta maximerad, kompletterad med en antalsvariabel
- Utökning kan simuleras genom allokering av större array och kopiering av gamla värden till den nya arrayen
- Direktåtkomststruktur: mycket snabb indexering
- Snabba tillägg och bortag i slutet om extra utrymme finns.
- Långsamma
- tillägg/borttag i början/mitten (befintliga element måste flyttas.