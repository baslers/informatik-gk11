% Sortieralgorithmen

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
    .footnotes {
      font-size:0.8em;
    }
    </style>
...

### Bubblesort
Pseudocodealgorithmus:
```
bubbleSort(Array A)
  for (n=A.size; n>1; --n){
    for (i=0; i<n-1; ++i){
      if (A[i] > A[i+1]){
        A.swap(i, i+1)
      } // Ende if
    } // Ende innere for-Schleife
  } // Ende äußere for-Schleife
```

Optimiert:
```
bubbleSort2(Array A)
  n = A.size
  do{
    swapped = false
    for (i=0; i<n-1; ++i){
      if (A[i] > A[i+1]){
        A.swap(i, i+1)
        swapped = true
      } // Ende if
    } // Ende for
    n = n-1
  } while (swapped)
```

^[Seite „Bubblesort“. In: Wikipedia, Die freie Enzyklopädie. Bearbeitungsstand: 29. Januar 2020, 08:56 UTC. URL: <https://de.wikipedia.org/w/index.php?title=Bubblesort&oldid=196297595> (Abgerufen: 23. Mai 2020, 15:26 UTC)]

### Bubblesort Beispiel
<img src=".\Abbildungen\Bubblesort.gif" style="max-width:100%">

^[By Swfung8 - Own work, CC BY-SA 3.0, <https://commons.wikimedia.org/w/index.php?curid=14953478>]

### Selectionsort
```
prozedur SelectionSort( A : Liste sortierbarer Elemente )
  hoechsterIndex = Elementanzahl( A ) - 1
  einfuegeIndex = 0
  wiederhole
    minPosition = einfuegeIndex
    für jeden idx von (einfuegeIndex + 1) bis hoechsterIndex wiederhole
      falls A[ idx ] < A[ minPosition ] dann
          minPosition = idx
      ende falls
    ende für
    vertausche A[ minPosition ] und A[ einfuegeIndex ]
    einfuegeIndex = einfuegeIndex + 1
  solange einfuegeIndex < hoechsterIndex
prozedur ende
```

^[Seite „Selectionsort“. In: Wikipedia, Die freie Enzyklopädie. Bearbeitungsstand: 22. März 2020, 16:47 UTC. URL: <https://de.wikipedia.org/w/index.php?title=Selectionsort&oldid=198005065> (Abgerufen: 23. Mai 2020, 15:27 UTC)]

### Selectionsort Beispiel
<img src=".\Abbildungen\Selectionsort.gif" style="max-width:100%">

^[By NullKomma00 - Own work, Public Domain, <https://commons.wikimedia.org/w/index.php?curid=9821204>]

### Mergesort
```
funktion mergesort(liste);
  falls (Größe von liste <= 1) dann antworte liste
  sonst
     halbiere die liste in linkeListe, rechteListe
     linkeListe = mergesort(linkeListe)
     rechteListe = mergesort(rechteListe)
     antworte merge(linkeListe, rechteListe)
     
funktion merge(linkeListe, rechteListe);
   neueListe
   solange (linkeListe und rechteListe nicht leer)
   |    falls (erstes Element der linkeListe <= erstes Element der rechteListe)
   |    dann füge erstes Element linkeListe in die neueListe hinten ein und entferne es aus linkeListe
   |    sonst füge erstes Element rechteListe in die neueListe hinten ein und entferne es aus rechteListe
   solange_ende
   solange (linkeListe nicht leer)
   |    füge erstes Element linkeListe in die neueListe hinten ein und entferne es aus linkeListe
   solange_ende
   solange (rechteListe nicht leer)
   |    füge erstes Element rechteListe in die neueListe hinten ein und entferne es aus rechteListe
   solange_ende
   antworte neueListe
```

^[Seite „Mergesort“. In: Wikipedia, Die freie Enzyklopädie. Bearbeitungsstand: 20. März 2020, 22:53 UTC. URL: <https://de.wikipedia.org/w/index.php?title=Mergesort&oldid=197948614> (Abgerufen: 23. Mai 2020, 15:31 UTC)]

### Mergesort Beispiel
<img src=".\Abbildungen\Mergesort.png" style="max-width:100%">

^[Von --Jkrieger 9. Jul 2005 16:01 (CEST) - selbst gezeichnet, Bild-frei, <https://de.wikipedia.org/w/index.php?curid=793375>]

### Insertionsort
```
INSERTIONSORT(A)
1 for i = 1 to (Länge(A)-1) do
2      einzusortierender_wert = A[i]
3      j = i
4      while (j > 0) and (A[j-1] > einzusortierender_wert) do
5           A[j] = A[j - 1]
6           j = j − 1
7      end while
8      A[j] = einzusortierender_wert
9 end for
```

^[Seite „Insertionsort“. In: Wikipedia, Die freie Enzyklopädie. Bearbeitungsstand: 28. Februar 2020, 08:58 UTC. URL: <https://de.wikipedia.org/w/index.php?title=Insertionsort&oldid=197248100> (Abgerufen: 23. Mai 2020, 15:34 UTC)]

### Insertionsort Beispiel
<img src=".\Abbildungen\Insertionsort.gif" style="max-width:200%">

^[By Swfung8 - Own work, CC BY-SA 3.0, <https://commons.wikimedia.org/w/index.php?curid=14961606>]
