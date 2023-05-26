#Kurs/Databasmetodik 
# $\cap$

Kombinerar rader från två tabeller och tar med alla rader som förekommer i båda tabellerna. Dubbletterna tas med bara en gång.


## INTERSECT
Returnerar de rader som finns i både mängd A och mängd B.
Exempel:
````
SELECT name, age FROM Cat
WHERE age > 5
INTERSECT
SELECT name, age FROM Dog
WHERE owner = 'Berg'
````

Microsoft Access har ingen INTERSECT-funktion.
INTERSECT-sats i Access:
````
SELECT name, age FROM Cat
WHERE age > 5
AND EXISTS (
SELECT * FROM Dog
WHERE owner = 'Berg'
AND name = Cat.name
AND age = Cat.age)