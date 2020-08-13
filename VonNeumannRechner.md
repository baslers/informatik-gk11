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
