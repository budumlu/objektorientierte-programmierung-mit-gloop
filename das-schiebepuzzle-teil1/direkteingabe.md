# 3.2 Direkteingabe

Das Schiebepuzzle, dass eben noch auf Papier ausgedruckt gespielt wurde,soll nun mit dem Code-Editor BlueJ programmiert und gesteuert werden. Dieser Editor bietet eine _Direkteingabe_ an \(-&gt; Ansicht oder Strg + E\). Dort kann zunächst mit dem Befehlsaufruf

```java
new GLOOP.GLKamera(600,400)
```

eine Kamere erzeugt werden,die einen Blick in die _GLOOP-Welt_ erlaubt. Um ein bißchen mehr Orientierung zu bekommen ist es hilfreich, mit der GLKamera-Methode `zeigeAchsen(true)`die x- und y-Koordinatenachsen anzeigen zu lassen. Um Die Kamera ansprechen zu können,muss diese zunächst einen Namen \(_Referenzierung_\) bekommen. Dazu muss das kleine rote Icon in das Feld links neben die Direkteingabe gezogen werden, wie es bereits in der unten stehenden Abbildungen bereits vollzogen worden ist.

![](/assets/Direkteingabe_1.png)

## Aufgabe

Programmieren Sie nun, wie in den Screenshots zu sehen, das Schiebepuzzle zu Ende. Um die Tafeln auch beschriften zu können, muss darauf geachtet werden, dass die Datei `Zeichen.png` im Projektordner abgespeichert wurde. Mit der `verschiebe`-Methode aus dem Kapitel [Unplugged](/das-schiebepuzzle-teil1/unplugged.md) können die Objekte vomTyp `GLTafel` auch verschoben werden.

![](/assets/Direkteingabe_2.png)

![](/assets/Direkteingabe_3.png)

