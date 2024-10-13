Map ist ein pipeable Operator, welcher die Werte eines Streams umformen kann. Map wird auf einen Stream ausgeführt und gibt einen Stream zurück. Map erwartet eine Callback-Funktion, mit welcher die einzelnen Werte eines Streams umgeformt werden sollen.

Beispiel:
`observable.map(x => x * 10)   //multipliziert jeden Wert im Stream mit 10`  