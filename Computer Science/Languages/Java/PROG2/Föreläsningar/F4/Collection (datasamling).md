#Kurs/Programmering_2/Föreläsning/2  #Kurs/Programmering_2/Föreläsning/4 

Ett [[Interface (gränssnitt)|gränssnitt]] och supertyp för [[List]], [[Set (mängd)]] och [[Map (avbildning)]].

- Rotklass för samtliga samlingar
- Har metoder för att lägga till, ta bort och kontrollera existens av objekt
- Iterera över objekten i samlingen med en [[Iterator|iterator]].
- Returnerar [[Ström (stream)|strömmar]].
- Returnerar [[Array|array]] av samlingen

## Operationer
- `sort(List)`
- `reverse(List)`
- `shuffle(List)`
- `max(Collection)`
- `min(Collection)`




## I Javas standardbibliotek
Exempel på generiska [[Klass|klasser]]:
- [[ArrayList]]
- [[TreeSet (trädmängd)]]
- [[HashMap (hashavbildning)]]
- [[TreeMap (trädavbildning)]]

Gränssnitt:
- [[Collection (datasamling)]] (alla)
- [[List]] (listor)
- [[Set (mängd)]] (mängder)
- [[Map (avbildning)]] (avbildningar)

#Kurs/Programmering_2/Föreläsning/4 
## Gränssnitt: 
[[Collection (datasamling)]]

#### Funktioner
- Ta bort element: `add(E e)
- `addAll(Collection<? extends E> c)
- Ta bort element `remove(E e)`
- Kontrollera om element finns: `contains(E e)`
- Kontrollera om listan är tom: `isEmpty`
- Iterera, ex. med `for(E e : coll)`: `Iterator<E> iterator()`
- Skapa array: `toArray()` eller `toArray(E[] a)`

## Olika typer
Det finns tre typer av datasamlingar som vardera har sina egna särskilda syften:
- [[List]]
- [[Set (mängd)]]
- [[Map (avbildning)]]

## Datasamlingsoperationer
Operationer på datasamlingar samlas i klassen Collections:
- `sort(List)`
- `reverse(List)`
- `shuffle(List)`
- `max(Collection)`
- `min(Collection)`

Metoder för arrayer i klassen Arrays:
- `sort(Object[])`
- `sort(int[])`
- `sort(double[])`
