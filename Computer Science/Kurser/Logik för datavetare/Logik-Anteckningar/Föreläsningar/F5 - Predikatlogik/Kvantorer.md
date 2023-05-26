#Kurs/Logik_för_datavetare 

Men även med en tolkning som $T$ ovan går det inte att avgöra om t.ex. $p(x) \lor q(f(y))$ är sann eller inte. Vi vet ju ingenting om $x$ och $y$. Men givet en tolkning kan vi ta reda på om $p(x) \lor q(f(y))$ är sant för alla $x$ eller $y$, eller för något $x$ eller $y$.

$\forall$, allkvantorn, utläses "för alla" och $\exists$, existenskvantorn, "det finns".

$\exists x \forall y (p(x) \lor q(f(y)))$ betyder att det finns ett exement $x$ så att för alla $y$ är sant  att $p(x) \lor q(f(y))$.

#### Exempel
$K(x)$ = $x$ är en katt
$L(x)$ = $x$ är lat

|Naturligt språk|Logiskt språk|
|---|---|
|Alla katter är lata|$\forall x[K(x) \to L(x)]$|
|Det finns en lat katt|$\exists x [K(x) \land L(x)]$|
|Inte alla katter är lata|$\exists x [K(x) \land \neg L(x)]$|
|Det finns inga lata katter|$\neg \exists x[K(x) \land L(x)]$|



