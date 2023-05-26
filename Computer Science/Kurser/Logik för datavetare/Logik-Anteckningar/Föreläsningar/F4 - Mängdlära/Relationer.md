#Kurs/Logik_för_datavetare #Kurs/Logik_för_datavetare/Föreläsning/4

Inom logik och matematik finns ofta ett behov av att relatera olika objekt med varandra. Detta kan användas för att skapa avbildningar eller modeller av olika typer av system.
***
#### Exempel
I en kurs kan man erhålla betyg från A till F. Studenterna Adan och Eva får betyget E respektive D. Detta kan skrivas som ett ordnat par: $( \text{Adam}, E)$ och $( \text{Eva}, D)$. Dett visar att det finns en relation mellan en student och ett betyg.
***
Produktmängden av de ingående mängderna utgör alla möjliga utfall som kan ske via relationen.

$A = \{Adam, Eva \}, B = \{A, B, C, D, E, F \}$
$A \times B = \{ (Adam, A), (Adam, B), (Adam, C), (Adam, D), (Adam, E), (Adam, F), (Eva, A), (Eva, B), (Eva, C), (Eva, D), (Eva, E), (Eva, F) \}$

En relation $R$ från en mängd $A$ till en mängd $B$ är en delmängd till $A \times B$. Paret $(x, y)$ tillhörande delmängden $R$, uttrycker att $x$ är relaterat till $y$ och detta skrivs:; $xRy$ eller $(x, y) \in  R$. 

För att beskriva att Adam och Eva fick betygen E respektive D kan vi skriva $R = {(Adam, E), (Eva, D)}

För att beskriva att Adam fick betyget E kan vi skriva $(Adam, E) \in R$ eller $\text{Adam R E}$

För att beskriva att en relation *inte* gäller skrivs således $(Adam, A) \notin R$


| |A|B|C|D|E|F|
|---|---|---|---|---|---|---|
|Adam| | | | |$\bullet$| |
|Eva| | | |$\bullet$| | |