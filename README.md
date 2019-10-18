# javafx-splash-screen
JavaFX Splash Screen

**Motivation**  
- Feedback an den Benutzer, dass Anwendung noch lädt
	- Wichtig für Anwendungen die viel I/O am Anfang haben
	- Webanwendungen
- Welcome experience
	- Präsentation des Brand Designs
- Kann benutzt werden um Anmeldedaten abzufragen

**Bestandteile eines Splash Screens**  
- Firmenname oder -logo
- Produktname oder -logo
- Brand Design
- Ladeindikator
- (Anmeldeformular)

**Implementierung**
- Jeder Implementierung eines Preloaders muss von der Preloader Klasse erben
	- Preloader erbt von Application und muss deswegen eine start(Stage stage)-Methode implementieren
- Zum Aufrufen des Preloaders gibt es 2 Möglichkeiten:
	- LauncherImpl.launchApplication(Application.class, Preloader.class, args)
		- Wird impliziet von launch(args) aufgerufen (Preloader = null)
	- Setzen der Umgebungsvariable javafx.preloader
- Es wird erst der Preloader gestartet, ist dieser geladen wird die Anwendung gestartet