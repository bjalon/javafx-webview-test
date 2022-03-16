* Installer 
  * le [JDK 11 (hotspot)](https://adoptopenjdk.net/) si vous ne l'avez pas
  * le [JavaFX 11 SDK](https://gluonhq.com/products/javafx/)
* Dans IntellIJ IDEA, dans le menu project structure > Project Settings > Project remplacez le project sdk par la version 11 et le project language level par 11 également. Faites de même dans Platform Settings > SDKs.
* Lancer le `main` de la classe `KEOSSimpleWebViewTest`
* Si l'exception suivante s'affiche :

```
Erreur : des composants dex�cution JavaFX obligatoires pour ex�cuter cette application sont manquants.
```

* Ajouter dans la configuration du run Intellij les JVM Options suivantes :

```
--module-path=%PATH_INSTALLATION_JAVAFX%\javafx-sdk-11.0.2\lib --add-modules=javafx.controls,javafx.fxml,javafx.swing,javafx.base,javafx.web,javafx.graphics,javafx.media
```

* Dans le fichier KEOSSimpleWebViewTest remplacer l'url ou le fichier racine à charger ligne 29