% Automaten

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

## Automaten im Alltag

- <div class="fragment fade-in">Snackautomat</div>
- <div class="fragment fade-in">Getränkeautomat</div>
- <div class="fragment fade-in">Fahrstuhl</div>
- <div class="fragment fade-in">Waschmaschine</div>
- <div class="fragment fade-in">Computer</div>

## Sonstiger Nutzen von Automaten

- <div class="fragment fade-in">Sprachen erkennen</div>
    - <div class="fragment fade-in">Syntax überprüfen</div>
    - <div class="fragment fade-in">Programmcode in Maschinencode übersetzen</div>
- <div class="fragment fade-in">Programme strukturieren (Modellierung)</div>
- <div class="fragment fade-in">Beweise führen</div>

## Automaten in der Informatik

Unter anderem gibt es...

- <div class="fragment fade-in">Turingmaschinen</div>
- <div class="fragment fade-in">Linear beschränkte Automaten</div>
- <div class="fragment fade-in">Kellerautomaten</div>
- <div class="fragment fade-in">Endliche Automaten</div>
    - <div class="fragment fade-in">Deterministische Automaten</div>
    - <div class="fragment fade-in">Nichtdeterministische Automaten</div>
    - <div class="fragment fade-in">Akzeptoren</div>
    - <div class="fragment fade-in">Transduktoren</div>
        - <div class="fragment fade-in">Moore-Automaten</div>
        - <div class="fragment fade-in">Mealy-Automaten</div>
- <div class="fragment fade-in">$\omega$-Automaten</div>

## Mealy-Automaten
Ein Mealy-Automat kann als 7-Tupel  
$A=(Q,\Sigma , \Omega , \delta, \lambda, q_0, F)$ definiert werden:

- <div class="fragment fade-in">$Q$ ist eine endliche Menge von Zuständen</div>
- <div class="fragment fade-in">$\Sigma$ ist das Eingabealphabet</div>
- <div class="fragment fade-in">$\Omega$ ist das Ausgabealphabet</div>
- <div class="fragment fade-in">$\delta$ ist die Übergangsfunktion $\delta : Q\times \Sigma \rightarrow Q$</div>
- <div class="fragment fade-in">$\lambda$ ist die Ausgabefunktion $\lambda : Q\rightarrow \Omega$</div>
- <div class="fragment fade-in">$q_0\in Q$</div>
- <div class="fragment fade-in">$F\subseteq Q$</div>

<div class="fragment fade-in">F kann weggelassen werden, wenn keine Sprache untersucht werden soll</div>

## Beispiel Mealy-Automaten
Arbeitsauftrag:  

1. Gehe auf <https://bit.ly/2uMIBUo> und bearbeite auf den vier Unterseiten (System 1-4) die Aufgaben.
2. Versuche anschließend jeweils das Verhalten durch die folgende Tabelle zu beschreiben.

| gedrückter Schalter | Türkonstellation |
| --- | --- |
| 1 |  |
| 2 |  |
| 3 |  |

##
<section data-background-iframe="https://www.inf-schule.de/modellierung/zustandsmodellierung/zustandsbasiertesysteme/erkundung_schaltsysteme/verhaltensbeschreibung/system3" data-background-interactive></section>
