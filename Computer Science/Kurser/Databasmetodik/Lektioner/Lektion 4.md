#Kurs/Databasmetodik/Lektion/4

# S11
***Ta fram kurskod och längd på kurser som hållits i lokalen Orion och i lokalen Jupiter, men aldrig i lokalen Tellus.***

``SELECT kurskod, längd``
``FROM Kurs``
``WHERE kurskod IN(``
``	SELECT kurs FROM Ktillf WHERE lokal = 'Orion')``
``AND kurskod IN(``
	```SELECT kurs FROM Ktills WHERE lokal = 'Jupiter')```
```AND kurskod NOT IN(```
```	SELECT kurs FROM Ktillf WHERE lokal = 'Tellus')```

***
# S12
***Ta fram kurstillfällen som inte har haft någon elev från Bro. Visa kurskod och startdatum.***

``SELECT KT.kurs, KT.startdatum`` <- kurskod definierar kurs
``FROM Ktillf KT``
``WHERE NOT EXISTS(``
``SELECT * FROM Deltag D, Elev E WHERE D.elev = E.eid``
``AND D.ort = 'Bro'``
``AND D.sdat = KT.sdat``
``AND D.kurs = KT.kurs``

***
# S13
***Hur många kurstillfällen har hållits för varje kurs? Visa kursbenämning och antal.***
``CREATE VIEW AKTPK AS`` <- följande kod behövs inte i Access
``SELECT K.kursben COUNT(*) AS Antal``
``FROM kurs K, Ktillf KT``
``WHERE K.kurskod = KT.kursben`` 
``GROUP BY K.kurskod, K.kursben``

***
# S14
***Vilken kurs har haft flest kurstillfällen? Visa kursbenämning och antal.***
``SELECT AKTPK.kursben, AKTPK.antal``
`FROM AKTPK`
`WHERE AKTPK.antal = (SELECT MAX(antal) FROM AKTPK)`

***
# S15
***Hur många kurstillfällen har varje elev gått? Visa namn och antal.***
`SELECT enamn, COUNT(*)`
`FROM Elev, Deltag`
`WHERE eid=elev`
`GROUP BY eid, enamn`

***
# S16
***Hur många kurser har varje elev gått? Visa namn och antal.***

`SELECT enamn, COUNT(*) antal`
`FROM Elev, (SELECT DISTINCT kurs, elev FROM Deltag) AS X`
`WHERE eid = elev
`GROUP BY eid, enamn

***
# S17
***Vilka lärare har gett alla kurser? Visa namnen.***
*Hur man ska tänka:*
1. Om det inte finns några kurser kvar efter att vi har dragit bort alla kurser som en lärare har gett, så har den läraren gett alla kurser.
2. Gör detta för alla lärare, så hittas de lärare som har gett alla kurser.

**Steg 1 -** för en given lärare, såg Lena Svensson, har hon gett alla kurser?:
`SELECT * FROM Kurs K WHERE K.kurskod NOT IN (`
`SELECT KT.kurs FROM Ktillf KT WHERE KT.lärare = (`
`SELECT L.lid FROM Lärare L WHERE L.lnamn = 'Lena Svensson'))`

**Steg 2 -** Vi generaliserar för att göra detta steg effektivt i en enda SQL-sats:
`SELECT L.lnamn FROM Lärare L`
`WHERE NOT EXISTS (`
`SELECT * FROM Kurs K WHERE K.kurskod NOT IN (`
`SELECT KT.kurs FROM Ktillf KT WHERE KT.lärare = L.lid` <- 'L.lid' återkopplar till 'L' på rad 1.

# S18
***Hur många kurstillfällen har varje lärare hållit? Visa lärareid, namn, samn antal kurstillfällen. Alla lärare ska med.***

`SELECT lid, `