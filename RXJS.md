RXJS besteht aus folgendem:
- [[Pipe]]
- [[Operators]]

Wissenswertes über "next, error, complete":
next fügt einen Wert zum Stream hinzu. next kann einmal oder unendlich mal oft aufgerufen werden
error ist die Fehlerausgabe. Nach error kann kein next oder complete folgen. error kann maximal nur einmal aufgerufen werden.
complete kennzeichnet das Ende des Streams. Nach complete kann kein next oder error folgen. complete kann nur maximal einmal aufgerufen werden. Wenn es gar nicht aufgerufen wird, ist der Stream endlos.

