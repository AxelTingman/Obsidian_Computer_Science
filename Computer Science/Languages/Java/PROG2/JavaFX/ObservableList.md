[[JavaFX]]
# ObservableList
F16
***

Exempel:
```
ObservableList<Planet> planets = FXCollections.observableArrayList(
	new Planet("Merkurius", 4879, 58, 0),
	new Planet( ...);
	new Planet( ... );
	new Planet( ... );
	new Planet( ... );
	new Planet( ... );
	new Planet( ... );
	new Planet( ... );

TableView<Planets> table = tableView<>(planets);
```
