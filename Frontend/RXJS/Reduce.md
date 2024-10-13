Der pipeable Operator `reduce` fasst alle Werte eines Streams zu einem Ergebnis unter Verwendung einer Callback Funktion zusammen. Reduce erwartet folgende Parameter:
- eine Callback-Funktion mit zwei Parameter:
	- Accumulator (Die Variable, in der das Zwischenergebnis gespeichert wird)
	- den aktuellen Wert
- den Initialwert des Accumulators