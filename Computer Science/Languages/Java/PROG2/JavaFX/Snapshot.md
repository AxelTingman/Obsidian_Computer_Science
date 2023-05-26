#Programming/Java/Graphical_User_Interface/JavaFX 

[[JavaFX]]
# Snapshot
***



## Exempel
Från F15:
```
class SaveImageHandler implements EventHandler<ActionEvent> {
	public void handle (ActionEvent event) {
		try{
			WritableImage image = center.snapshot(null, null);
			BufferedImage bufferedImage = SwingFXUtils.fromFXImage(image, null);
		(...)
```