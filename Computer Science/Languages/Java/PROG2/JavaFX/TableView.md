[[JavaFX]]
# TableView
F16
***
Presenterar data i tabellform.

Exempel:
```
ObservableList<Planet> planets = FXCollections.observableArrayList(
	new Planet("Merkurius", 4879, 58, 0),
	new Planet( ... );
	new Planet( ... );
	new Planet( ... );
	new Planet( ... );
	new Planet( ... );
	new Planet( ... );
	new Planet( ... );

TableView<Planets> table = tableView<>(planets);
```

## Kolumner
Det finns olika sätt att skapa kolumner.

Exempel A:
```
TableColumn<Planet, String> c1 = new TableColumn<>("Namn");
c1.setCellValueFactory(new PlanetNameCellFactory());

class PlanerNameCellFactory
	implements Callback<TableColumn.CellDataFeatures<Planet, String>, ObservableValue<String>>{
	
	@Override 
	public ObservableValue<String>
		call (TableColumn.CellDataFeatures<Planet, String> cell) {
			return new SimpleStringProperty(cell.getValue().getName());
		}

TableColumn<Planet, Integer> c2 =) new TableColumn<>("Diameter");
c2.setCellValueFactory(cell -> new ReadOnlyObjectWrapper<>(cell.getValue().getDiameter()));

TableColumn<Planet, Integer> c3 =) new TableColumn<>("Avstånd");
c3.setCellValueFactory(cell -> new ReadOnlyObjectWrapper<>(cell.getValue().getDiameter()));

TableColumn<Planet, Integer> c4 =) new TableColumn<>("Månar");
c4.setCellValueFactory(cell -> new ReadOnlyObjectWrapper<>(cell.getValue().getDiameter()));

table.getColumns().addAll(c1, c2, c3, c4);
```

## Fylla en TableView med data
Tabellen kan skapas med sin data:
```
ObservableList<Planet> planet = FXCollections.observableArrayList( ... );
TableView<Planet> table = new TableView<>(planets);
```

Man kan även sätta in data i en redan existerande tabell:
```
table.setItems(planets);
```

Vill man göra ändringar i dessa data så ska de göras i listan varvid `TableView` uppdateras automatiskt:
```
planets.add("Pluto", 2300, 5910, 5);
```

`Tableview.getItems()` returnerar en ObservableList.

## Hantera val i TableView
Selektionen sköts av `TableView.selectionModel`:
```
Planet vald = table.getSelectionModel().getSelectedItem();
ObservableList<Planet> valda = table.getSelectionModel().getSelectedItems();
```

Man kan också ta fram index för valda alaternativ:
```
int pos = table.getSeöectionModel().getSelectedItem();
ObservableList<Integer> poses = table.getSelectionModel().getSelectedIndices();
```

Man kan även inifrån programet sätta det utvalda värdet:
```
table.getSelectionModel().select(3);
```

Avmarkering av selektionen:
```
table.getSelectionModel().clearSelection();
```
