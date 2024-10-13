Der Operator tap dient zum debuggen einer RXJS-Anweisung. Man kann mit  ihm den aktuellen Wert in der Pipe beobachten und weiterverwenden. Der Operator tap verändert nicht den Wert und ist nur zum Debuggen gedacht. Der Operator tap erwartet als Parameter eine Callback function, in der der aktuelle Wert der Pipe verarbeitet wird. Diese Verarbeitung kann z. B. log.console sein.

Beispiel:
`observable.pipe(`
	`...`
	`tap(value => console.log('foo' + value)),`
	`...`
`)`