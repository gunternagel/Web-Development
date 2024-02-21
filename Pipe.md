Pipe ist ein RXJS Operator. Er nimmt als Parameter eine unendlich große Anzahl an Functions an, welche andere RXJS- [[Pipeable Operators]] sind. Pipe wird auf ein Stream ausgeführt und gibt einen neuen Stream zurück.

Beispiel:
`pipe(
	op1(),
	 op2(),
	 op3(),
	 op4(),
	)`

Pipe wird auf einem Stream ausgeführt und die Pipeline innerhalb der Parameter werden dabei auf jedes Stream-Element ausgeführt.

Auf `pipe()` muss immer `.subscribe()` folgen!