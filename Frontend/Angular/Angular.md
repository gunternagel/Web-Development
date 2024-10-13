Angular ist ein Framework zur Erstellung von SinglePageApplications basierend auf CSS, HTML und TypeScript. Es ermöglicht Oberflächen-Controls als [[Control]]-Klassen und Services als [[Service]]-Klassen zu erstellen. 

Angular-Anwendungen bestehen aus Angular [[Components]]. Components definieren Views, welche aus Oberflächenelementen bestehen und aus denen man bei Angular auswählen kann und die man nach Programmfluss und Daten verändern kann.
Components verwenden Services, welche Hintergrundfunktionalität bereitstellen, die nicht mit den Views verknüpft sind wie z.B. Daten abrufen. Diese Services können in die Components injiziert werden (Dependency Injection), was den Code modular, wieder verwendbar und effizient macht.

Components und Services sind Klassen, die mit bestimmten [Decorators](https://medium.com/google-developers/exploring-es7-decorators-76ecb65fb841#.x5c2ndtx0) markiert werden. Diese Decorators stellen Metadaten bereit, die Angular erklärt, wie diese Klassen zu verwenden sind:
- Eine Component wird immer durch Metadaten beschrieben, die 
	- ein template für die View-Beschreibung (HTML)
- Ein Service wird immer mit Metadaten beschrieben, die Angular die Bereitstellung durch Dependency Injection ermöglicht.

Ein [[Router]] verbindet die Views mit einander und ermöglicht, dass jede View eine andere URL hat, wobei die URL abhängig von den dargestellten Daten sein sollte. 

Jede Angular App hat mindestens eine Component, die root component, welche die Component Hierarchie mit dem Document Object Model (DOM) der Webseite verbindet. 

[Architektur einer SinglePageApplication mit Angular](https://angular.io/guide/architecture)


Für Angular 17 Vortrag:
[Angular 17 features](https://blog.angular.io/introducing-angular-v17-4d7033312e4b)
