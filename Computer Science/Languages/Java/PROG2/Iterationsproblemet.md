[[Iterator]]
# Iterationsproblemet
***
## F6:
#### Problem:
- Tillämpningar måste kunna gå igenom (iterera över) ina objekt för ttt utföra någon operation på varje objekt. 
- Det är bara datasamlingsklassen som kan iterera över alla objekt (vet hur de är implementerade).
- Det är bara tillämpningen som vet vilken operation som ska göras på varje objekt.

#### Lösning 1: itererbara samlingar
- Datasamlingen ger ett speciellt objekt ([[Iterator|iterator]]) som kan hålla reda på en position i samlingen och har operationer för att få fram ett objekt ur samlingen.
- Iteratorn kan flytta fram positionenoch kolla om det fins fler objekt.

#### Lösning 2
- Datasamlingen har en metod forEach som tar som argument en operation, går igenom alla objekt och utför iterationer på dem.
- Tillämpningen måste ange vad som ska göras med objekten (oftast med lambda-uttryck).

