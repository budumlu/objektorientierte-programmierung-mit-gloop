#Primitive Datentypen
In Java ***eingebaute*** Datentypen:
* Ganze Zahlen: `byte, short, int, long`
* Gleitkomma (Reelle-) Zahlen: `float, double` 
* Zeichen: `char`
* Wahrheitswerte: `boolean (true/false)`


#Werte von primitive Datentypen

| Typname            | Größe   | Wertebereich  |Default-Werte |
| --------------- | -------- | --------- | --------- |
| boolean  |undefiniert (1 bit)          | true/false  | `false` | 
| char   |16 bit        | 0 ... 65.535 (z. B. 'A')     | `null` | 
| byte   |8 bit          | -128 ... 127  | `0`  |
| short   |16 bit         | -32.768 ... 32.767 |    `0`       |
| int  |32 bit  | -2.147.483.648 ... 2.147.483.647  | `0` |
| long   |64 bit         | $$-2^{63}$$ bis $$2^{63}-1$$, ab Java 8 auch 0 bis $$2^{64} -1$$ |    `0L`       |
| float  |32 bit  | +/-1,4E-45 ... +/-3,4E+38  | `0.0f` |
| double  |64 bit  | +/-4,9E-324 ... +/-1,7E+308  | `0.0d` |

