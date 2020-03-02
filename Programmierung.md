% Einführung in die Programmierung

---
revealjs-url: https://revealjs.com
theme: white
...

## Compilersprachen vs Interpretersprachen
Compilersprachen:  
<li class="fragment fade-in">Compiler übersetzt Quelltext in Maschinencode</li>
<li class="fragment fade-in">Maschinencode ist nur von jeweiligem Betriebssystem ausführbar</li>
<li class="fragment fade-in">Beispiel: Quelle.c $\rightarrow$ Quelle.exe</li>  

Interpretersprachen:  
<li class="fragment fade-in">Interpreter lässt Quelltext direkt ausführen</li>
<li class="fragment fade-in">Quelltext ist auf jedem Betriebssystem ausführbar, auf dem der Interpreter verfügbar ist</li>

## Compilersprachen vs Interpretersprachen
Aufgabe 1: Informiere dich im Internet über die Vor- und Nachteile von Compilersprachen bzw. Interpretersprachen  
Aufgabe 2: Suche im Internet nach Beispielen für Compilersprachen bzw. Interpretersprachen  
Aufgabe 3: Informiere dich im Internet darüber, wie Java und Python zuzuordnen sind

## Java Installation
<li class="fragment fade-in">Um Java-Programme zu schreiben benötigt man das Java Development Kit (JDK)</li>
<li class="fragment fade-in">Zum Ausführen von Java-Programmen reicht die Java Runtime Environment (JRE)</li>
<li class="fragment fade-in">Beides ist auf java.com kostenlos verfügbar</li>

## Java Programmierung
<li class="fragment fade-in">Nach Installation des JDK kann eine Java-Datei mit der Endung .java in der Kommandozeile mit dem Befehl "javac dateiname.java" kompiliert werden</li>
<li class="fragment fade-in">Mit "java dateiname" kann das kompilierte Programm ausgeführt werden</li>

## Java Programmierung
<li class="fragment fade-in">Zur Erstellung von Java-Dateien reicht ein Texteditor</li>
<li class="fragment fade-in">Integrierte Entwicklungsumgebungen (IDE) bieten hilfreiche Zusatzfunktionen zum fortgeschrittenen Programmieren</li>
<li class="fragment fade-in">Beispiele sind Eclipse, Netbeans oder zum Lernen der Java-Editor</li>

## Programmaufbau

    public class Klassenname{
      public static void main(String[] args){
        Deklarationen und Anweisungen; //Hier beginnt das Programm
      }
    }

Beispiel:  

    public class Hallo{
      public static void main(String... args){
        System.out.println("Hallo in meinem ersten Programm");
      }
    }

## Pakete importieren
Statt das Rad neu zu erfinden, kann es auch importiert werden:  
Beispiel für Nachrichtenfenster:  

    import javax.swing.JOptionPane;
    public class Nachrichtenfenster{
      public static void main(String... args){
        JOptionPane.showMessageDialog(null, "Hallo im Nachrichtenfenster");
      }
    }

## Klassen
<li class="fragment fade-in">Ein Java-Programm besteht aus mindestens einer "Klasse"</li>
<li class="fragment fade-in">Die Klassendeklaration beginnt mit den Wörtern "public class" gefolgt vom Klassennamen</li>
<li class="fragment fade-in">Klassenname=Dateiname</li>
<li class="fragment fade-in">Konventionell beginnen Klassennamen mit einem Großbuchstaben und jedes weitere Wort folgt ohne Leerzeichen beginnend mit Großbuchstaben (CamelCase-Notation)</li>

## Datentypen
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

## Anweisungen, Deklarationen und Initialisierungen
<li class="fragment fade-in">Ein Programm besteht aus Anweisungen, d.h. Befehlen, und Deklarationen</li>
<li class="fragment fade-in">Anweisungen werden nacheinander abgearbeitet</li>
<li class="fragment fade-in">Anweisungen werden mit einem Semikolon abgeschlossen</li>
<li class="fragment fade-in">Deklarationen legen u.a. Bezeichner und Datentyp einer Variablen fest</li>
<li class="fragment fade-in">Wird einer Variablen erstmalig ein Wert zugeordnet, spricht man von einer Initialisierung</li>

## Deklaration und Initialisierung
Deklaration einer Variablen:  

    //<Datentyp> <Bezeichner>;
    int zahl;

Initialsierung (Zuweisung):

    //<Bezeichner> = <Wert>;
    zahl = 1;

Deklaration und Initialisierung:

    //<Datentyp> <Bezeichner> = <Wert>;
    int zahl = 1;


## Kommentare
<li class="fragment fade-in" data-fragment-index="0">Um Programme lesbarer zu machen, können Kommentare eingefügt werden, die vom Compiler ignoriert werden</li>
<li class="fragment fade-in" data-fragment-index="1"><span class="fragment highlight-blue" data-fragment-index="1">// ...</span> ist ein einzeiliger Kommentar, der mit dem Zeilenende endet</li>
<li class="fragment fade-in" data-fragment-index="2"><span class="fragment highlight-blue" data-fragment-index="2">/* ... \*/</span> ist ein mehrzeiliger Kommentar</li>
<li class="fragment fade-in" data-fragment-index="3"><span class="fragment highlight-blue" data-fragment-index="3">/** ... \*/</span> ist ein mehrzeiliger Dokumentationskommentar vor Deklarationen</li>

## Deklaration und Initialisierung (Übung)
Öffne das Programm DeklarationUndInitialisierung.java und schreibe als Kommentar hinter der jeweiligen Zeile, ob eine Deklaration oder eine Initialisierung vorliegt.

## Blöcke
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


## Strings und Texte
<li class="fragment fade-in" data-fragment-index="1">Strings sind Ketten von Zeichen</li>
<li class="fragment fade-in" data-fragment-index="2">In Anführungszeichen gesetzter Text wird als String definiert</li>
<li class="fragment fade-in" data-fragment-index="3">Neue Zeilen können durch <span class="fragment highlight-blue" data-fragment-index="3">\\n</span> erzeugt werden</li>
<li class="fragment fade-in" data-fragment-index="4">Mit der Anweisung <span class="fragment highlight-blue" data-fragment-index="4">System.out.println("...")</span> kann Text in der Konsole ausgegeben werden</li>

## Texte einlesen

    import java.util.Scanner;

    public class Text{
      public static void main(String[] args) throws IOException{
        Scanner in = new Scanner(System.in);
        String text = in.nextLine();
      }
    }
