[[JavaFX]]
# Installera Java FX i Eclipse
***

1. Ladda ner Java FX från följande hemsida: https://gluonhq.com/products/javafx/. Ladda ner SDK.
2. Extrahera den nedladdade zip-filen i varfri mapp.
3. Skapa ett nytt Java-projekt i Eclipse.
4. Högerklicka på projektmappen i Eclipse och välj "Build Path" -> "Configure Build Path..."
5. Välj fliken "Libraries".
6. Klicka på "Mudulepath".
7. Klicka på "Add external JARs...".
8. Välj mappen "lib" i den mapp som du laddade ner tidigare. (exempel: javafx-sdk-18.0.1\lib)
9. Högerklicka på projektmappen i Eclipse.
10. Välj "Run As" -> "Run Configurations".
11. Välj fliken "Main".
12. I textfältet "Project"; skriv samma namn som projektmappen.
13. I textfältet "Main class"; skriv samma namn som Main-klassen i ditt projekt.
14. Välj fliken "Arguments".
15. I textfältet med titeln "VM Arguments"; klistra in någon av följande kod:
	Windows:
	```
	--module-path "C:\Program Files\Java\JavaFX\javafx-sdk-18.0.1\lib" --add-modules javafx.controls,javafx.fxml
	```

	Linux:
	```
	--module-path [SÖKVÄGEN TILL LIB-mappen] --add-modules javafx.controls,javafx.fxml
	```
	I linux kan det vara så att du måste ta bort ciatationstecknen runt sökvägen.

16. Använd följande testprogram för att testa att installationen lyckades:
	```
	import javafx.application.Application;
	import javafx.scene.Scene;
	import javafx.scene.control.Label;
	import javafx.scene.layout.FlowPane;
	import javafx.scene.layout.Pane;
	import javafx.stage.Stage;
	public class Testing extends Application{
	
		@Override
		public void start(Stage primaryStage) {
			Pane root = new FlowPane();
			
			Label label = new Label("Det funkar!");
			root.getChildren().add(label);
			
			Scene scene = new Scene(root);
			primaryStage.setScene(scene);
			primaryStage.show();
		}
		
		
		public static void main(String[] args) {
			launch(args);
		}
	}
	```