#Kurs/Programmering_2/Föreläsning/6 

- "Konverteras" till ett interface.
- Functional interface (interface med en abstrakt metod).
- Kan nå variabler deklarerade i ett omgivande scope som är "effectively final" eller final

En iterator kan utföra metoder eller operationer på element i en lista genom lambdauttryck:
`iterator.forEach(object -> System.out.print(o));

### Prog 2, Föreläsning 17:
Ett sätt att anropa en [[Metod|metod]], till exempel i samband med att användaren trycker på en knapp.

Exempel (F17):
```
four.setOnAction((e) -> {
	System.out.println("Three");
}

```