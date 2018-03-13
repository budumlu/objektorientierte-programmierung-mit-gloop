# 4.5 Das Schiebepuzzle II

Im [Kapitel 3](/das-schiebepuzzle-teil1.md) haben Sie sich mit einem Schiebepuzzle beschäftigt. Bei diesem Schiebepuzzel konnte man Puzzelteile auf Wegen verschieben, die eigentlich dem Spielprinzip nach eigentlich nicht erlaubt sind.

Im zweiten Teil soll nun ein Schiebepuzzel entwickelt werden, bei dem Puzzelteile nicht über den Rahmen oder über andere Puzzelteile hinweg verschoben werden können.

**Aufgaben**  
1. Analysieren Sie dazu zunächst den folgenden Programmcode. Erläutern Sie die Funktionsweise des Codes und gehen Sie dabei auch auf die Verwendung von [American Standard Code for Information Interchange ](https://de.wikipedia.org/wiki/American_Standard_Code_for_Information_Interchange)ein.  
2. Entwickeln Sie in Gruppenarbeit ein Prinzip, mit dem sich prüfen ließe, ob ein Puzzleteil verschoben werden dürfte, also ob das Feld auf das geschoben werden soll frei ist.  
3. Implementieren Sie die notwendige Methode `frei()` in Partnerarbeit.  
4. Gestalten sie das Schiebepuzzle nach Ihrem Geschmack neu.

```java
import GLOOP.*;

public class Puzzleanwendung
{
    private GLKamera dieKamera;
    private GLLicht dasLicht;
    private GLTastatur dieTastatur;
    private GLHimmel derHimmel;
    private GLBoden derBoden; 
    private String richtung;
    private Puzzleteil[] dasTeil;
    private GLTafel anzeigeTafel;

    public Puzzleanwendung()
    {
        dieKamera = new GLSchwenkkamera(800,600);
        dieKamera.setzePosition(55,250,250);
        dieKamera.setzeBlickpunkt(55,0,0);
        dasLicht = new GLLicht();
        dieTastatur = new GLTastatur();
        derBoden = new GLBoden("Gras.jpg");
        derHimmel = new GLHimmel("Himmel.jpg");
        anzeigeTafel = new GLTafel(55,15,-100,  200,40 );
        anzeigeTafel.setzeText("Löse das Puzzle!!!",20); 
        dasTeil = new Puzzleteil[8];
        int n=1;

        for(int j=0;j<3;j++){
            for(int i=0;i<3;i++){
                dasTeil[n-1]= new Puzzleteil(i,j,n);
                n++;
                if (n==9) break;
            }
        }
        fuehreAus();
        Sys.beenden();
    }

    void fuehreAus(){
        int markiert = 56;

        while (!dieTastatur.esc()){
            if (dieTastatur.wurdeGedrueckt()){
/** da das Zeichen nach dem Methodenaufruf gibZeichen() aus dem Speicher gelöscht
* wird, muss das Zeichen zunächst in einen Puffer geschrieben werden. Dann kann
* geprüft werden, ob die Tastatureingabe zulässig war. Wird etwas anderes als 1 bis 8 
* eingegeben und die folgende IF-Abfrage wird nicht durchgeführt, kann es passieren
* , dass man einen Array-Fehler bekommt: java.lang.ArrayIndexOutOfBoundsException (Laufzeitfehler)
*/
                int puffer = dieTastatur.gibZeichen();
                if(48<puffer&&puffer<57){
                    markiert = puffer;
                }
            }

            if (dieTastatur.unten()){
                richtung ="unten";
                dasTeil[markiert-49].verschiebe(0,0,1);
                Sys.warte(10);
                if(!frei(markiert-49))
                {
                    dasTeil[markiert-49].verschiebe(0,0,-1);
                }
                else
                {
                    for(int i=1;i<55;i++){
                        dasTeil[markiert-49].verschiebe(0,0,1);
                        Sys.warte(10);
                    }
                }
            }
            if (dieTastatur.oben()){
                richtung = "oben";
                dasTeil[markiert-49].verschiebe(0,0,-1);
                Sys.warte(10);
                if(!frei(markiert-49))
                {
                    dasTeil[markiert-49].verschiebe(0,0,1);
                }
                else
                {
                    for(int i=1;i<55;i++){
                        dasTeil[markiert-49].verschiebe(0,0,-1);
                        Sys.warte(10);
                    }
                }
            }

            if (dieTastatur.rechts()){
                richtung = "rechts";
                dasTeil[markiert-49].verschiebe(1,0,0);
                Sys.warte(10);
                if(!frei(markiert-49)){dasTeil[markiert-49].verschiebe(-1,0,0);
                }
                else
                {
                    for(int i=1;i<55;i++){
                        dasTeil[markiert-49].verschiebe(1,0,0);
                        Sys.warte(10);
                    }
                }
            }

            if (dieTastatur.links()){
                richtung = "links";
                dasTeil[markiert-49].verschiebe(-1,0,0);
                Sys.warte(10);
                if(!frei(markiert-49))
                {
                    dasTeil[markiert-49].verschiebe(1,0,0);
                }
                else
                {
                    for(int i=1;i<55;i++){
                        dasTeil[markiert-49].verschiebe(-1,0,0);
                        Sys.warte(10);
                    }
                }
            }

            Sys.warte();

        }         
        Sys.beenden();

    }
    
    public boolean frei(int pN){
        return true;
    }
    }
}
```



```java
import GLOOP.*;

public class Puzzleteil
{
    private GLTafel dieTafel;
     private int i;
     private int j;
     private int platz;

    public Puzzleteil(int pI, int pJ, int pN)
    {
        int i = pI;
        int j = pJ;
        this.setzePlatz(pN);
        dieTafel = new GLTafel(i*55,1,j*55,50,50);
        dieTafel.drehe(270,0,0);
        dieTafel.setzeText(""+platz,20);
    }
    
    public void verschiebe(int x, int y, int z)
    {
        dieTafel.verschiebe(x,y,z);
    }

    public float gibX()
    {
        return dieTafel.gibX();   
    }

    public float gibZ()
    {
        return dieTafel.gibZ();   
    }

    public void setzePlatz(int pPlatz)
    {
        this.platz = pPlatz;
    }

    public int gibPlatz()
    {
        return this.platz;
    }
}

```




