% Wiederholung Von-Neumann-Rechner

---
revealjs-url: ../../reveal.js
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

### Komponenten eines Von-Neumann-Rechners
<font size="6">
<ul>
<li class="fragment fade-in" data-fragment-index="2">Rechenwerk/ Arithmetic Logic Unit/ ALU</li>
<ul>
<li class="fragment fade-in" data-fragment-index="1">Führt Rechenoperationen und logische Verknüpfungen aus</li>
</ul>
<li class="fragment fade-in" data-fragment-index="4">Steuerwerk/ Control Unit</li>
<ul>
<li class="fragment fade-in" data-fragment-index="3">Interpretiert Anweisungen eines Programms und steuert die Befehlsabfolge</li>
</ul>
<li class="fragment fade-in" data-fragment-index="6">Bus</li>
<ul>
<li class="fragment fade-in" data-fragment-index="5">Verbindet die einzelnen Komponenten des Rechners</li>
</ul>
<li class="fragment fade-in" data-fragment-index="8">Speicher / Memory</li>
<ul>
<li class="fragment fade-in" data-fragment-index="7">Speichert Programme und Daten, die vom Rechenwerk verwendet werden</li>
</ul>
<li class="fragment fade-in" data-fragment-index="10">Ein- und Ausgabewerk/ I/O Unit</li>
<ul>
<li class="fragment fade-in" data-fragment-index="9">Steuert die Ein- und Ausgabe von Daten und Programmen zwischen Rechner und Anwender oder Schnittstellen zu anderen Systemen</li>
</ul>
</ul>

</font>

### Prinzipien eines Von-Neumann-Rechners
<ul>
<li class="fragment fade-in">Lösen vielseitige Probleme, da ihre Struktur unabhängig vom Problem ist und Programme im Speicher liegen</li>
<li class="fragment fade-in">Daten und Programme liegen im selben Speicher</li>
<li class="fragment fade-in">Programme können wie Daten verändert werden</li>
<li class="fragment fade-in">Aufeinanderfolgende Programmbefehle folgen auch im Speicher aufeinander</li>
<li class="fragment fade-in">Mit Sprungbefehlen kann von der Programmfolge abgewichen werden</li>
<li class="fragment fade-in">Daten werden im Speicher binär kodiert</li>
<li class="fragment fade-in">Daten sind in fortlaufenden Zellen fester Größe gespeichert</li>
</ul>

### Das binäre Zahlensystem
<font size="5">

| Dezimalsystem |        |        |        |             | Binärsystem |       |       |       |       |       |       |       |
| ------------- | ------ | ------ | ------ | ----------- | ----------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| T             | H      | Z      | E      | Stellenwert | 128er       | 64er  | 32er  | 16er  | 8er   | 4er   | 2er   | 1er   |
| $10^3$        | $10^2$ | $10^1$ | $10^0$ |             | $2^7$       | $2^6$ | $2^5$ | $2^4$ | $2^3$ | $2^2$ | $2^1$ | $2^0$ |
| 1000          | 100    | 10     | 1      |             | 128         | 64    | 32    | 16    | 8     | 4     | 2     | 1     |
|               |        |        |        |             |             |       |       |       |       |       |       |       |
| 4             | 1      | 0      | 6      |             | 1           | 0     | 1     | 1     | 0     | 0     | 1     | 1     |
|               |        |        |        |             |             |       |       |       |       |       |       |       |

</font>
<font size="4">

| Dezimalsystem                                      | Binärsystem                                                                          |
| -------------------------------------------------- | ------------------------------------------------------------------------------------ |
| $4\cdot 1000+1\cdot 100+0\cdot 10+6\cdot 1 = 4106$ | $1\cdot 128+0\cdot 64+1\cdot 32+1\cdot 16+0 \cdot 8+0\cdot 4+ 1\cdot 2+1\cdot 1=179$ |
|                                                    |                                                                                      |

</font>

### Binärzahlen in Dezimalzahlen umwandeln
<font size="5">

Beispiel: 10110011  

1. Möglichkeit: $1\cdot 128+0\cdot 64+1\cdot 32+1\cdot 16+0 \cdot 8+0\cdot 4+ 1\cdot 2+1\cdot 1=179$
2. Möglichkeit: Horner-Schema

| $\downarrow\cdot 2$ | 1   | 0   | 1   | 1   | 0   | 0   | 1   | 1                                                      |
| ------------------- | --- | --- | --- | --- | --- | --- | --- | ------------------------------------------------------ |
| $\nearrow +$        | 2   | 4   | 10  | 22  | 44  | 88  | 178 | =179 (Letztes Ergebnis wird nicht mit 2 multipliziert) |
|                     |     |     |     |     |     |     |     |                                                        |

</font>

### Übungen Binärzahlen in Dezimalzahlen umwandeln
a) 0010 0111
b) 1111 1111 
c) 1101 1010 
d) 0011 0111 
e) 1111 0100 

### Lösungen Binärzahlen in Dezimalzahlen umwandeln
a) 0010 0111 = 39
b) 1111 1111 = 255
c) 1101 1010 = 218
d) 0011 0111 = 55
e) 1111 0100 = 244

### Dezimalzahlen in Binärzahlen umwandeln
<font size="5">

Beispiel: 190

| Division | Quotient | Rest |
| -------- | -------- | ---- |
| 190:2    | 95       | 0    |
| 95:2     | 47       | 1    |
| 47:2     | 23       | 1    |
| 23:2     | 11       | 1    |
| 11:2     | 5        | 1    |
| 5:2      | 2        | 1    |
| 2:2      | 1        | 0    |
| 1:2      | 0        | 1    |
|          |          |      |

Die Reste ergeben von unten nach oben gelesen das Ergebnis 10111110.

</font>

### Übungen Dezimalzahlen in Binärzahlen umwandeln
a) 37
b) 127
c) 90
d) 166
e) 200

### Lösungen Dezimalzahlen in Binärzahlen umwandeln
a) 37 = 0010 0101 
b) 127 = 0111 1111 
c) 90 = 0101 1010 
d) 166 = 1010 0110 
e) 200 = 1100 1000
