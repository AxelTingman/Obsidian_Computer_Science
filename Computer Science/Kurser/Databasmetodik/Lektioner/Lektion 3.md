#Kurs/Databasmetodik/Lektion/4 



```
SELECT kostnad, pris
FROM Kurs
WHERE längd > 4
```

```
SELECT kostnad, pris
FROM Kurs
WHERE längd = 4
AND pris > 4000
```

- Alla vilkor skrivs i where-klausulen.


``SELECT kostnad, pris`` 
``FROM Kurs, Ktilf`` <- Exempel på join-villkor
``WHERE längd = 4``
``AND pris > 4000`` <- Filter-/sökvillkor

***

Följande två kodexempel uppfyller samma funktion.
Distinct-satsen behövs eftersom det kan uppstå dubletter:
```
SELECT kostnad, pris
FROM Kurs
WHERE kostnad IN (
	SELECT kurs
	FROM Ktillf
	WHERE lokal = 'Jupiter'
	)
```


``SELECT DISTINCT kostnad, pris``
``FROM Kurs, Ktillf``
``WHERE kurskod = kurs``
``AND lokal = *Jupiter*``


***


## S4
***Ta fram namn och adress på elever som har haft Sofia Wilsson som lärare.***

``SELECT DISTINCT E.namn, E.adress`` <- Distinct behövs för att undvika dubletter eftersom samma elev kan ha haft Sofia WIlson som lärare flera gånger. 
``FROM Elev E, Deltag D, Ktillf KT, Lärare L`` <- Bokstäverna efter tabellnamnen är alias
``WHERE E.eid = D.elev``
``AND D.stat = KT.stat``
``AND D.kurs = KT.kurs``
`AND KT.lärare = L.Gd`
`AND L.lnamn = 'Sofia Wilsson'`

### Alternativ lösning med IN-sats
`SELECT E.namn, E.adress`
`FROM Elev.E`
`WHERE I.eid IN (`
	`SELECT D.elev`
	`FROM Deltag D
	`WHERE (D.stat, D.kurs) IN (
		`SELECT KT.stat, KT kurs
		``FROM Ktillf.KT``
		`WHERE KT))`

***

## S6

***

## S7
***Vilka lärare har aldrig hållit någon kurs? Visa namnen!***

```
SELECT L.lnamn
FROM Lärare L
WHERE L.lid NOT IN (
	SELECT KT.lärare
	FROM Ktillf.KT)
```