% Einführung in die Programmierung

---
revealjs-url: https://revealjs.com
theme: white
...

### Compilersprachen vs Interpretersprachen
Compilersprachen:  
<li class="fragment fade-in">Compiler übersetzt Quelltext in Maschinencode</li>
<li class="fragment fade-in">Maschinencode ist nur von jeweiligem Betriebssystem ausführbar</li>
<li class="fragment fade-in">Beispiel: Quelle.c $\rightarrow$ Quelle.exe</li>  

Interpretersprachen:  
<li class="fragment fade-in">Interpreter lässt Quelltext direkt ausführen</li>
<li class="fragment fade-in">Quelltext ist auf jedem Betriebssystem ausführbar, auf dem der Interpreter verfügbar ist</li>

### Compilersprachen vs Interpretersprachen
Aufgabe 1: Informiere dich im Internet über die Vor- und Nachteile von Compilersprachen bzw. Interpretersprachen  
Aufgabe 2: Suche im Internet nach Beispielen für Compilersprachen bzw. Interpretersprachen  
Aufgabe 3: Informiere dich im Internet darüber, wie Java und Python zuzuordnen sind

### Java Installation
<li class="fragment fade-in">Um Java-Programme zu schreiben benötigt man das Java Development Kit (JDK)</li>
<li class="fragment fade-in">Zum Ausführen von Java-Programmen reicht die Java Runtime Environment (JRE)</li>
<li class="fragment fade-in">Beides ist auf java.com kostenlos verfügbar</li>

### Java Programmierung
<li class="fragment fade-in">Nach Installation des JDK kann eine Java-Datei mit der Endung .java in der Kommandozeile mit dem Befehl "javac dateiname.java" kompiliert werden</li>
<li class="fragment fade-in">Mit "java dateiname" kann das kompilierte Programm ausgeführt werden</li>

### Java Programmierung
<li class="fragment fade-in">Zur Erstellung von Java-Dateien reicht ein Texteditor</li>
<li class="fragment fade-in">Integrierte Entwicklungsumgebungen (IDE) bieten hilfreiche Zusatzfunktionen zum fortgeschrittenen Programmieren</li>
<li class="fragment fade-in">Beispiele sind Eclipse, Netbeans oder zum Lernen der Java-Editor</li>

### Programmaufbau

    public class Klassenname{
      public static void main(String[] args){
        Definitionen und Anweisungen; //Hier beginnt das Programm
      }
    }

Beispiel:  

    public class Hallo{
      public static void main(String... args){
        System.out.println("Hallo in meinem ersten Programm");
      }
    }

### Pakete importieren
Statt das Rad neu zu erfinden, kann es auch importiert werden:  
Beispiel für Nachrichtenfenster:  

    import javax.swing.JOptionPane;
    public class Nachrichtenfenster{
      public static void main(String... args){
        JOptionPane.showMessageDialog(null, "Hallo im Nachrichtenfenster");
      }
    }

### Klassen
<li class="fragment fade-in">Ein Java-Programm besteht aus mindestens einer "Klasse"</li>
<li class="fragment fade-in">Die KlassenDefinition beginnt mit den Wörtern "public class" gefolgt vom Klassennamen</li>
<li class="fragment fade-in">Klassenname=Dateiname</li>
<li class="fragment fade-in">Konventionell beginnen Klassennamen mit einem Großbuchstaben und jedes weitere Wort folgt ohne Leerzeichen beginnend mit Großbuchstaben (CamelCase-Notation)</li>

### Datentypen
<font size="4">

| Typ                  | Wertebereich                | Beispiel |
| -------------------- | --------------------------- | -------- |
| **Ganze Zahlen**     |                             |          |
| byte                 | -1238...127                 | 123      |
| short                | -32768...32767              | 1234     |
| int                  | $2\cdot 10^9...2\cdot 10^9$ | 12345    |
| long                 | $-10^{19}...10^{19}$        | 123456L  |
| **Gleitkommazahlen** |                             |          |
| float                | $-10^{38}...10^{38}$        | 1.2f     |
| double               | $-10^{308}...10^{308}$      | 1.2      |
| **Wahrheitswert**    |                             |          |
| boolean              | {true, false}               | true     |
| **Zeichen**          |                             |          |
| char                 | Unicode Zeichen             | 'c'      |
| **Zeichenkette**     |                             |          |
| String               |                             | "Hallo"  |

</font>

### Anweisungen, Definitionen, Deklarationen und Initialisierungen
<font size="6">
<li class="fragment fade-in">Ein Programm besteht insbesondere aus Anweisungen, d.h. Befehlen, und Definitionen</li>
<li class="fragment fade-in">Anweisungen werden nacheinander abgearbeitet</li>
<li class="fragment fade-in">Anweisungen werden mit einem Semikolon abgeschlossen</li>
<li class="fragment fade-in">Definitionen legen u.a. Bezeichner und Datentyp einer Variablen fest und reservieren entsprechenden Speicherplatz</li>
<li class="fragment fade-in">Deklarationen machen dem Programm ebenfalls Variablen bekannt, reservieren aber keinen Speicherplatz</li>
<li class="fragment fade-in">Wird einer Variablen erstmalig ein Wert zugeordnet, spricht man von einer Initialisierung</li>
</font>

### Definition und Initialisierung
Definition einer Variablen:  

    //<Datentyp> <Bezeichner>;
    int zahl;

Initialsierung (Zuweisung):

    //<Bezeichner> = <Wert>;
    zahl = 1;

Definition und Initialisierung:

    //<Datentyp> <Bezeichner> = <Wert>;
    int zahl = 1;


### Kommentare
<li class="fragment fade-in" data-fragment-index="0">Um Programme lesbarer zu machen, können Kommentare eingefügt werden, die vom Compiler ignoriert werden</li>
<li class="fragment fade-in" data-fragment-index="1"><span class="fragment highlight-blue" data-fragment-index="1">// ...</span> ist ein einzeiliger Kommentar, der mit dem Zeilenende endet</li>
<li class="fragment fade-in" data-fragment-index="2"><span class="fragment highlight-blue" data-fragment-index="2">/* ... \*/</span> ist ein mehrzeiliger Kommentar</li>
<li class="fragment fade-in" data-fragment-index="3"><span class="fragment highlight-blue" data-fragment-index="3">/** ... \*/</span> ist ein mehrzeiliger Dokumentationskommentar vor Definitionen</li>

### Definition und Initialisierung (Übung)
<ol>
<li class="fragment fade-in">Öffne das Programm DefinitionUndInitialisierung.java und schreibe als Kommentar hinter der jeweiligen Zeile, ob eine Definition oder eine Initialisierung vorliegt.</li>
<li class="fragment fade-in">Öffne das Programm SelbstDefinierenUndZuweisen.java und setze die Kommentare um.</li>
</ol>

### Blöcke
<li>Anweisungen können zu einem Block zusammengefasst werden</li>
<li>Blöcke werden durch geschweifte Klammern umschlossen und sollten eingerückt werden</li>
<li>Zwei Konventionen zur Platzierung der Klammern sind verbreitet:</li>

    public class Willkommen{
      ...
    }

    public class Willkommen
    {
      ...
    }


### Strings und Texte
<font size="6">
<li class="fragment fade-in" data-fragment-index="1">Strings sind Ketten von Zeichen</li>
<li class="fragment fade-in" data-fragment-index="2">In Anführungszeichen gesetzter Text wird als String definiert</li>
<li class="fragment fade-in" data-fragment-index="3">Neue Zeilen können durch <span class="fragment highlight-blue" data-fragment-index="3">\\n</span> erzeugt werden</li>
<li class="fragment fade-in" data-fragment-index="4">Mit der Anweisung <span class="fragment highlight-blue" data-fragment-index="4">System.out.println("...")</span> kann Text in der Konsole ausgegeben werden</li>
<li class="fragment fade-in" data-fragment-index="5">Strings und Variablen können mit einem + miteinander verbunden werden, z.B. <span class="fragment highlight-blue" data-fragment-index="5">System.out.println("hier steht der Text von "+name)</span></li>
<li class="fragment fade-in" data-fragment-index="6">Strings können durch <span class="fragment highlight-blue" data-fragment-index="6">string1.equals(string2)</span> verglichen werden</li>
</font>

### Texte einlesen

    import java.util.Scanner;
    public class Text{
      public static void main(String[] args){
        Scanner in = new Scanner(System.in);
        String text = in.nextLine(); //liest die nächste Zeile ein
        int i = in.nextInt(); //liest die nächste Zeile als Zahl ein
        int j = in.nextInt();
        System.out.println(i+j);
      }
    }

### Operatoren
<font size="5">

| Numerische Operatoren |                              | Logische Operatoren |                |
| --------------------- | ---------------------------- | ------------------- | -------------- |
| +                     | Addition                     | ==                  | Gleichheit     |
| -                     | Subtraktion                  | !=                  | Ungleichheit   |
| *                     | Multiplikation               | <                   | kleiner als    |
| /                     | Division                     | <=                  | kleiner gleich |
| %                     | Modulo (Rest einer Division) | >                   | größer als     |
| ++                    | Inkrement                    | >=                  | größer gleich  |
| +=                    | Inkrement und Zuweisung      | !                   | nicht          |
| --                    | Dekrement                    | &&                  | UND            |
| -=                    | Dekrement und Zuweisung      | \|\|                | ODER           |
| (...)                 | Klammerung                   |                     |                |
|                       |                              |                     |                |

</font>

### Bedingte Anweisungen und Verzweigungen

    //Bedingte Anweisung:
    if(bedingung){
      //Anweisungen, die ausgeführt werden, wenn bedingung true ist
    }
    //Anweisungen, die unabhängig von bedingung nach der bedingten Anweisung ausgeführt wird

    //Verzweigung
    if(bedingung){
      //Anweisungen, die ausgeführt werden, wenn bedingung true ist
    }else{
      //Anweisungen, die ausgeführt werden, wenn bedingung false ist
    }
    //Anweisungen, die unabhängig von bedingung nach der Verzweigung ausgeführt wird

### Übungsaufgabe Chatbot
<font size="5"><p style="line-height: 100%">
Aufgabe: Schreibe einen Chatbot, der mit dem Nutzer chattet. Sorge durch sinnvolle Variablen und Kommentare dafür, dass das Programm für Andere leicht nachzuvollziehen ist und achte auf die besprochenen Konventionen. Der Dateiname soll dein Name sein.
</p>  
<span class="fragment fade-in">Der Chatbot / das Programm sollte folgendes erfüllen:</span>  
<li class="fragment fade-in">Jede Ausgabe des Chatbots soll mit "Chatbot: " starten</li>
<li class="fragment fade-in">Das Programm startet mit der Aufforderung an den Nutzer, den Chatbot zu begrüßen</li>
<li class="fragment fade-in">Das Programm liest die Begrüßung mithilfe der Scannerklasse ein</li>
<li class="fragment fade-in">Der Chatbot begrüßt den Nutzer mit den selben Worten</li>
<li class="fragment fade-in">Der Chatbot fragt den Nutzer nach seinem Namen und verwendet den Namen fortan</li>
<li class="fragment fade-in">Der Chatbot stellt einige Ja/Nein-Fragen, die der Nutzer mit "Ja" oder "Nein" beantwortet</li>
<li class="fragment fade-in">Abhängig von der Antwort des Nutzers, soll der Chatbot die Antwort kommentieren</li>
<li class="fragment fade-in">Der Chatbot fragt nach dem Alter des Nutzers</li>
<li class="fragment fade-in">Der Chatbot fragt, wie alt der Nutzer den Chatbot schätzt</li>
<li class="fragment fade-in">Der Chatbot fragt, wie viele Wochen das gemeinsame Alter geschätzt wäre</li>
<li class="fragment fade-in">Der Chatbot berechnet das gemeinsame Alter des Nutzers und des Chatbots in Wochen und gibt das Ergebnis aus</li>
<li class="fragment fade-in">Der Chatbot gibt abhängig davon, ob man richtig, zu niedrig oder zu hoch geschätzt hat, eine entsprechende Antwort aus</li>
</font>

### Schleifen
<li class="fragment fade-in">Kontrollstrukturen, um Anweisungs-Blöcke zu wiederholen</li>
<li class="fragment fade-in">Man unterscheidet:</li>
<li class="fragment fade-in">Zählschleifen (For-Schleifen)</li>
<li class="fragment fade-in">Kopfgesteuerte Schleifen (While-Do-Schleifen)</li>
<li class="fragment fade-in">Fußgesteuerte Schleifen (Do-While-Schleifen)</li>
<li class="fragment fade-in">Mengenschleifen (Foreach-Schleifen)</li>

### Zählschleifen (For-Schleifen)
<font size="6">
    for(INITIALISIERUNG; BEDINGUNG; AKTUALISIERUNG){}
      ANWEISUNGEN;
    }

Beispiel:  

    int summeVon0Bis9 = 0;
    for(int i=0; i<10; i++){
      summeVon0Bis9 += i;
    }

<li class="fragment fade-in">Initialsierung: Zählvariable wird initialisiert</li>
<li class="fragment fade-in">Bedingung: Schleife wird wiederholt, bis die Bedingung nicht mehr erfüllt ist</li>
<li class="fragment fade-in">Aktualisierung: Zählvariable wird aktualisiert</li>
</font>

### Kopfgesteuerte Schleifen (While-Do-Schleifen)
<font size="6">
    while(BEDINGUNG){
      ANWEISUNGEN;
    }

Beispiel:  

    int summeVon0Bis9 = 0;
    int i = 0;
    while(i<10){
      summeVon0Bis9 += i;
      i++;
    }

<li class="fragment fade-in">Schleife wird nur durchlaufen, wenn die Bedingung erfüllt ist</li>
<li class="fragment fade-in">Schleife wird wiederholt, bis die Bedingung nicht mehr erfüllt ist</li>
<li class="fragment fade-in">Initialisiert wird ggfs. vor der Schleife</li>
<li class="fragment fade-in">Aktualisiert wird ggfs. innerhalb der Schleife</li>
</font>

### Fußgesteuerte Schleifen (Do-While-Schleifen)
<font size="6">
    do{
      ANWEISUNGEN;
    }(BEDINGUNG);

Beispiel:  

    int i = 0;
    int summeVon0Bis9 = 0;
    do{
      summeVon0Bis9 += i;
      i++;
    }while(i<10);

<li class="fragment fade-in">Schleife wird mindestens einmal durchlaufen, unabhängig von der Bedingung</li>
<li class="fragment fade-in">Schleife wird wiederholt, bis die Bedingung nicht mehr erfüllt ist</li>
<li class="fragment fade-in">Initialsiert wird ggfs. vor der Schleife</li>
<li class="fragment fade-in">Aktualisiert wird ggfs. innerhalb der Schleife</li>
</font>

### Mengenschleifen (Foreach-Schleifen)
<font size="6">
    for(TYP ELEMENT : KOLLEKTION){
      ANWEISUNGEN;
    }

Beispiel:  

    int[] numbers = {0,1,2,3,4,5,6,7,8,9};
    int summeVon0Bis9 = 0;
    for(int i : numbers){
      summeVon0Bis9 += i;
    }

<li class="fragment fade-in">Schleife wird für jedes Element einer Menge (z.B. Array oder Liste) durchgeführt</li>
</font>

### Übungsaufgabe Schleifen
Verwende jeweils die ersten drei Schleifenarten und beschreibe jeweils Vor- und Nachteile.  
<ol>
<li class="fragment fade-in">Gib die Zahlen von 1000 bis 0 in der Konsole aus.</li>
<li class="fragment fade-in">Berechne mithilfe einer Schleife 10! und gib das Ergebnis in der Konsole aus.</li>
<li class="fragment fade-in">Gib das kleine Einmaleins in der Konsole aus:</li>
<ul style="list-style-type:none;">
<li class="fragment fade-in">1 x 1 = 1</li>
<li class="fragment fade-in">1 x 2 = 2</li>
<li class="fragment fade-in">...</li>
<li class="fragment fade-in">10 x 10 = 100</li>
</ul>
</ol>

### Übungsaufgabe Verflixte Sieben
<font size="6">
Ein in der Grundschule und in der Sekundarstufe 1 beliebtes Mathespiel ist die verflixte Sieben.  
Dabei zählt man reihum von 1 beginnend aufwärts, aber lässt jede Zahl aus, die durch die 7 teilbar ist oder die 7 als Ziffer enthält.  
Also: 1,2,3,4,5,6,8,...,13,15,16,18...  
Erstelle ein Programm das auf diese Weise von 1 bis 1000 zählt.  
Dabei ist der Modulo Operator % und die Funktion STRINGVARIABLENNAME.contains("ZEICHENKETTE, DIE ENTHALTEN SEIN SOLL") nützlich.
</font>

### Arrays
<font size="6">
<li class="fragment fade-in">Ein Array (Feld) ist eine Datenstruktur, die mehrere Daten vom selben Typ speichert</li>
<li class="fragment fade-in">Der Zugriff erfolgt über Indizes</li>
<span class="fragment fade-in">Beispiel:  </span>
<li class="fragment fade-in">Statt name0="Max", name1="Hans", name2="Petra" benutzen wir ein Array zum Speichern der Vornamen einer Namensliste</li>
<li class="fragment fade-in">Dann ist namen[0]="Max", namen[1]="Hans", namen[2]="Petra"</li>
<li class="fragment fade-in">Durch den Zugriff durch Indizes ist z.B. der Zugriff auf die Variablen innerhalb von Schleifen deutlich leichter</li>
</font>

### Aufbau von Arrays

    DATENTYP[] ARRAYVARIABLENNAME = new DATENTYP[LÄNGEDESARRAYS];

Die leeren eckigen Klammern dürfen auch hinter dem Arrayvariablennamen stehen:

    DATENTYP ARRAYVARIABLENNAME[] = new DATENTYP[LÄNGEDESARRAYS];

Der Inhalt des Arrays kann bereits bei der Definition des Arrays initialisiert werden:

    DATENTYP[] ARRAYVARIABLENNAME = {ELEMENT0, ELEMENT1, ..., ELEMENTN};

### Array Beispiel Namensliste

    String[] namen = new String[3]; //Array wird deklariert
    namen[0] = "Max"; //Der Inhalt an der Stelle 0 des Arrays wird initialisiert
    namen[1] = "Hans";
    namen[2] = "Petra";
    System.out.println("Der erste Name in der Liste ist " + namen[0]); //Der erste Name wird in der Konsole ausgegeben

### Array Beispiel Namensliste

    String[] namen = {"Max", "Hans", "Petra"}; //Array wird deklariert und sein Inhalt gleichzeitig initialisiert, die Länge ergibt sich damit automatisch
    System.out.println("Der erste Name in der Liste ist " + namen[0]); //Der erste Name wird in der Konsole ausgegeben

### Weitere Beispiele

    boolean[] istMaennlich = new boolean[3];
    istMaennlich[0] = true;
    istMaennlich[1] = true;
    istMaennlich[2] = false;
    int[] alter = {16, 17, 16};
    System.out.println(namen[0] + " ist " + alter[0] " Jahre alt."); //Max ist 16 Jahre alt.
    if(istMaennlich[0]){  //Wenn die erste Person in der Liste männlich ist, wird dies so ausgegeben.
      System.out.println(namen[0] + " ist männlich.");
    }else{ //ansonsten wird ausgegeben, dass sie weiblich ist.
      System.out.println(namen[0] + " ist weiblich.");
    }

### Länge eines Arrays
<li class="fragment fade-in">Arrays haben immer eine bestimmte Länge</li>
<li class="fragment fade-in">Die Länge kann durch ARRAYVARIABLENNAME.length abgerufen werden</li>
<li class="fragment fade-in">Zugriff über einen Index, der kleiner als 0 ist oder größer oder gleich der Länge des Arrays ist, führt zu einem Fehler</li>

### Mehrdimensionale Arrays (Matrizen)
<li class="fragment fade-in">Mit Arrays können auch Matritzen realisiert werden</li>
<li class="fragment fade-in">Beispiel: Bilddarstellung an einem Full HD-Monitor, wobei der gespeicherte int-Wert die Farbe codiert, die an dem Pixel dargestellt wird, der durch die Indizes beschrieben wird</li>
<li class="fragment fade-in">int[][] bild = new int[1080][1920]</li>

### Beispiel Mehrdimensionale Arrays
<font size="6">

    int[][] matrix = new int[3][4];
    matrix[0][0] = 1;
    matrix[0][1] = 2;
    ...
    matrix[2][3] = 12;

die gleiche Matrix erzeugt auch

    int[][] matrix = new int[3][4];
    int[] zeile0 = {1,2,3,4};
    int[] zeile1 = {5,6,7,8};
    int[] zeile2 = {9,10,11,12};
    matrix[0] = zeile0;
    matrix[1] = zeile1;
    matrix[2] = zeile2;

oder

    int[][] matrix = {{1,2,3,4},{5,6,7,8},{9,10,11,12}};

</font>

### Übungsaufgabe Primzahlenfinder
<font size="6"><p style="line-height: 100%">
Eine Primzahl ist eine natürliche Zahl, die durch genau zwei verschiedene natürliche Zahlen teilbar ist. Anders ausgedrückt ist eine Primzahl eine natürliche Zahl, die nur durch sich selbst und die Zahl 1 teilbar ist, mit Außnahme der 1 selbst.  
1. Schreibe ein Programm, das die ersten 100 Primzahlen findet, in einem Array speichert und das Array am Ende ausgibt.  
Um zu ermitteln, ob eine natürliche Zahl x eine Primzahl ist, kann man x durch jede natürliche Zahl kleiner als x teilen und überprüfen, ob ein Rest übrig bleibt.  
Dabei kann der Modulo-Operator % nützlich sein, der den Rest zurückgibt der beim Teilen von zwei Zahlen übrig bleibt.  
2. Finde und implementiere einen Algorithmus, der effizienter arbeitet, als der eben beschriebene Algorithmus, indem nicht jede kleinere Zahl als x überprüft wird, sondern nur die nötigen.
</p></font>
