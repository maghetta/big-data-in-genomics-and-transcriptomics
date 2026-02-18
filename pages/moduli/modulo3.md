---
title: Modulo 3
---

![modulo3](images/modulo3/modulo3.jpg)

<br>

## Argomenti

- *Data Frames in R, cioé il capitolo 5 del [corso di Introduzione a R di DataCamp](https://www.datacamp.com/courses/free-introduction-to-r)*

- *Grafici in R (vedi istruzioni nel box più in basso su questa stessa pagina)*

<br>
<br>

## Obiettivi conoscitivi

Al termine di questa attività dovresti essere in grado di:

- descrivere cos'è e come si crea un data.frame in R

- elencare almeno una differenza tra matrici e data.frames in R

- caricare un data.frame di dati di esempio (*mtcars*) nella console R 

- stampare a video nella console di R le prime o le ultime righe di un data.frame

- ispezionare la struttura di un data.frame

- creare un data.frame in R

- selezionare gli elementi di un data.frame (es. 1+ righe e/o 1+ colonne) utilizzando l'indice numerico di righe e colonne

- selezionare gli elementi di un data.frame (es. 1+ righe e/o 1+ colonne) utilizzando il nome di righe e colonne

- selezionare una colonna di un data.frame utilizzando il simbolo $

- selezionare un sottinsieme di dati di un data.frame (es. 1+ righe o 1+ colonne) utilizzando un vettore logico

- riordinare le righe di un data.frame (es. secondo valori crescenti o decrescenti di un dato vettore)  

<br>

## Durata e programma dell'attività:

4 ore;

<table border="1" width="700">
	<tr>
		<td>[35']</td>
		<td>Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa</td>
	</tr>
	<tr>
	<td colspan="2">5'</td>
	</tr>
	<tr>
		<td>[40']</td>
		<td>Svolgimento corso R online (capitolo 5 del corso di DataCamp)</td>		
	</tr>
	<tr>
		<td>[30']</td>
		<td>Sfide interattive sul contenuto del capitolo 5</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 15'</td>
	</tr>
	<tr>
		<td>[20']</td>
		<td>Svolgimento del tutorial sui grafici in R (scorri questa pagina per trovarlo)</td>		
	</tr>
	<tr>
		<td>[30']</td>
		<td>Svolgimento sfida tremendissima  (scorri questa pagina per trovarla)</td>		
	</tr>
	<tr>
		<td>[20']</td>
		<td>Sfide interattive sul contenuto del capitolo 2</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 15'</td>
	</tr>
	<tr>
		<td>[20']</td>
		<td>Spazio per domande e curiosità</td>		
	</tr>
	<tr>
		<td>[10']</td>
		<td>Conclusioni</td>		
	</tr>
</table>


<hr>

Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa

<br>



1. Abbiamo visto un altro modo di accedere ad una console di R per fare i propri esercizi: la console di R del corso di DataCamp

![modulo3_datacamp](images/modulo3/dataCamp1.png)

- Sia l'editor di testo (riquadro in alto a dx della finestra di lavoro di DataCamp) che la console di R (riquadro in basso a dx della finestra di lavoro di DataCamp) possono essere usati anche per svolgere propri esercizi (ad esempio, per scrivere e testare il codice R richiesto come compito alla fine di ciascun modulo di PCTO).

- Ad esempio, nella foto allo schermo riportata qui sopra si può leggere nell'editor un testo indipendete dall'esercizio del corso di DataCamp.

- Per eseguire un codice a proprio piacimento e da te scritto nell'editor di DataCamp (riquadro in alto a dx) --> premi sul tasto "Run Code" e ne vedrai apparire il risultato nella console di R deella stessa schermata di DataCamp  (riquadro in basso a dx)

<br>

2. Abbiamo conosciuto il secondo tipo di "oggetto" di R: la matrice

![modulo3_datacamp](images/modulo3/dataCamp2.png)

A proposito: secondo te, posso avere colonne di classe diversa in una matrice? Perché (perché si o perché no)?

<br>

3. Qua e là tra i capitoli abbiamo anche conosciuto

diversi altri esempi di funzioni disponibili in R, quali: *matrix(), rownames(), colnames(), rowSums(), colSums(), ls(), cbind(), rbind()*

<hr>

## Svolgimento corso R online (capitolo 5)


- Nel capitolo 5 (*Data.Frames*) imparerai a creare un data frame, selezionare solo alcuni elementi di esso che ti interessano e ordinarlo in funzione di certe variabili. Questo tipo di oggetto, che può ospitare dati eterogenei nelle sue diverse colonne, è il tipo di oggetto R di uso più comune per immagazzinare la maggior parte dei set di dati con cui ci si può trovare a lavorare, che spesso includono colonne di varia natura (esempio, colonna di dati di tipo numerico alternata a colonna di dati categorici).


<hr>


***Come riprendere il corso di Introduzione a R su DataCamp da dove lo si aveva interrotto***
<br>
Per riprendere il corso di R su DataCamp al capitolo 5 --> segui i passaggi illustrati nel <a href="https://maghetta.github.io/Corso-R-livello-base/modulo2">[modulo 2]</a> alla sezione intitolata


<hr>

## Grafici in R

<hr>

**Andiamo a leggere** la guida su come creare grafici con R che trovi qui: [https://www.html.it/pag/67232/grafici-con-r/](https://www.html.it/pag/67232/grafici-con-r/)

Vedrai che la guida include dei **blocchi di codice R** (evidenziati come box su sfondo grigio nella guida): 

- esegui nella console R ciascuno di questi blocchi di codice, provando anche a modificare il codice (ad esempio cambiando il colore suggerito in altro)


<hr>

<span style="color:red;">Sfida tremendissima</span>

**Premessa:**
<br>

Per risolvere questa sfida tremendissima **ti servirà una console di R**. Se non ne hai una installata in locale sul tuo PC (ad esempio, disponibile da RStudio), **puoi usare quella del corso di DataCamp**.

<br>

**Pronti? Via!**

<br>

Sicuramente ti sarà capitato in questi anni complicati di vedere uno di quei grafici, in rete o in televisione, che fotografa la situazione in Italia delle vaccinazioni contro il Sars-CoV-2, cioé il virus responsabile della malattia covid-19.

Ebbene, questi dati sulle vaccinazioni effettuate in Italia, direttamente forniti dal Ministero della Salute, sono pubblicamente disponibili in rete e continuamente aggiornati, ad esempio su questa pagina GitHub ([https://github.com/italia/covid19-opendata-vaccini](https://github.com/italia/covid19-opendata-vaccini)).


La bellezza di R nel maneggiare file di dati è che sa andarseli a prendere anche direttamente dalla rete.

Per esempio, i dati più aggiornati sulle vaccinazioni effettuate in Italia sono disponibili in formato csv (comma-separated value) a questo link:

[https://raw.githubusercontent.com/italia/covid19-opendata-vaccini/master/dati/anagrafica-vaccini-summary-latest.csv](https://raw.githubusercontent.com/italia/covid19-opendata-vaccini/master/dati/anagrafica-vaccini-summary-latest.csv)


Li puoi caricare direttamente dalla rete in uno spazio di lavoro R con il seguente comando:

*urlcsv <- "[https://raw.githubusercontent.com/italia/covid19-opendata-vaccini/master/dati/anagrafica-vaccini-summary-latest.csv](https://raw.githubusercontent.com/italia/covid19-opendata-vaccini/master/dati/anagrafica-vaccini-summary-latest.csv)"*

*X <- read.csv(url(urlcsv), header=1)*

1. Comincia la sfida eseguendo le 2 righe di codice qui sopra, così da creare il data.frame X nel tuo spazio di lavoro.

2. Utilizza almeno un paio di funzioni che hai appreso nel modulo di oggi per: ispezionare la struttura del data.frame X e stamparne a video le prime righe (**domanda tremendissima**: *quante variabili sono presenti in questo data.frame?*)

Crea un sottoinsieme di dati chiamato Xmf che contenga solo le colonne "m" e  "f" del data.frame X (**domanda tremendissima**: *che tipo di oggetto è l'oggetto Xmf che hai appena creato?*)

Assegna come nomi delle righe dell'oggetto Xmf i valori della colonna "eta" del data.frame X

Usa un operatore di confronto tra quelli che hai visto nel capitolo 2 del corso di DataCamp per vedere in quale fasce di età ci sono più vaccinati  tra le donne che tra gli uomini

Hai ancora energie??? Allora crea un altro sottoinsieme di dati chiamato Xaltro che contenga solo la colonna "db3" del data.frame X. Assegna come nomi al vettore Xaltro che hai appena creato i valori della colonna "eta" del data.frame X

Fai un grafico a torte di Xaltro (**domanda tremendissima**: quale fascia di età è più rappresentata nella categoria "db3" dei vaccinati ?)


Beh, già se sei arrivato a leggere fin qui ti faccio i complimenti per il coraggio e la tenacia!!!
