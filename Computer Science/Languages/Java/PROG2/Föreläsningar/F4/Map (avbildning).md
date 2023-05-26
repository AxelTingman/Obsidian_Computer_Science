Supertyp för [[HashMap (hashavbildning)]] och [[TreeMap (trädavbildning)]].

Ärver inga funktioner från collections.

Fungerar som en array men kopplar nycklar till värden i elementen istället för index.

Har metoder för att hämta, lägga till, ta bort enligt en given nyckel. Kan även iterera över nycklar, värden eller nyckel-värde-par.

## Metoder
- Lägg till: `put(Key k, Value v)`
- `putAll(Map<? extends K, ? extends V> o)`
- Ta bort par: `remove(Object k)`
- Iterera:
	- `keySet()`
	- `values()`
	- `entrySet()`