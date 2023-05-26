#Kurs/Databasmetodik/Lektion/5
⋈
## R2
π kurskod, kursbenämning( σ längd = 4 AND pris > 4000 KURS)

***

## R3
1. Rättkurstillfällen <- σ lokal = 'Jupiter' Ktillf
2. Rättkurser <- Kurs ⋈ kurskod=kurs Rättkurstillfällen
3. π kursben, pris Rättkurser

## R4
***Ta fram namn och adress på elever som har gått kurs för Sofia Wilsson!***
1. RättLärare(lärare) <- π lid σ lnamn = 'Sofia Wilson' LÄRARE
2. RättKtillf <- Ktillf ⋈ Rättlärare
3. RättDeltagare  <- Deltag ⋈ RättKtillf
4. RättElev <- Elev ⋈ eid = elev RättDeltagare
5. Svar <- π enamn, adress RättElev


π enamn, adress (  Ktillf ()