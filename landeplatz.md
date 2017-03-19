Nachdem im Skulpturengarten Objekte rein statisch waren, d.h. ohne sich selbst zu verändern oder die Position im Raum zu wechseln, sollen in diesem Projekt drei neue Programmiertechniken eingeführt werden:

1. Java-Arrays
2. for-Schleifen
3. Animationen in GLOOP

Der folgende Programm-Code dient Ihnen als Prototyp zur Erstellung eines Hubschrauber-Landeplatzes.

**Aufgaben**  
1. Recherchieren Sie im Internet was eine Java-Array ist \(siehe z.B. [JAVAkompakt](https://lezius.gitbooks.io/javakompakt/content/01-grundlagen/05-felder.html "JAVAkompakt - Felder") ).
2. Recherchieren Sie,wie eine for-Schleife funktioniert und erläutern Sie den Einsatz der for-Schleife im vorliegenden Prototypen.  
3. Die Lichter sollen nun animiert werden. Sie sind entweder aus oder sie leuchten. Programmieren Sie folgende Animationen:

* Die Lichter gehen der Reihe nach an \(Variante 1\) und aus.
* Alle Lichter blinken gleichzeitig.
* Überlegen Sie sich zusätzlich noch eine eigene Animation der Landeplatzlichter.

```java
import GLOOP.*;
class Landeplatzszene{
    GLKamera kamera;
    GLLicht licht;
    GLHimmel himmel;
    GLBoden boden;
    GLTastatur tastatur;

    GLZylinder landeplatz;
    GLKugel[] lampe;

    Landeplatzszene(){
        kamera  = new GLSchwenkkamera();
        licht   = new GLLicht();
        himmel  = new GLHimmel("Himmel.jpg");
        boden   = new GLBoden("Gras.jpg");
        tastatur = new GLTastatur();

        //Landeplatz erstellen
        landeplatz = new GLZylinder(0,0,0,300,20);
        landeplatz.drehe(90,0,0);
        landeplatz.setzeTextur("Feld.jpg");

        //Lampen erstellen
        lampe = new GLKugel[20];
        for (int i=0; i<20; i++){
            lampe[i] = new GLKugel(290,20,0,10);
            lampe[i].drehe(_double_, _double_, _double_, _double_, _double_, _double_);
        }
    }

    void starteLauflichter(){

    }

    void starteBlinken(){

    }

}
```



