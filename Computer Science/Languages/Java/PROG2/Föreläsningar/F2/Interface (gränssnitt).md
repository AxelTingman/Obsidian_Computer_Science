Används istället för ärva från överordnade[[Klass|klasser]].

- Gränssnitt är en helt abstrakt [[Klass|klass]] som enbart kan
	- Deklarera abstrakta publika metoder
	- Deklarera konstanta variabler
	- Deklarera default-metoder
	- Deklarera ...
- En klass kan deklarera att den implementerar en interface
- Interface kan användas som referenstyp.
- Ett interface har inga egna instanser. En interface är därför en [[Abstrakta klasser och metoder|abstrakt klass]].

Exempel:
```
public class Ko extends Djur implements Breedable {


}
```

## Exempel
- [[Collection (datasamling)]]

## [[Designpriciper|Designprincip 1]]
För att på bästa sätt implementera gränssnitt så bör man använda designprincip 1.
