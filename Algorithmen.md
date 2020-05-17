% Algorithmen

---
revealjs-url: https://revealjs.com
theme: white
width: \"95%\"
height: \"95%\"
header-includes:
    <style>
    .beispiel {
      border:3px;
      border-style:solid;
      border-color:black;
      width:fit-content;
      margin:auto;
    }
    .wichtig {
      border:3px;
      border-style:solid;
      border-color:red;
      width:fit-content;
      margin:auto;
    }
    </style>
...

### Definition: Algorithmus
Ein **Algorithmus** ist eine *endliche*, *eindeutige*, *ausführbare* und *allgemeingültige* Verarbeitungsvorschrift.

### Endlichkeit
Ein Algorithmus besteht aus endlich vielen Anweisungen (**Finitheit**) und darf zur Ausführung nur endlich viele Schritte benötigen (**Terminiertheit**).

### Eindeutigkeit
An jeder Stelle des Algorithmus ist der nächste Schritt eindeutig definiert (**Determinismus**). Daraus folgt, dass gleiche Eingaben bei wiederholter Ausführung des Algorithmus zu gleichen Ausgaben führen (**Determiniertheit**).

### Ausführbarkeit
Jede Anweisung des Algorithmus muss für den "Prozessor" verständlich und ausführbar sein.

### Allgemeingültigkeit
Ein Algorithmus löst nicht nur einen Spezialfall, sondern eine ganze Klasse gleichartiger Probleme.

### Beispiel: Euklidischer Algorithmus
    euclid(a, b)
      wenn a = 0 dann
        Ergebnis = b
      sonst
        solange b != 0
          wenn a > b dann
            a = a - b
          sonst
            b = b - a
          //
        //
      Ergebnis = a
1. Aufgabe: Führe den Algorithmus euclid(44, 12) durch. Was berechnet der euklidische Algorithmus?
2. Aufgabe: Implementiere den Algorithmus.

### Aufgabe: Schaltjahr
Regeln eines Schaltjahres:  

1. Ist ein Jahr durch 4 ganzzahlig teilbar, ist es ein Schaltjahr.  
2. Ist ein Jahr durch 100 teilbar, ist es trotz Regel 1 *kein* Schaltjahr.  
3. Ist ein Jahr durch 400 teilbar, ist es trotz Regel 2 ein Schaltjahr.  

Aufgabe: Entwickle und implementiere einen Algorithmus, der für ein gegebenes Jahr bestimmt, ob es sich um ein Schaltjahr handelt.  
Input: int  
Output: boolean  
