
# Hallo! Leere Welt!
```java

import GLOOP.*;
class HalloWelt{
    //Kamera und Umgebung deklarieren
    GLKamera kamera;
    GLLicht licht;
    GLBoden boden;
    GLHimmel himmel;


    HalloWelt(){
        //Kamera und Umgebung instanziieren
        kamera = new GLSchwenkkamera();
        kamera.setzePosition(0,300,500);
        licht  = new GLLicht();
        boden  = new GLBoden("Gras.jpg");
        himmel = new GLHimmel("Himmel.jpg"); 
    }
}
```

