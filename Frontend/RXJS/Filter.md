Filter ist ein pipeable Operator, welcher zum Filtern von Werten eines Streams dient. Filter erwartet als Parameter eine Callback-Funktion, in der gefiltert wird.

[Learnrxjs Filter](https://www.learnrxjs.io/learn-rxjs/operators/filtering/filter)
[rxjs.dev Filter](https://rxjs.dev/api/operators/filter)

![[Pasted image 20240224202648.png]]

`// RxJS v6+
import { from } from 'rxjs';
import { filter } from 'rxjs/operators';

//emit (1,2,3,4,5)
const source = from([1, 2, 3, 4, 5]);
//filter out non-even numbers
const example = source.pipe(filter(num => num % 2 === 0));
//output: "Even number: 2", "Even number: 4"
const subscribe = example.subscribe(val => console.log(`Even number: ${val}`));`