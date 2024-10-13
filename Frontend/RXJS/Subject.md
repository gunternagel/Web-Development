Ein Subject ist eine Kombination aus Observable und Observer.
Ein Subject ist ein Multicast Observable.

Ein Subject ist ein erweitertes Observable. Es implementiert zusätzlich noch das Interface `SubscriptionLike`:
![[Pasted image 20240306192645.png]]



Beispiel:
`const  subject = new Subject();`

`subject.subscribe(data => console.log('Observer1: ' + data));`

`subject.next(1);`
`subject.next(2);`
`subject.next(3);`

`subject.subscribe(data => console.log('Observer2: ' + data));`

`subject.next(4);`
`subject.next(5);`
`subject.next(6);`

Ergibt:
![[Pasted image 20240306192959.png]]

Bei einem normalen Subject wird gerade aktuelle Wert an die Observable geliefert. 

## BehaviorSubject
Das BehaviourSubject cached den zuletzt gelieferten Wert für den/die nächsten subscribenden Observer. Beim ersten Observer wird nichts geliefert. Dieses Subject behält diesen Cache nur für kurze Zeit!!!

## ReplaySubject
Das ReplaySubject erwartet im Constructor-Parameter die Anzahl der zu cachenden Werte und liefert diese bei einem neu erfolgten Subscribe an den Observer bevor der nächste aktuelle Wert geliefert wird. Dieses Subject behält diesen Cache nur für kurze Zeit!!!

## AsyncSubject
Das AsyncSubject liefert nur den letzten Wert, wenn `complete` oder `error` aufgerufen wird. Ansonsten wird kein einziger Wert geliefert!!!
