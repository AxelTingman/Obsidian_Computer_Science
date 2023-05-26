#Kurs/Databasmetodik #Kurs/Databasmetodik/Övning
***
## 3A
Ta fram personnummer på lärare som har undervisat i rummet med id 1!

```
SELECT Kurstillfälle.lärare
FROM Lärare, Kurstillfälle
WHERE Lärare.personnummer = Kurstillfälle.lärare
AND Kurstillfälle.rum = 1
GROUP BY Kurstillfälle.lärare
```
Ta fram personnummer på lärare som har undervisat i rummet med id 2!
***
## 3B
Ta fram personnummer på lärare som har undervisat i rummet med id 2!

```
Select Lärare.personnummer
FROM Lärare, Kurstillfälle
WHERE Kurstillfälle.lärare = Lärare.personnummer
AND Kurstillfälle.rum = 2
GROUP BY Lärare.personnummer
```

***
## 4A
Ta fram personnummer, namn och telefon på lärare som har undervisat i rummet med id 1!

```
SELECT Person.personnummer, Person.namn, Person.telefon
FROM Person, Kurstillfälle
WHERE Kurstillfälle.lärare = Person.personnummer
AND Kurstillfälle.rum = 1
GROUP BY Person.personnummer
```

***
## 5A
Ta fram personnummer, namn och tjänsterum på lärare som har undervisat i rummet med id 1!

```
SELECT DISTINCT Person.personnummer, Person.namn, Lärare.tjänsterum
FROM Person, Lärare, Kurstillfälle
WHERE Kurstillfälle.rum = 1
AND Kurstillfälle.lärare = Person.personnummer
AND Lärare.personnummer = Person.personnummer
```
***
## 6A
Ta fram personnummer på studenter som har deltagit i något kurstillfälle i Jupiter!

```
SELECT DISTINCT Deltagande.student
FROM Deltagande, Kurstillfälle, Rum
WHERE Rum.namn = "Jupiter"
AND Kurstillfälle.rum = Rum.id
AND Deltagande.kurs = Kurstillfälle.kurs
AND Kurstillfälle.rum = Rum.id
AND Deltagande.startdatum = Kurstillfälle.startdatum
```
***
## 6B
Ta fram personnummer på studenter som har deltagit i något kurstillfälle i Orion!

```
SELECT DISTINCT Deltagande.student
FROM Deltagande, Kurstillfälle, Rum
WHERE Rum.namn = "Orion"
AND Kurstillfälle.startdatum = Deltagande.startdatum
AND Kurstillfälle.kurs = Deltagande.kurs
AND Kurstillfälle.rum = Rum.id
```
***
## 6C
Ta fram personnummer på studenter som har deltagit i något kurstillfälle i Orion!

```
SELECT DISTINCT Deltagande.student
FROM Deltagande, Kurstillfälle, Rum
WHERE Deltagande.startdatum = Kurstillfälle.startdatum
AND Deltagande.kurs = Kurstillfälle.kurs
AND Kurstillfälle.rum = Rum.id
AND Rum.namn = "Tellus"
```
***
## 6D
Ta fram personnummer på studenter som har deltagit i något kurstillfälle i Sirius!

```
SELECT DISTINCT Deltagande.student
FROM Deltagande, Kurstillfälle, Rum
WHERE Deltagande.startdatum = Kurstillfälle.startdatum
AND Deltagande.kurs = Kurstillfälle.kurs
AND Kurstillfälle.rum = Rum.id
AND Rum.namn = "Sirius"
```
***
## 7A
Ta fram personnummer, namn och telefon på studenter som har deltagit i något kurstillfälle i Jupiter!

```
SELECT DISTINCT Person.personnummer, Person.namn, Person.telefon
FROM Person, Student, Deltagande, Kurstillfälle, Rum
WHERE Person.personnummer = Student.personnummer
AND Student.personnummer = Deltagande.student
AND Deltagande.kurs = Kurstillfälle.kurs
AND Deltagande.startdatum = Kurstillfälle.startdatum
AND Kurstillfälle.rum = Rum.id
AND Rum.namn = "Jupiter"
```
***
## 7B
Ta fram personnummer, namn och ort på studenter som har deltagit i något kurstillfälle i Orion!

```
SELECT DISTINCT Person.personnummer, Person.namn, Person.ort
FROM Person, Student, Deltagande, Kurstillfälle, Rum
WHERE Person.personnummer = Student.personnummer
AND Student.personnummer = Deltagande.student
AND Deltagande.kurs = Kurstillfälle.kurs
AND Deltagande.startdatum = Kurstillfälle.startdatum
AND Kurstillfälle.rum = Rum.id
AND Rum.namn = "Orion"
```
***
## 8A
Ta fram antal kurstillfällen som varje student har deltagit i! Visa studentens personnummer, studentens namn och antalet!

```
SELECT Person.personnummer, Person.namn, COUNT(Person.personnummer)
FROM Person, Student, Deltagande, Kurstillfälle
WHERE Person.personnummer = Student.personnummer
AND Student.personnummer = Deltagande.student
AND Deltagande.kurs = Kurstillfälle.kurs
AND Deltagande.startdatum = Kurstillfälle.startdatum
GROUP BY Person.personnummer, Person.namn
```
***
### 8B
Ta fram antal kurstillfällen som varje rum har använts till! Visa rummets namn, rummets kapacitet och antalet!

```
SELECT Rum.namn, Rum.antalplatser, COUNT(Rum.namn)
FROM Rum, Kurstillfälle
WHERE Kurstillfälle.rum = Rum.id
GROUP BY Rum.namn
```
***
### 8C
Ta fram antal kurstillfällen som varje kurs har haft! Visa kursens kod, kursens namn och antalet!

```
SELECT Kurs.kurskod, Kurs.namn, COUNT(Kurstillfälle.startdatum)
FROM Kurs, Kurstillfälle
WHERE Kurs.kurskod = Kurstillfälle.kurs
GROUP BY Kurs.kurskod
```
***
### 8D
Ta fram antal kurstillfällen som varje lärare har hållit! Visa lärarens personnummer, lärarens namn och antalet!

```
SELECT Person.personnummer, Person.namn, COUNT(Kurstillfälle.lärare)
FROM Person, Lärare, Kurstillfälle
WHERE Person.personnummer = Lärare.personnummer
AND Lärare.personnummer = Kurstillfälle.lärare
GROUP BY Person.personnummer
```
***
### 8E
Ta fram antal deltagande studenter för varje kurstillfälle! Visa kurstillfällets kurskod och kursnamn, kurstillfällets startdatum och antalet!

```
SELECT Kurs.kurskod, Kurs.namn, Kurstillfälle.startdatum, COUNT(Deltagande.student) AS Antal
FROM Kurs, Kurstillfälle, Deltagande
WHERE Kurs.kurskod = Kurstillfälle.kurs
AND Kurstillfälle.kurs = Deltagande.kurs
AND Kurstillfälle.startdatum = Deltagande.startdatum
GROUP BY Kurs.kurskod, Kurs.namn, Kurstillfälle.startdatum
```
***
### 9A
I. Ta fram personnummer, namn och telefon samt antal kurstillfällen varje lärare har hållit! II. Ta fram personnummer, namn och telefon på den lärare som har hållit flest kurstillfällen! Använd lösningen av I (vyn) som källa i

**kurstillfälle_per_lärare**:
```
CREATE VIEW kurstillfälle_per_lärare AS
SELECT Person.personnummer, Person.namn, Person.telefon, COUNT(Kurstillfälle.startdatum) AS antal_kurstillfällen
FROM Person, Lärare, Kurstillfälle
WHERE Person.personnummer = Lärare.personnummer
AND Lärare.personnummer = Kurstillfälle.lärare
GROUP BY Person.personnummer 
```

**Svar:**
```
SELECT kurstillfälle_per_lärare.personnummer, kurstillfälle_per_lärare.namn, kurstillfälle_per_lärare.telefon
FROM kurstillfälle_per_lärare
WHERE antal_kurstillfällen = (SELECT MAX(antal_kurstillfällen) FROM kurstillfälle_per_lärare)
```
***
### 9B
I. Ta fram personnummer, namn och telefon samt antal kurstillfällen per student! II. Ta fram personnummer, namn och telefon på den student som har deltagit i flest kurstillfällen! Använd lösningen av I (vyn) som källa i II!

**kurstillfällen_per_student**
```
CREATE VIEW kurstillfälle_per_student AS
SELECT Person.personnummer, Person.namn, Person.telefon, COUNT(Deltagande.startdatum) AS antal_kurstillfällen
FROM Person, Student, Deltagande
WHERE Deltagande.student = Student.personnummer
AND Student.personnummer = Person.personnummer
GROUP BY Person.personnummer 
```

**Svar:**
```
SELECT kurstillfälle_per_student.personnummer, kurstillfälle_per_student.namn, kurstillfälle_per_student.telefon
FROM kurstillfälle_per_student
WHERE antal_kurstillfällen = (SELECT MAX(antal_kurstillfällen) FROM kurstillfälle_per_student)
```
***
### 10A
Ta fram personnummer, namn och ort på studenter som har deltagit i minst tre OLIKA kurser!

**genomförda_kurser_per_student**:
```
CREATE VIEW genomförda_kurser_per_student AS
SELECT Person.personnummer, Person.namn, Person.ort, COUNT(DISTINCT Kurstillfälle.kurs) AS genomförda_kurser
FROM Person, Student, Deltagande, Kurstillfälle
WHERE Person.personnummer = Student.personnummer
AND Student.personnummer = Deltagande.student
AND Deltagande.startdatum = Kurstillfälle.startdatum
AND Deltagande.kurs = Kurstillfälle.kurs
GROUP BY Person.personnummer 
```

**Svar:**
```
SELECT gkps.personnummer, gkps.namn, gkps.ort
FROM genomförda_kurser_per_student AS gkps
WHERE gkps.genomförda_kurser >= 3
```
***
### 11A
Ta fram namn och ort på personer som inte är lärare!

```

```


```

```