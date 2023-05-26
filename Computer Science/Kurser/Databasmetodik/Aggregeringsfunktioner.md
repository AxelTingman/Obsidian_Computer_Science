#Kurs/Databasmetodik 

Vi behöver ofta göra mer med vår data änm att "bara" hämta fram data direkt från tabeller och kolumner. När man *aggregera* används SQL:s aggregeringsfunktioner.

|Funktion|Returnerar|
|:---|:---|
|Count(\*)|Radantal i en tabell - se GROUP BY|
|Count(*kolumn*)|Antalet icke-NULL-värden i en kolumn|
|SUM(*kolumn*)|Summan av icke-NULL-Värdena i en kolumn|
|MIN(*kolumn*)|Det minsta av icke-NULL-värden i en kolumn|
|MAX(*kolumn*)|Det största av icke-NULL-värden i en kolumn|

## En SQL-query med COUNT()
![[count.PNG]]

![[count-2.PNG]]