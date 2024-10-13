Der distinctUntilChanged Operator ist ein pipeable Operator, welcher aus einem Stream nur den ersten von einer Werte-Folge mit gleicher Wertigkeit übernimmt und erst dann wieder einen Wert übernimmt, wenn sich die Wertigkeit geändert hat.

Beispiel:
`observable = from([1,1,1,3,3,1,1,1,2]);`
`obserable.pipe(`
	`distictUntilChanged()`
`).subscribe(value => console.log(value));`
*Ergibt: 1, 3, 1, 2*

