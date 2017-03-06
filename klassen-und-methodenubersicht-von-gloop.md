# GLOOP-Objekte
Im Folgenden wird eine kurze Übersicht über die Grundlagen der Verwendung von GLOOP-Objekten und GLOOP-Methoden gegeben.

Eine vollständige Üersicht finden Sie [hier](http://www.schulentwicklung.nrw.de/cms/upload/gloop/dokumentation/Komplettuebersicht_GLOOP_3.7.pdf "Komplettuebersicht_GLOOP_3.7") verlinkt.

##Einbindung der GLOOP-Bbliothek
Um GLOOP-Objekte erzeugen zu können, müssen die GLOOP-Bibliotheken importiert werden.
```java
import GLOOP.*;
```

## Kameraklassen
Um einen Blick in die GLOOP-Welt zu ermöglichen muss eine Kamera erzeugt und instanziiert werden. Im Beispiel wird eine Kamera mit einem Sichtfeld von 800 mal 600 Pixeln erzeugt und ihre Position auf die Werte x=0, y=300 und z=500 verändert.
```java
kamera = new GLKamera(800,600);     
kamera.setzePosition(0,300,500);
```
Im nächsten Beispiel sind Kameras, deren Blickwinkel mit der Maus verändert werden können, zu sehen.

 ```java
kamera = GLEntwicklerkamera(); //Im Vollbildmodus.
kamera.setzeStereomodus(true); //Für Streoskop-Brillen
  
 ``` 

##Himmel, Boden und Licht
Auf folgende Weise rufen Sie die wichtigsten Grafikklassen auf:

```java
licht    = new GLLicht(); 
himmel   = new GLHimmel("Himmel.jpg");
boden    = new GLBoden("Boden.jpg");

```

##Unterklassen von GLObjekt
Häufig werden Quader, Kugel, Kegel usw. benötigt, um eine GLOOP-Welt zu gestalten. Die wichtigesten Klassen und Methoden sind in einer kurzen Übericht [hier](http://www.schulentwicklung.nrw.de/cms/upload/gloop/dokumentation/Grundlagenuebersicht_GLOOP_3.7.pdf "Grundlagenuebersicht_GLOOP_3.7") verlinkt.

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
        
        ``

# Manipulieren von GLOOP-Objekten


## Bewegen




## Texturen setzen


##Tastatur- und Mauseingaben

```java

tastatur = new GLTastatur();

```