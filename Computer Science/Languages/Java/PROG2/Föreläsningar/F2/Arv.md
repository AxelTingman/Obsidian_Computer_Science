Innebär att [[Klass|klasser]] ärver attribut från en annan, föräldraklass (supertyp).

Exempel:
```
public class Human extends Mammal {
}
```

## Nackdelar med arv
Från F2:
- Koden riskeras att dupliceras mellan subklasser
- Förändringar av beteende under körning försvåras
- Svårt att få kännedom om samtliga bettenden
- Änder kan inte flyga och kvacka samtidigt
- Förändringar kan oavsiktligt påverka andra änder

Vissa barnklasser kan ärva oönskvärda attribut från föräldraklassen.

Barnklasser kan bara ha en föräldraklass.

När arv implementeras bör de följa [[Designpriciper|tre designprinciper]].

## Alternativ till arv
Istället för arv så kan man använda sig av [[Interface (gränssnitt)|interfaces]] som kan implementera (ärva) attribut från flera olika klasser.

Både fåglar och flygplan kan flyga, men det vore fel att säga att flygplan *är en* fågel för att implementera att de båda kan flyga. Istället är det bättre att implementera ett gränssnitt som heter *flygbar* som anger alla egenskaper som behövs för objekt som kan flyga.


