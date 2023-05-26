#Kurs/Databasmetodik #Kurs/Databasmetodik/Föreläsning/3 #Database #Database/SQL 

- Standardspråket för relationsdatabaser sedan 1992.
- Ett **deklarativt** språk, inte procedurellt- Man anger vad som ska göras, inte hur.
- "Relationally complete", men med extra funtionalitet, t.ex. sortera sökresultat.
- Inte ett komplett programspråk, men kan bäddas in i riktiga programspråk (*embedded SQL*).
- Varje sats i SQL kallas för **klausul**. T.ex. select-klausul, from-klausul, where-klausul, etc.

# Klausuler
|Namn|Beskrivning|
|:---|:---|
|SELECT| |
|FROM| |
|WHERE| |
|GROUP HAVING| |
|ORDER BY| |
|ON DELETE| |
|ON UPDATE| |
|CASCASDE|Genomför operationen på alla andra förekomster.|
|RESTRICT|Genomför operationen på bara den valda klassen. |
|SET NULL|Sätter NULL som värde på attributet i samband med operationen framför|ör||
# Tre underdelar
## DDL
## DML
## DCL

# Datatyper i SQL
## Texttyper
|Namn|Beskrivning|
|:---|:---|
|CHAR| |
|VARCHAR| |
|STRING| |
|TEXT| |

## Nmmertyper
|Namn| Beskrivning|
|:---|:---|
|NUMERIC| |
|DECIMAL| |
|INTEGER| |
|SMALLINT| |
|BIGINT| |
|FLOAT| |
|REAL| |
|DOUBLE| |

## Andra datatyper
|Namn| Beskrivning|
|:---|:---|
|BOOLEAN| |
|DATE| |
|TIMER| |
|TIMESTAMP| |
|CLOB| |
|BLOB| |
|XML| |



# SQL-DDL: CREATE TABLE
(se bild från föreläsning 3: slide med samma namn)
1. Översätt Den konceptuella UML-modellen till en logisk RDB-modell.
2.  Se till att alla klasser har en kandidatnyckel. Om det inte finns någon naturlig kandidatnyckel så måste en "syntetisk" primärnyckel utses.
3.  Skapa tabeller som saknar främmande nycklar.
# ALTER TABLE
Förändrar data i en tabell
# DROP TABLE
Raderar hela tabellen
# SQL-DLL: SELECT-kommandot
- Används för att läsa data.
- Kan vara :
	- Väldigt enkla
	- Oerhört komplicerade
	- ... och allt färemellan
## Grundform
`SELECT` (...) Välj column/attribut
`FROM` (...) Anger vilken tabell
`WHERE` (...) ange villkor för 


Exempel:
```
SELECT name, salary
FROM employee
WHERE department = 'shoes'

```
## DISTINCT
Används för att ta bortdubletter i resultatet (inte i själva operationen)
(se föreläsning 3)

# Where-klausulen
- Är inte syntaktiskt nödvändig, men används nästan alltid i praktiken för att joina tabeller (`JOIN`) eller söka/filtrera tabeller
Kan innehålla 
- `=`, `<>`, `>`, `<`, `>=`, `<=`
- Logiska operationer: `AND`, `OR`, `NOT`
(se föräläsning 3)

## IN
Exempel 1 (föreläsning 3):
```
SELECT name, department
FROM Employee
WHERE department IN ('Shoes', 'Perfume')
```

Exempel 2 (föreläsning 3):
```
SELECT name, department
FROM Employee
WHERE department IN
	(
	SELECT dname
	FROM Department
	WHERE manager = 'Berg'
	)
```

## EXISTS
Returnerar `TRUE` om resultatet av en nästlad query inte är tom, och `FALSE` om det är tomt.

Exempel 1 (föreläsning 3):
*"Vem chefar över en avdelning där minst en person tjänar mer än 17000? Visa namnet."*
```
SELECT manager
FROM Department
WHERE EXISTS
	(
	SELECT *
	FROM Employee
	WHERE department = Department.dname
	AND salary > 17000
	)
```
Den nästlade queryn körs två gånger (se föreläsning 3).

# Kombinera tabeller genom JOIN
`JOIN` kombinerar tabeller (två eller fler). Detta är en fundamental egenskap i SQL och hela relationsmodellen.

Särklassigt är oftast över PN/FN-par.

Sällsynt: andra kolumnkombinationer.

Join uttrycks som villkor i WHERE-klausulen
 Exempel (från föreläsning 3):
 *"Ta fram våningen som var och en av de anställda arbetar på"*
 ```
 SELECT name, floor
 FROM Employee, Department
 WHERE dept = dname
 ```

Om man glömmer JOIN-villkoret?:
```
SELECT name, floor
FROM Employee, Department
```
Riskerar att skapa en ***kartetisk produkt***, vilket innebär att felaktiga och irrelevanta värden presenteras.

#### Join mellan fler än två tabeller

Exempel (F3):
```
SELECT c.city AS City, CN.name AS Continent
FROM City C, Country CO, Continent CN
WHERE C.country = CO.coid
AND CO.continent  CN.cnid
```

#### Self-join
Exempel (Frl. 3):
*"Vilka kontinentstorlekar finns det fler än en kontinent som har?"*
```
SELECT DISTINCT C1.size AS continentSize
FROM Continent C1, Continent C2
WHERE c1.size = C2.size
AND C1.cnid <> C2.cnid
```

# Alias
Används för att döpa om kolumner och tabeller. Detta förs i `FROM` för tabeller och i `SELECT` för kolumner.

Exempel 1 (F3):

```
FROM Tabell AS alias
```

eller

```
FROM Tabell alias
```

Exempel 2 (F3): 
`SELECT column AS alias`

För att slippa skriva långa tabell-/kolumnnamn i SQL: `n`

För att kunna gra s.k. *self-join* med en tabell senare

#### Kvalificera kolumnnamn
Görs när tabeller i `FROM` innehåller kolumner med samma namn.
Exempel (F3):
```

```

# Räkna i SQL
Exempel (F3):
*"Hur många kontinenter finns det?"*
```
SELECT CLOUNT(*) AS antal
FROM Continent
```

Exempel 2 (F3):
*"Vilka kontinentstorlkear finns det fler än en kontinent som har?"*
```
SLECT size
FROM Continent
GROUP BY size
HAVING COUNT(*)
```