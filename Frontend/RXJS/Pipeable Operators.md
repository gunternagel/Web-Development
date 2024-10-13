Es gibt diverse Pipeable Operators, welche aneinander gekettet werden können und die Verarbeitungs-Pipeline von RXJS darstellen. Alle haben eines gemeinsam: Sie haben einen Stream als Eingang und einen neuen Stream als Ausgang. Der eingegangene Stream wird nicht verändert. Mittels den Pipeable Operatoren können dadurch Streams umgeformt werden. Wichtig ist dabei, dass die Operatoren, zwar einen Stream als Eingangsparameter haben und einen Stream als Ausgabe, aber dabei die einzelnen Werte Wert für Wert umbauen.

Pipeable Operatoren sind:
- [[Concat]]
- [[Distinct]]
- [[DistinctUntilChanged]]
- [[Filter]]
- [[Map]]
- [[Merge]]
- [[MergeAll]]
- [[Range]]
- [[Reduce]]
- [[Skip]]
- [[SkipLast]]
- [[Take]]
- [[TakeLast]]
