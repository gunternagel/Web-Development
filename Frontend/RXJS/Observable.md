Ein Observable kann man sich als Gegenstück zu einem Array vorstellen. Anstatt die Daten zu behalten, gibt es Datenströme / Streams an interessierte Abonnenten ([[Observer]]) weiter.
Ein Observable ist erst aktiv, wenn es mit der **subscribe**-Funktion abonniert wird!
Deshalb ist ein Observable eine lazy Push Collection aus mehreren Werten. Es stellt also, sobald ein Wert dem Observable zur Verfügung steht, dem Observer zur Verfügung und informiert diesen über den Aufruf der Next-Funktion des Observers. 
Wenn ein Observer nicht mehr ein Observable abonnieren will, muss der Observer das Observable unsubscriben. Alle Observer müssen vor der Vernichtung durch den Garbage Collector das Observable unsubscriben!!!

Ein Observable ist unicast, sprich es kann nur einen Observer mit Daten versorgen.

Die Ergebnisse eines Observables können von RxJS-Operatoren verarbeitet werden. Ein Observable kann deutlich länger leben als ein Promise - nämlich so lange, wie es subscribed ist. ein Observable ist für ein dauerhaftes Leben gedacht - um eine Folge von Werten zu pushen.

Ein Observable hat drei Zustande, die mittels eines Objektes verwaltet werden:
- der Wert (next)
- Ende der Folge (complete)
- Fehlerfall
## Die subscribe-Funktion
Die subscribe-Funktion erwartet eine Callback-Funktion als Parameter. Diese erhält die Daten vom Observable über die Parameter.

Beispiel:
`observable.subscribe(x => console.log(x*x));`

Dabei ist x der Parameter. `console.log(x*x)` ist die Callback-Funktion.

`subscribe` kann nicht verkettet werden mit folgenden `subscribe`-Aufrufen von anderen Observables.

Ein Observable lebt erst durch den Aufruf des subscribe. 

## Die unsubscribe-Funktion
Die unsubscrib-Funktion stoppt ein Observable. Dadurch wird das Observable wieder frei gegeben. Wenn es keine Subscriptions auf ein Observable gibt, wird es für den Garbage Collector frei gegeben.

## Was stoppt alles ein Observable?
Was stoppt alles ein Observable?:

- Aufruf der Methode `unsubscribe()`
- Bestimmte Operatoren können ein Observable beenden wie
	- takeWhile
	- takeUntil
- Exception wird ausgelöst
- ein `complete()` wird ausgelöst

## Cold Observable / Hot Observable
Ein cold Observable ist ein Observable bei dem einzelne jede Observable-Instanz von einem jeweils einzigen Observer abonniert wird. Es gibt keine zwei Observer pro Observable-Instanz.
Bei hot Observables gibt es mehrere Observer-Instanzen, die sich eine Observable-Instanz teilen. Man kann nur mit einem Subject ein hot Observable bauen.

![[Pasted image 20240306200226.png]]