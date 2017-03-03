# Kontrollstrukturen
Um einen Programmablauf ereignisgesteuert gestalten zu können, verwendet man in Java folgende Kontrollstrukturen.
* `while(...){}`-Schleife
* `if(...){}`-Anweisung
* `for(...){}`-Schleife
* `switch(...){}`-Anweisung

---


## `while(...){}`-Schleife
Die Anweisung wird solange ausgeführt, wie die Bedingung `true` ist.
```java
while(Bedingung)
{
	Anweisungsblock
}
```

---


## `if(...){}`-Anweisung

```java
if(Bedingung)
{
	Anweisungsblock_1
}
else
{
	Anweisungsblock_2
}
```

---
# Beispiel mit `while` und `if`

```java
void fuehreAus(){
        //Farbe setzen
        while (!tastatur.istGedrueckt(' ')){           
            if (tastatur.oben()){
                tafelBunt.setzeFarbe(1,0,0);
            }
            if (tastatur.unten()){ 
                tafelBunt.setzeFarbe(1,1,0);
            }
            if (tastatur.rechts()){
                tafelBunt.setzeFarbe(1,0,1);
            }
            if (tastatur.links()){ 
                tafelBunt.setzeFarbe(0,1,0);
            }
        }
```

---



```
