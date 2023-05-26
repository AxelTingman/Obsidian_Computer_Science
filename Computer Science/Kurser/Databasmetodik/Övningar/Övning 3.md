#Kurs/Databasmetodik #Kurs/Databasmetodik/Övning 

![[ö3a.png]]

Bokverk(titel)
Författare(<u>namn</u>, <u>titel</u>) Författare.titel är FN mot Bokverk.titel
Tryckbok(löpnummer, antalSidor, bokverk) Tryckbok.bokverk är FN mot Nokverk.titel
Inbunden(trådtyp, pärmmaterial, löpnummer, bokverk) Inbunden.(löpnummer, bokverk) är FN mot Tryckbok.(löpnummer, bokverk)

![[ö3b.png]]

#### Bokverk
|titel |
|:---|
|LOTR|
|Stiftelsen|
|DBMS 101|
|Dune|

#### Författare
(...)


![[ö3c.png]]

Land(landsnamn)
Stad(<u>Stadnamn</u>, land); Stad.land är FN mot Land.landsnamn
Vänort(Sn1, L1, Sn2, L2); Vänort.(Sn1, L1) är FN mot Stad.(stadnamn, land); Vänort(Sn2, L2) är FN mot Stad.(stadnamn, land)
Kung(kunganamn, land far) Kung.land är FN ot land.landnamn;  Kung.far är FN mot Kung.byggnad