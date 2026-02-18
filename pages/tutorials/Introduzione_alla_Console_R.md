---
title: Introduzione alla Console R
---

```markdown
# Tutorial introduttivo a R e all'uso della sua console interattiva

# In questo breve tutorial vedremo:
# - cos'è e come usare la console interattiva (o terminale interattivo) di R
# - come utilizzare R come una calcolatrice
# - come scrivere un commento in un codice R
# - cos'è una variabile e come crearla in R, o modificarne il valore
# - quali sono i tipi principali di variabili che si possono incontrare


## Terminale Interattivo di R

# R è spesso utilizzato tramite un terminale interattivo, noto anche come console R.
# Il terminale interattivo è un ambiente in cui è possibile digitare comandi R
# e vedere immediatamente mostrati i risultati.
# Questo è molto utile per testare rapidamente il codice e sperimentare.

# Per avviare il terminale interattivo di R, è possibile:

# 1. Avviare R dall'icona corrispondente sul nostro PC
# 2. Avviare R da una finestra di terminale (o prompt dei comandi)
# 3. Avviare RStudio e utilizzare la console R integrata nella sua interfaccia.

# NOTA: tutte e tre le opzioni qui sopra riportate prevedono che tu abbia
# una versione di R installata e funzionante sul tuo PC.
# Se poi scegliessi l'opzione #3, dovrai aver installato sul tuo PC anche RStudio.
# Se così non fosse, puoi vedere come installare R e/o RStudio ad esempio qui:
# https://rstudio-education.github.io/hopr/starting.html.
# Una volta avviato il terminale interattivo,
# un prompt (`>`), sarà il segnale che la console interattiva di
# R è pronta ad accettare ed eseguire i comandi digitati.

## A proposito del simbolo `#` che compare spesso in questo tutorial
# questo simbolo indica all’interprete di ignorare tutto il testo che segue
# sulla stessa riga. In altre parole, `#` serve a introdurre un commento,
# utile per annotazioni, spiegazioni o promemoria per chi legge lo script,
# senza influenzare l’esecuzione del codice.


## Uso di R come Calcolatrice

# R può essere utilizzato per eseguire semplici operazioni aritmetiche. Ecco alcuni esempi:

```R
# Somma
3 + 5

# Sottrazione
10 - 4

# Moltiplicazione
6 * 7

# Divisione
20 / 4

# Potenza
2^3

# Radice quadrata
sqrt(16)

## Variabili e Assegnazione

# In R, possiamo memorizzare i risultati delle operazioni in variabili. 
# Una variabile è un contenitore con un nome che rappresenta un valore. 
# Per assegnare il valore ad una variabile, in R si 
# utilizza il simbolo `<-` (o `=`). 
# Una variabile è un contenitore simbolico utilizzato per memorizzare un valore
# o un insieme di valori in un programma. 
# In R, una variabile può contenere diversi tipi di dati, quali ad esempio:
# numeri, stringhe, vettori, matrici, liste o data frame.

# Le variabili rendono il codice più flessibile e leggibile, permettendo 
# di riferirsi ai dati senza conoscerne direttamente il valore specifico, 
# come pure di modificare questo valore rispetto all'assegnazione iniziale.

```R
# Assegnazione di un valore a una variabile
x <- 5

# Utilizzo della variabile in un'operazione
y <- x + 3

# Stampa del valore della variabile
print(y)

## controllo delle variabili create / presenti nel proprio spazio di lavoro
# Per verificare quali variabili sono presenti nella sessione di lavoro R,
# puoi utilizzare la funzione 'ls()'.
# Ad esempio, prova a digitare:
ls()
# ls() restituisce un elenco dei nomi di tutti gli oggetti attualmente
# creati nella sessione R.



## Comandi incompleti e il prompt che si trasforma in `+`
# Prima abbiamo menzionato che il simbolo `>` caratterizza
# la console interattiva di R quando è pronta a ricevere ed
# eseguire comandi. Qualche volta capita invece, premendo invio, di
# trovarsi di fronte ad una riga che inizia con il simbolo `+`.
# Questo simbolo `+` indica che R sta aspettando il completamento
# del comando precedente. Succede ad esempio se ci si dimentica
# di chiudere una parentesi. Infatti, se non completi un comando,
# R aspetta che tu finisca di scriverlo e mostra il prompt
# come un `+` invece del solito `>`. Per uscire da questa situazione,
# concludi il comando oppure premi una delle seguenti opzioni:
# a) la combinazione 'ctrl + c' (se lavori su terminale R)
# b) tasto 'Esc' della tastiera (se lavori in RStudio)

# Prova ad esempio a digitare il seguente comando incompleto
# e premi il tasto invio per eseguirlo:
x <- c(1, 2, 3   # manca la parentesi chiusa

# Una volta chiusa la parentesi, il comando verrà eseguito correttamente




## Rivediamo tutto insieme in un esempio:

# Assegnazione di valori a variabili
a <- 10
b <- 2

# Operazioni aritmetiche
somma <- a + b
diffrenza <- a - b
prodotto <- a * b
quoziente <- a / b
potenza <- a^b
radice <- sqrt(a)

# Stampa dei risultati
print(paste("Somma:", somma))
print(paste("Differenza:", differenza))
print(paste("Prodotto:", prodotto))
print(paste("Quoziente:", quoziente))
print(paste("Potenza:", potenza))
print(paste("Radice quadrata:", radice))


## Principali Tipi di Variabili in R
# In R esistono quattro tipi principali di variabili: 
# ***numeric***, ***integer***, ***character*** e ***logical***. 
# Esempi di ciascun tipo di variabile sono forniti qui di seguito.
# Una funzione utile per conoscere la tipologia di dato contenuto 
# in una variabile è **class()**.

# 1. **Variabili Numeriche**
#  - **Interi**: Numeri senza decimali.
     x <- 10
     class(x)   # per controllare il tipo di variabile contenuto nella variabile 'x'
     x          # per stampare a video il contenuto della variabile x (o **print(x)**)
#   - **Numeri a virgola mobile (double)**: Numeri con decimali.
     x <- 10.5
     # con quale comando R puoi stampare a video il contenuto della variabile x ?
     # con quale comando R puoi conoscere il tipo della variabile x ?


# 2. **Variabili Carattere (Stringhe)**
   # Sequenze di caratteri racchiuse tra virgolette.
     x <- "Ciao, mondo!"
    

# 3. **Variabili Logiche (Boolean)**
   # Variabili che possono assumere solo due valori: `TRUE` o `FALSE`.
     x <- TRUE


# Stampa delle variabili
print(intero)   # ma anche, più semplicemente, digita il nome della variabile


## Conclusione
# In questo tutorial, abbiamo visto come usare R come calcolatrice, abbiamo introdotto
# i concetti di variabile e assegnazione, e visto i principali tipi di variabile.
```
