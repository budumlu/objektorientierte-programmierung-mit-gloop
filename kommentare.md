# Kommentare
Alle Informationen, die nicht für den eigentlichen Programmablauf wichtig sind, müssen auskommentiert werden.

Kommentare werden häufig dazu genutzt, um den eigentliche Quellcode zu erläutern, so dass er beim Lesen verständlicher ist

In Java gibt es zwei verschiedene Weisen, wie Kommentare in Dateien kenntlich gemacht werde:

* Die Zeile beginnt mit `//`:

```java
// Die ist ein Kommentar, der den Quellcode erläutern soll
int a = pA;
```

* Ein Abschnitt, der einen Kommentar enthält startet mit `/*` und endet mit `*/`:

```java
/*
Die ist ein Kommentar,
der über mehrere Zeile geht.
*/
int a = pA;
```


---

{% exercise %}
Markiere den Inhalt als Kommentar

{% initial %}
Markiere mich als Kommentar!
Ansonsten wird ein Error ausgeworfen!

{% solution %}
/*
Markiere mich als Kommentar!
Ansonsten wird ein Error ausgeworfen!
*/

{% validation %}
assert(true);


{% endexercise %}




---