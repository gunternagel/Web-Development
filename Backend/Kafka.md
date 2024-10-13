Kafka ist ein Service, um Messages weiterzuleiten. Dabei ist für Kafka das Format der Messages unwichtig. Sie werden als Byte-Array behandelt und nur Versender und Empfänger kennen das genaue Format. 
Messages werden in Gruppen von Messages mit gleichem Topic und Partition weitergeleitet, um einen möglichst kleinen Overhead zu generieren und Kafka nimmt in Kauf, dass dadurch eine gewisse Latenz entsteht. 







