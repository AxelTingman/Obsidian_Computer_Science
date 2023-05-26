#Kurs/Programmering_2 

[[Behållare]]
# GridPane
***
Använder inte `getChildren()`, utan anropar en add-metod istället.

Rutorna behöver inte vara lika stora och kan även utelämnas.

#### Exempel:
```
GridPane root = new GridPane();

root.add(new Button("0"), 0, 0);
root.add(new Button("1"), 1, 0);
root.add(new Button("2"), 2, 0);
root.add(new Button("3"), 0, 1);
root.add(new Button("4"), 1, 1);
root.add(new Button("5"), 2, 1);
root.add(new Button("6"), 0, 2);
root.add(new Button("7"), 2, 2);

Scene scene = new Scene(root);
primaryStage.setScene(scene);
primaryStage.show();
```

Resultat:

![[f11_gridpane.png]]