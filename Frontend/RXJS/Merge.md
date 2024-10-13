Der pipeable Operator merge dient dazu, um unterschiedliche Observables zu einem gemeinsamen Observable zusammen zu fassen. Dieser Operator wird im Allgemeinen vor dem pipe-Befehl geschrieben. Merge erwartet als Parameter die zu mergenden Observables, wobei die Reihenfolge der Paarameter  die Reihenfolge der Werte im neuen Observable festlegt.

Beispiel:
`let observable1 = Observable\<Type1\>;`
`let observable2 = Observable\<Type2\>;`
`merge(observable1, observable2).pipe(`
	`...`
`).subscribe(...);`