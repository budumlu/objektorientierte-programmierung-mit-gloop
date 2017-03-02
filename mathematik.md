#Vergleichsoperatoren

| Operator            | Beschreibung   | Mögliche Datentypen  |Beispiel |
| --------------- | -------- | --------- | --------- |
| `==`   |ist gleich          | alle  | `a==true` | 
| `!=`   |ist ungleich        | alle     | `4.23!=5.65` | 
| `>`    |größer als          | alle, bis auf boolean  | `'d'>'b'`  |
| `<`    |kleiner als         | alle, bis auf boolean |    `1<2`       |
| `>=`   |größer oder gleich  | alle, bis auf boolean  | `b>=e` |
| `<=`   |kleiner oder gleich | alle, bis auf boolean |  `banane<=apfel`  | 


#Die Klasse *Math*
| Methode   | Beschreibung  |Beispiel |
| -------- | --------- | --------- |
|`int round(float a)`          | Gibt die nächste Ganzzahl von a zurück.  | `Math.round(3.422)`gibt: 3; `Math.round(3.5)`gibt: 4 | 
|`double sqrt(double a)`      | Gibt die Quadratwurzel der Zahl a zurück. sqrt gibt square root.     | `Math.sqrt(36)`gibt: 6 | 
|`double pow(double a, double b)`          | Gibt den Wert der Potenz $$a^b$$ zurück.  | `Math.pow(2,3)` gibt: 8  |
|`double random()`       | Erzeugt eine Zufallszahl größer oder gleich 0.0 und kleiner als 1.0. Durch Multiplikation und Addition kann der Bereich entsprechend angepasst werden. |    `Math.random()*5+10` gibt ein x mit 10.0<=x<15.0       |




