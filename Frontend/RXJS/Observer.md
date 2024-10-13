Ein Observer ist ein Beobachter. Er beobachtet ein Observable, dass eine Quelle für den Observer repräsentiert. Ein Observer hat die drei Methoden, die vom Observable aufgerufen werden:
- next()
- error()
- complete()
Error und Complete schließen sich gegenseitig aus!!! Nach einem error kann kein complete kommen und umgekehrt!

## Die Methode next()
Die Methode **next()** nimmt den nächsten Wert entgegen und führt darauf eine Funktion aus, mit der dieser neue Wert verarbeitet wird.

## Die Methode error()
Die Methode **error()** ist die Fehlerbehandlung von diesem Observer.

## Die Methode **complete()**
Die Methode complete() wird aufgerufen, wenn alle Werte der Source verarbeitet wurden.





Wissenswertes über "next, error, complete":
next fügt einen Wert zum Stream hinzu. next kann einmal oder unendlich mal oft aufgerufen werden
error ist die Fehlerausgabe. Nach error kann kein next oder complete folgen. error kann maximal nur einmal aufgerufen werden.
complete kennzeichnet das Ende des Streams. Nach complete kann kein next oder error folgen. complete kann nur maximal einmal aufgerufen werden. Wenn es gar nicht aufgerufen wird, ist der Stream endlos.