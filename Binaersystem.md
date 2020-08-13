% Binärsystem

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

### Mit Binärzahlen rechnen
Binärzahlen können addiert, subtrahiert, multipliziert und dividert werden.  
Dabei geht man genauso vor, wie beim Rechnen mit Dezimalzahlen.

### Negative Binärzahlen
Aufgabe: Entwirf ein Binärsystem, mit dem auch negative Zahlen dargestellt werden können. 

### Erste Idee: Vorzeichen-Bit
Erstes Bit einer Zahl fester Bitlänge gibt das Vorzeichen an (0=+ und 1=-). Die restlichen Bits geben den Betrag an.  
Beispiel:  

| Positive Binärzahlen | Negative Binärzahl |
| -------------------- | ------------------ |
| $0010 \hat{=} 2$     | $1010 \hat{=} -2$  |
| $0000 \hat{=} 0$     | $1000 \hat{=} -0$  |
|                      |                    |

### Nachteile eines Vorzeichen-Bits
1. Problem: Zwei Zahlen für die 0.
2. Problem: Addition negativer Zahlen mit positiver Zahlen (Subtraktion) funktioniert nicht:  
$$
\begin{aligned}
&0010\\
+&1010\\
\hline
&1100 \hat{=}-4\text{, statt } 0
\end{aligned}
$$

### Zweite Idee: Einerkomplement
- Feste Bitlänge
- Positive Zahlen haben eine 0 als erstes Bit und werden wie vorzeichenlose Zahlen gebildet
- Negative Zahlen haben eine 1 als erstes Bit und werden gebildet, indem ihre Gegenzahl bitweise invertiert wird

### Zweite Idee: Einerkomplement

| Positive Binärzahl | Negative Binärzahl |
| ------------------ | ------------------ |
| $0010\hat{=}2$     | $1101\hat{=}-2     |
| $0000\hat{=}0$     | $0000\hat{=}-0$    |
|                    |                    |

### Vorteil des Einerkomplements
Subtraktion funktioniert:

$$
\begin{alignedat}{2}
&0010\hat{=}2&\qquad &0101\hat{=}5\\
+&1101\hat{=}-2& +&1000\hat{=}-7\\
&\overline{1111\hat{=}0}& &\overline{1101\hat{=}-2}
\end{alignedat}
$$

### Nachteile des Einerkomplements
1. Problem: Zwei Zahlen für die Null
2. Problem: Wird die Null durchschritten, muss der Überlauf zum Ergebnis hinzuaddiert werden:

$$
\begin{alignedat}{2}
&1011\hat{=}-4\\
+&0110\hat{=}6\\
&\overline{0001\hat{=}1}\quad\text{falsch, Übertrag muss addiert werden}\\
+&0001\\
&\overline{0010\hat{=}2}
\end{alignedat}
$$

### Dritte Idee: Zweierkomplement
- Positive Zahlen haben eine 0 als erstes Bit und werden wie vorzeichenlose Zahlen gebildet
- Negative Zahlen haben eine 1 als erstes Bit und ergeben sich aus der bitweisen Invertierung und anschließender Addition der 1 (Überlauf wird ignoriert)

### Dritte Idee: Zweierkomplement

| Positive Binärzahl | Negative Binärzahl |
| ------------------ | ------------------ |
| $0010\hat{=}2$     | $1110\hat{=}-2$    |
| $0000\hat{=}0$     | $0000\hat{=}-0$    |
|                    |                    |

### Vorteile des Zweierkomplement
- Nur eine Zahl für die 0
- Subtraktion funktioniert auch ohne den Überlauf auszuwerten

### Hinweise zum Zweierkomplement
- Bitlänge ist vorher festgelegt
- Ergebnisse müssen durch die Bitlänge darstellbar sein
- Betragsmäßiger Zahlenbereich ist kleiner als bei vorzeichenlosen Zahlen (z.B. -8 bis +7 statt 0 bis 15)
