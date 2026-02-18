---
title: Modulo 2
---

![modulo2](images/modulo2/modulo2.jpg)

<br>

## Argomenti

- Matrici in R, cioé il capitolo 3 del corso di Introduzione a R di DataCamp

<hr>

## Obiettivi conoscitivi

Al termine di questa attività dovresti essere in grado di:

- descrivere cos'è e come si crea una matrice in R

-assegnare i nomi alle righe e/o alle colonne di una matrice

- calcolare la somma degli elementi di ogni riga o di ogni colonna di una matrice numerica

- aggiungere una o più colonne ad una matrice

- aggiungere una o più righe ad una matrice

- ispezionare il contenuto del tuo spazio di lavoro (workspace)

- selezionare gli elementi di una matrice

- effettuare delle operazioni matematiche (es. +, -, /, \*) con matrici numeriche



## Durata e programma dell'attività:

4 ore;

<table border="1" width="700">
	<tr>
		<td>[50']</td>
		<td>Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa</td>
	</tr>
	<tr>
	<td colspan="2">pausa 15'</td>
	</tr>
	<tr>
		<td>[45']</td>
		<td>Svolgimento corso R online (capitolo 3 del corso di DataCamp)</td>		
	</tr>
	<tr>
		<td>[45']</td>
		<td>Sfide interattive sul contenuto del capitolo 3</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 15'</td>
	</tr>
	<tr>
		<td>[40']</td>
		<td>Spazio per domande e curiosità</td>		
	</tr>
	<tr>
		<td>[15']</td>
		<td>Conclusioni</td>		
	</tr>
	<tr>
		<td>[15']</td>
		<td>Uno sguardo al prossimo Modulo: Data Frames vs. Matrici</td>		
	</tr>
</table>


<br>

<hr>


### Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa

1. Abbiamo cominciato ad usare la console di R

![datacamp](images/modulo2/datacamp1.png)

<br>

schema della finestra di lavoro del corso R su DataCamp

NOTA: 

- i riquadri (1), (2) e (4) sono specifici del sito di  DataCamp.

- (3) e (5) rappresentano 2 elementi fondamentali della programmazione in R, in particolare:

	1. Il riquadro (3) fornisce un editor di testo (software per scrivere il tuo codice R)

	2. Il riquadro (5) fornisce la console R: ambiente interattivo in grado di ricevere e interpretare le righe di comando scritte utilizzando la sintassi del linguaggio R

Nota: 

- un editor di testo non è strettamente fondamentale. Puoi anche digitare i tuoi comandi R direttamente nella console interattiva e premere invio per eseguirli. Però i comandi digitati direttamente in console verranno dimenticati quando chiudi la sessione di lavoro.

- di solito un codice R per svolgere un certo obiettivo lo si costruisce avendo aperti davanti un editor di testo e la console di R. Sulla console di R puoi testare il comando (esempio: il comando per creare un vettore), una volta trovata la riga di codice che funziona, la puoi annotare nell'editor di testo per conservarla. E magari integrarla con una riga di commento che ne spieghi il senso. Il codice così costruito nell'editor di testo lo puoi salvare con un nome (es. "mio_primo_script.R") per conservarlo sul tuo PC. L'estensione del nome del file ".R" (in maiuscolo o in minuscolo) viene convenzionalmente usato per specificare che quel dato file di testo semplice contiene istruzioni scritte nel linguaggio R ed eseguibili se lette da un interprete R.


<table>
	<tr>
		<td><iframe src="https://rdrr.io/snippets/embed/" width="800" height="600"></iframe></td>
		<td>Emulatore della console di R disponibile gratuitamente online al link: <a href="https://rdrr.io/snippets/"><(https://rdrr.io/snippets/)</a></td>
	</tr>
</table>

2. **Abbiamo conosciuto l'utilizzo di base della console di R, come un semplice calcolatore**

![datacamp](images/modulo2/datacamp2.png)

A proposito: cos'è una variabile? E come la creo in R?

3. **Abbiamo conosciuto i primi due tipi di "oggetto" di R: il vettore e il fattore**

![datacamp](images/modulo2/datacamp3.png)

A proposito: in cosa si somigliano e in cosa si differenziano, ad esempio, un vettore e un fattore?

![modulo3_datacamp](images/modulo3/dataCamp3.png)

A proposito, sapresti farmi un esempio di variabile fattoriale nominale? e un esempio di variabile fattoriale ordinale?



Una perla di saggezza: in R tutto è un oggetto (sia esso un vettore, un fattore, o... altri oggetti che conosceremo nelle prossime puntate). A proposito: i nomi di un vettore, che tipo di oggetto sono?

4. **Qua e là tra i capitoli abbiamo anche conosciuto**

- alcuni esempi di funzioni disponibili in R (quali: c(), class(), mean(), factor(), levels(), summary() )

- come riconoscere una funzione in un codice R (a proposito, come la riconosci una funzione? che caratteristica ha?)

- l'importanza delle parentesi e il loro diverso significato in R (quando hai visto una parentesi tonda? quando una parentesi quadra?)

- il simbolo "<-" (che chiamiamo di assegnazione) per creare una variabile (la scelta del nome di una variabile è obbligato o a piacere?)

- l'esistenza di "parole speciali" utilizzate in R, come ad esempio TRUE, FALSE, NA

<hr>

**Svolgimento corso R online (capitoli 3)**


- Nel capitolo 3 (Matrici) imparerai come utilizzare le matrici in R. Alla fine del capitolo, avrai appreso come creare matrici e come effettuare le operazioni di bases su di esse. 

<hr>

**Come riprendere il corso di Introduzione a R su DataCamp da dove lo si aveva interrotto**

<hr>

Per riprendere il corso online "Introduzione a R" su DataCamp, segui le istruzioni fornite <a href="https://maghetta.github.io/Corso-R-livello-base/premessa">a questo link</a>.

NOTA: possono comparire durante lo svolgimento del corso online - soprattutto al completameno di un capitolo - messaggi promozionali. Scegli sempre di chiudere il messaggio (quando possibile, facendo click sulla X in alto a destra del messaggio. Oppure facendo click al difuori del riquadro di pubblicità).

<hr>


**Esercizi**
<br>

1. Quale comando si può utilizzare in R per visualizzare il contenuto del proprio spazio di lavoro?

- *a. dir()*
- *b. read()*
- *c. ls()*
- *d. list()*


2. Il comando  c(1, TRUE,"A") genera in R un vettore di che tipo?

- *a. Numerico.*
- *b. Logico.* 
- *c. Carattere.*

<br>

3. Risolvi la seguente espressione in R: (1-(5-4))+\{2^10/2^7-(6-(3\*2-10\/5))\} . Quanto fa? 


4. Voglio estrarre da un vettore chiamato "compiti" composto da 24 elementi, i valori corrispondenti alle posizioni 3, 11, 15 e 21. Scrivi il comando R opportuno per farlo.


5. La funzione rep() di R genera ripetizioni di un dato vettore tante volte quanto specificato nel parametro times. Ad esempio: *rep( c(1,0,2), times=2)* genererà il seguente output:  *1 0 2 1 0 2*. Usa il comando *rep()* per generare il seguente vettore: *1 0 1 0 1 0 1 0 1 0 1 0*


6. Scrivi 3 righe di codice R che facciano quanto segue: (1) creare un vettore denominato "regioni" che contiene gli elementi "Sicilia", "Lombardia" e "Liguria"; (2) aggiungere a questo vettore l'elemento "Molise"; (3) stampare a video il contenuto del vettore regioni. 


7. Risolvi la seguente espressione in R: *-3 x 5<sup>6</sup> + 3<sup>2-2</sup> x 2<sup>2</sup> -(-2)<sup>2</sup>*. Quanto fa?


8. La funzione dim() di R ti permette di conoscere le dimensioni di un oggetto multidimensionale, come ad esempio una matrice (che ha 2 dimensioni). Considerando la seguente matrice: *m = matrix(-31:100, ncol=6)*, applica la funzione dim() alla matrice m per vedere che dimensioni ha. Poi, calcola il valore medio della sua 5a riga.


9. Crea un vettore denominato x con i seguenti elementi: *3,4,5,6,6,5,2,2,6,7,8,2,3,2,5,4,5,9*; Poi calcola la media e la lunghezza del vettore x.


10. Crea un fattore ordinato denominato *geografia* che contenga le seguenti valutazioni di uno studente in geografia nei tre anni delle scuole medie: *ottimo, buono, buono, discreto, ottimo, insufficiente, buono*
