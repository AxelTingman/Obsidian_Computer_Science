#Kurs/Programmering_2 
# #Kurs/Programmering_2/Föreläsning/3 
### Primitiva värden vs. objekt
- Primitiva värden sparas i [[Stack|stacken]] och kan inte muteras, bara kopieras
- [[Instans (Objekt)|Objekt]] sparas på heapen och kan muteras
	- `Häst h = new Häst();`
	- `h.setName(h);` ändrar hästens tillstånd.
	- Objekten är inte lokala i sitt [[Scope|scope]] - dock kan deras referens vara det. 


**Exempel på primitiva värden:**
- int
- double
- long
- char
... osv.