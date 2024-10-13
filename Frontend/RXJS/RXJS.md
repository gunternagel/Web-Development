## Allgemeines
RXJS dient zum Bau von Programmen für reaktive Funktionen, um asynchron empfangene Daten zu verarbeiten. Man kann damit Streams/Daten vom Observer Datenpaket für Datenpaket einzeln verarbeiten.

Verwendet [Observer-Entwurfsmuster](https://de.wikipedia.org/wiki/Beobachter_(Entwurfsmuster)).

Reaktive Programmierung führt dazu, dass reaktiver Code erst dann aktiv wird, wenn eine bestimmte Bedingung erfüllt ist.

## Bestandteile
RXJS besteht aus folgendem:
- [[Pipe]]
- [[Operators]]
- [[Observable]]
- [[Observer]]


Zusammenhang zwischen Observer, Observable, Pipe und Operators:
Ein Observer subscribed ein Observable. Das Observable ruft bei Auftreten neuer Werte die Observer-Methode next auf und übergibt die neuen Werte im Parameter. Zwischen Observable und Observer kann bei Bedarf eine Pipe geschaltet werden, welche das Observable wertweise anpasst. Wenn der Observer nicht mehr die Daten vom Observable empfangen soll, muss das Observable unsubscribed werden.
## RXJS debuggen
Um eine RXJS-Anweisung zu debuggen, drückt man im Browser *F12* um die Entwicklertools des Browsers aufzurufen. Dann fügt man den pipeable Operator [[Tap]] zur Pipe hinzu.



[Video von Gregor Biswanger](https://www.youtube.com/watch?v=jehhUUL88GM)

[RxJS-Spiel](www.rxjs-fruits.com.md)


