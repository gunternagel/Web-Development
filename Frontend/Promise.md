Ein Promise ist eine Datenquelle ähnlich wie ein Observable. Ein Promise liefert nur einen Wert, ein Observable liefert eine Folge von Werten. Das Ergebnis eines Promise kann nicht von RxJS verarbeitet werden. Ein Promise stirbt, nachdem der Wert geliefert wurde. Ein Promise ist für das Pushen eines einzelnen Wertes gedacht.


Ein Promise ist so etwas wie ein Cold Observable bei RxJS. 
Ein Promise wird mit `then` abonniert:

Beispiel:
`setTimeoutPromise(1000).then((data) => {`
	`console.log(data);`
`});`


Man kann die Methode `then` verketten zu einer beliebig langen `then`-Kette. 

Ein Promise hat zwei Zustände: 
- den Wert
- Fehlerfall

**Ein Promise lebt ==NICHT== dauerhaft und ist ausschließlich exklusiv.**
