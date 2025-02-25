% Akzeptoren

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

## Definition eines Akzeptors
Ein Akzeptor ist (mindestens) ein 5-Tupel  
$A=(Q,\Sigma , \delta , q_0, F)$ mit  

- <div class="fragment fade-in">$Q$: eine endliche Menge von Zuständen</div>
- <div class="fragment fade-in">$\Sigma$: das Eingabealphabet</div>
- <div class="fragment fade-in">$\delta$: die Übergangsfunktion $\delta : Q\times \Sigma \rightarrow Q$</div>
- <div class="fragment fade-in">$q_0\in Q$: der Startzustand</div>
- <div class="fragment fade-in">$F\subseteq Q$: die akzeptierenden Zustände</div>

##  
<section data-background-iframe="https://www.inf-schule.de/sprachen/sprachenundautomaten/spracherkennung/endlicherautomat/fallstudie_zahlen/zustandsbasiertessystem" data-background-interactive></section>
