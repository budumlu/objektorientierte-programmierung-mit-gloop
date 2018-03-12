# 2.2 Klassen-/Methodenübersicht zu GLOOP

Im Folgenden wird eine kurze Übersicht über die Grundlagen der Verwendung von GLOOP-Objekten und GLOOP-Methoden gegeben. Diese Übersicht dient dazu, wichtige Grundlagen von GLOOP schnell nachschlagen zu können. Der eigentliche Lehrgang beginnt im Kapitel [Das Schiebepuzzle Teil 1](/das-schiebepuzzle-teil1.md).

Eine vollständige Übersicht über die Java-Bibliothek **GLOOP** ist [hier](http://www.schulentwicklung.nrw.de/cms/upload/gloop/dokumentation/Komplettuebersicht_GLOOP_3.7.pdf "Komplettuebersicht\_GLOOP\_3.7") verlinkt.

## Einbindung der GLOOP-Bibliothek

Um GLOOP-Objekte erzeugen zu können, müssen die GLOOP-Bibliotheken importiert werden.

```java
import GLOOP.*;
```

## Kameraklassen

Um einen Blick in die GLOOP-Welt zu ermöglichen muss eine Kamera erzeugt und instanziiert werden. Im Beispiel wird eine Kamera mit einem Sichtfeld von 800 mal 600 Pixeln erzeugt und mit der Methode `setzePosition`ihre Position auf die Werte x=0, y=300 und z=500 verändert.

```java
kamera = new GLKamera(800,600);     
kamera.setzePosition(0,300,500);
```

Im nächsten Beispiel sind Kameras, deren Blickwinkel mit der Maus verändert werden können, zu sehen.

```java
kamera = GLEntwicklerkamera(); //Im Vollbildmodus.
kamera.setzeStereomodus(true); //Für Streoskop-Brillen
kamera.zeigeAchsen(true);
 //Blendet die Koordinatenachsen im Kamerabild ein. Dies hilft häufig bei der Orientierung im Raum.
```

## Himmel, Boden und Licht

Auf folgende Weise rufen Sie die wichtigsten Grafikklassen auf:

```java
licht    = new GLLicht(); 
himmel   = new GLHimmel("Himmel.jpg");
boden    = new GLBoden("Boden.jpg");
```

## Unterklassen von GLObjekt

Häufig werden Quader, Kugel, Kegel usw. benötigt, um eine GLOOP-Welt zu gestalten. Die wichtigesten Klassen und Methoden sind in einer kurzen Übericht [hier](http://www.schulentwicklung.nrw.de/cms/upload/gloop/dokumentation/Grundlagenuebersicht_GLOOP_3.7.pdf "Grundlagenuebersicht\_GLOOP\_3.7") verlinkt.

```java
//Die folgende Kugel wird an Position (0,0,0) mit dem Radius von 20 Pixeln erstellt.
kugel = new GLKugel(0,0,0,20);

//Ein Torus mit dem Radius 120 und der Dicke 10. Die ersten drei Werte geben wieder die Position des Ringes an.
ring = new GLTorus(-280,70,0, 120,10);
```

Für das Schiebepuzzel haben Sie bereits Tafelobjekte eingesetzt. Sie sind aber auch gut geeignet, um eine Spielanleitung einem Spieler zur Verfügung zu stellen.

```java
tafel = new GLTafel(0,100,300,200,15);
tafel.setzeText("Triff das Ziel!!!",10); //Schriftgröße 10
```

# Manipulieren mit GLOOP-Methoden

GLOOP-Objekte können verschoben werden, man kann ihre Farbe verändern oder ihre Größe manipulieren. Um Objekte zu manipulieren benötigt man Methoden, mit denen man auf die Attribute der Objekte verändern kann.

## Bewegen und Färben

```java
//Dreht das Objekt um durch den Mittelpunkt des Objektes gehende Parallelen der Koordinatenachsen.
void drehe(double pWX, double pWY, double pWZ)
//Dreht das Objekt um durch den Punkt (pX,pY,pZ) gehende Parallelen der Koordinatenachsen.
void drehe(double pWX, double pWY, double pWZ, double pX, double pY, double pZ)  

//Liefert die entsprechende Koordinate des Mittelpunktes des Objekts.
double gibX()
double gibY()
double gibZ()

//Setzt das Objekt an die angegebene Position.
void setzePosition(double pX, double pY, double pZ)

//Das Objekt kann durch angabe von drei Werten entlang der x-,y- und z-Achse verschoben werden.
void verschiebe(double pX, double pY, double pZ)

//Texturen werden häufig verwendet, um Objekt ansprechender zu gestalten. Die jpg- oder png-Datei muss im Projektordner liegen. 
void setzeTextur(String pDateiname)

//Färbt das Objekt ein. pR = Rotanteil, pG = Grünanteil, pB = Blauanteil
void setzeFarbe(double pR, double pG, double pB)
```

## Tastatur- und Mauseingaben

```java
tastatur = new GLTastatur();
```



