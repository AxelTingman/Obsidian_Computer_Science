#Kurs/Databasmetodik 

Exempel : ``UNION``,  ``INTERSECT`` och ``EXCEPT``.

Opererar på mängder av rader.

INPUT: två radmängder, de så kallade operanderna. Dessa två är resultaten av  varsin SELECT-sats.

OUTPUT: en radmängd, resultatet som visas.

Operanderna måste vara/göras unionskompatibla. Måste ha samma antal kolumner och parvis samma domän för koolumnerna (samma datatyper). SQL kräver dock itne parvis samma kolumnnamn. Första opeerandens kjolumnnamn används i resultatet

Resultatet är automatiskt dublettfritt.

## Unionskompatibilitet
**Tre mängder**
Cat(<u>name</u>:string, age:int, ownedBy:string)
Dog(<u>name</u>string, age:int, owner:string)
Pig(<u>name</u>:string, age:int, price:int)

I exemplet ovan är Cat och Dog unionskompatibla med varandra, medan Pig är inte unionskompatibel med varken Cat eller Dog.

Exempel:
```
SELECT * FROM Cat
WHERE age >= 5
UNION
SELECT * FROM Dog
WHERE owner = 'Clint Eastwood'
```

## UNION
Returnerar alla rader i mängd A och mängd B. Dubletterna tas bort.



# [[Snitt (intersect)]]


````


## EXCEPT
Returnerar  som finns i mängd A förutom det som finns i mängd B.

Exempel:
````
SELECT name, age FROM Cat
WHERE age > 5
EXCEPT
SELECT name, age FROM Dog
WHERE owner = 'Berg'
````

Microsoft Access har ingen EXCEPT-funktion.
EXCEPT-sats i Access:
````
SELECT name, age FROM Cat
WHERE age > 5
AND NOT EXISTS (
SELECT * FROM Dog
WHERE owner = 'Berg'
AND name = Cat.name
AND age = Cat.age)
````



