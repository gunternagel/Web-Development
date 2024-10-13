Eine Angular Component definiert eine Klasse, welche Daten und Anwendungscode enthält und welche mit einem HTML-Template verknüpft ist, die die zugehörige View definiert, mit der diese Daten dargestellt werden sollen.

Eine Component wird mit dem `@Component()` Decorator dekoriert, welcher die direkt nachfolgende Klasse als Component markiert. damit das System weiß, was diese Klasse bedeutet und wie sie funktionieren soll.

## Templates, Directives und Data Binding
Ein Template ist HTML Code, welcher durch Angular Markups angereicht ist. Die Angular Markups können HTML-Elemente modifizieren bevor der HTML-Code angezeigt wird. Template Direktives stellen Programmlogik in der UI bereit und Binding Markups verbindet die Application Daten mit dem DOM. Es gibt zwei Arten der Datenbindung:
- [[Event binding]]
- [[Property binding]]
Bevor eine View angezeigt wird, wertet Angular die vorhandenen Directives aus und verwendet die Binding Syntax, um die vorhandenen HTML-Elemente und den DOM nach der Programmlogik und den aktuellen Daten zu verändern. Angular ermöglicht two-way-Data-Binding, was bedeutet, dass vom Anwender vorgenommene Änderungen im DOM auch in die Programmdaten zurück gespiegelt werden.

Die Templates können [[Pipes]] verwenden, um das Anwendererlebnis zu verbessern, in dem die anzuzeigenden Werte für die Anzeige transformiert werden. Zum Beispiel werden Pipes verwendet um Datumswerte und Währungswerte an die lokalen Einstellungen des Anwenders anzupassen. Angular stellt vordefinierte Pipes für Standardtransformationen bereit. Außerdem kann man auch eigene Pipes definieren.

[Weiteres hier](https://angular.io/guide/architecture-components)
