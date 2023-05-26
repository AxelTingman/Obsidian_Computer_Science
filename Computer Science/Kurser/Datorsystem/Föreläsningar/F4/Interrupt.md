#Kurs/Datorsystem #Kurs/Datorsystem/Föreläsning/4 
***
#### Hur sker en interrupt?
- En enhet som vill att procesorn ska göra ett avbrott antecknar det i  ett register
- Processorn kontrollerar efter execute-cykeln om avbrott ska göras.
- Om avbrott ska göras ändras programräknarens värde till adressen för avbrottshanteraren.

#### Interrupt-cykeln
- Innehållet i programräknaren flyttas till MBR och skrivs till minnet
- Addressen till avbrottshanteraren flyttas till programräknaren

[[Maskable Interrupt]] & [[Non-Maskable Interrupt]]
