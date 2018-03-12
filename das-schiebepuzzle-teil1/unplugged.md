# 3.1 Programme per Hand ausführen
Du hast gelernt Klassendiagramme zu erstellen. Nun wirst Du lernen Programmanweisungen aufzuschreiben, mit denen Du später Dein erstes echtes Computer-Programm steuern kannst. Unten siehst Du ein Koordinatensystem abgebildet, in dem sich 8 Puzzleteile befinden. Diese Teile lassen sich durch Verschieben in die richtige Reihenfolge bringen (von unten links nach oben rechts aufsteigend) . Dabei lässt sich ein Puzzle-Teil nur in ein leeres Puzzlefeld schieben, wie bei einem echten Schiebepuzzle.
Da es in unserer verwendeten Programmierwelt 3 Dimensionen gibt musst Du auch hier immer 3 Koordinaten zum Verschieben eines Puzzleteils angeben. Die rote (waagerechte) Achse ist die x-Achse, die grüne (senkrechte) Achse ist die y-Achse. Später gibt es dann noch die blaue Achse als z-Achse. (x- und z-Achse liegen dabei, wie bei allen aktuellen Spiele-Engines, in der Bodenebene.)

![50%](/assets/Schiebepuzzel.png)

**Beispiele**: 
- zum Verschieben des zweiten Puzzleteils nach oben:

 `dasTeil2.verschiebe(0,50,0)`
- zum Verschieben des siebten Puzzleteils nach rechts:
 `dasTeil7.verschiebe(50,0,0)`

- allgemein:
`dasTeil#.verschiebe(x,y,z)`

**1. Aufgabe**:  Notiere die Programmanweisungen, die notwendig sind, um das oben abgebildete Schiebepuzzle zu lösen. Schneide dazu die Puzzleteile auf dem zweiten Arbeitsblatt aus und zeichne ein Koordinatensystem auf ein leeres Blatt.
assert(true);
 

{% exercise %}
Kontrolliere Deinen Lösungsweg, indem Du auf `Solution` klickst:

{% initial %}
Hier darf derzeit leider kein Programmcode eingegeben werden!
Ansonsten kann die Lösung nicht angezeigt werden!
{% solution %}
dasTeil4.verschiebe(0,-50,0);
dasTeil5.verschiebe(50,0,0);
dasTeil7.verschiebe(0,50,0);
dasTeil4.verschiebe(-50,0,0);
dasTeil5.verschiebe(0,-50,0);
dasTeil8.verschiebe(-50,0,0);

{% validation %}



{% endexercise %}
 
 
 **2. Aufgabe**:  Führe zunächst maximal 5 Anweisungen auf das gelöste Puzzle durch und notiere Dir die Anweisungen. Dein Partner versucht das so verschobene Puzzle zu lösen und notiert seine Anweisungen. Vergleicht eure notierten Anweisungen. Was stellt ihr fest?

 **3. Aufgabe**:  Entwickle anhand des echten Schiebepuzzles oder des Papier-Schiebepuzzles eine allgemeine Lösungsstrategie für Schiebepuzzle und notiere diese.
 
 **4. Aufgabe**:  Gibt es eine Möglichkeit das Schiebepuzzle so zu legen, dass es nicht lösbar ist? Stelle eine Vermutung an, probiere es aus und recherchiere dazu im Internet.