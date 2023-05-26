#Kurs/Programmering_2 


## Exempel #Kurs/Programmering_2/Tenta
För att göra så att en instans av en klass kan läggas till i en TreeMap behöver klassen deklareras genom att implementera gränssnittet `Comparable<>`. I exempeltenta 1 görs detta på följande vis: 
```
public class Plats implements Comparable<Plats> {

}
``` 

Klassen behöver också en metod som heter `compareTo()`

```
public class Plats implements Comparable<Plats> {

		(...)

	public int compareTo(Plats other){
		if (rad < other.rad) {
			return -1;
		} else if (rad > other.rad) {
			} return 1;
		} else {
			return stol.compareTo(other.stol);
		}
	}
}
```

