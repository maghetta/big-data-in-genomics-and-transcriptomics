---
title: Liste in R
---

```markdown

## Introduzione alle liste in R

# In questo tutorial conoscerai l'ultimo tipo di oggetto fondamentale di R: le `liste`. Imparerai
# come crearle, e come manipolarle. Ad esempio come accedere ai suoi elementi, o nominarli.  
# Le liste in R sono oggetti flessibili che possono contenere come propri elementi diversi tipi di dati,
# inclusi vettori, matrici, data frame e persino altre liste.

## Creare una lista in R
# In R puoi creare una lista utilizzando il comando `list()`, a cui dovrai dare
# come argomenti separati da virgola l'elemento o gli elementi che vuoi inserire
# nella data lista. Es. `list(elemento1, elemento2, ecc.)`.
# Creiamo ad esempio una lista per organizzare gli ingredienti di una ricetta:

# Definiamo gli ingredienti principali come vettore
ingredienti <- c("Farina", "Uova", "Latte", "Zucchero", "Burro")

# Creiamo una matrice con le quantità degli ingredienti per 1 o 2 porzioni
quantita <- matrix(c(200, 2, 250, 100, 50, 400, 4, 500, 200, 100), 
                   nrow = 2, byrow = TRUE, 
                   dimnames = list(c("Dose 1", "Dose 2"), ingredienti))

# Creiamo un data frame con le informazioni nutrizionali per ogni ingrediente
# (per 100g):
info_nutrizionali <- data.frame(Ingrediente = ingredienti,
                                Calorie = c(364, 155, 42, 387, 717),
                                Proteine = c(10, 13, 3, 0, 1))

# Creiamo infine una lista che raccolga tutti questi dati:
ricetta <- list(ingredienti = ingredienti, 
                quantita = quantita, 
                info_nutrizionali = info_nutrizionali)

#--> domanda per te: stampa a video la variabile *ricetta* appena creata

# Potresti aver notato che abbiamo nominato gli elementi della lista nello
# stesso comando `list()` con cui l'abbiamo creata.

#--> domanda per te: che nome abbiamo dato agli elementi della lista *ricetta*?


## Ispezionare una lista
# Analogamente a quanto visto con i data frame, possiamo utilizzare la funzione `str()`
# per ispezionare la struttura di una lista.

#--> domanda per te: prova ad applicare la funzione `str()` per ispezionare la struttura
# della lista *ricetta* appena creata.


## Nominare gli elementi di una lista
# Oltre alla possibilità di nominare gli elementi di una lista all'interno del
# comando `list()`, possiamo visualizzare o rinominare gli elementi di una lista, 
# utilizzando la funzione `names()` già incontrata con i `vettori` e i `fattori`.

#--> domanda per te: prova a stampare a video i nomi degli elementi della lista *ricetta*

#--> domanda per te: con quale comando R potresti rinominare gli elementi della lista
#  *ricetta* in "Ingredienti", "Quantita" e "Info_nutrizionali" ?


## Selezione di elementi da una lista
# Possiamo accedere agli elementi della lista utilizzando sempre le parentesi `[]`,
# ma con una sintassi un pò diversa, che riflette la struttura delle liste.
# In particolare, utilizzeremo:
# - le parentesi `[]`: per una sottolista contenente 1+ elementi della lista originale
# - le doppie parentesi `[[]]`: per accedere ad un elemento specifico di una lista
# - le doppie parentesi `[[]]` seguite da parentesi `[]`: per selezionare elementi dall'oggetto
#    contenuto nell'elemento della lista selezionato.

# Vi sentite persi??! Vediamo degli esempi, molto più chiari delle parole!

#... Alcuni esempi della situazione #1: le parentesi `[]`:

#--> domanda per te: utilizzando la funzioni `length()` e `class()` verifica rispettivamente lunghezza e classe
#  di oggetto delle selezioni che andremo ad effettuare con i comandi qui sotto

ricetta[2]      # selezionerà una sottolista composta dal solo 2° elemento della lista *ricetta*
ricetta[c(1,3)] # selezionerà una sottolista composta dagli elementi 1 e 3 della lista *ricetta*
ricetta[2:3]    # selezionerà una sottolista composta dagli elementi 2 e 3 della lista *ricetta*

#... Alcuni esempi della situazione #2: le parentesi `[[]]`:
# Ricordi quando abbiamo detto che tutto in R è un oggetto? Utilizzando la funzione `class()`,
# verifica classe di oggetto delle selezioni che andremo ad effettuare con i comandi qui sotto

ricetta[[2]]    # estrarrà l'oggetto che costituisce il 2° elemento della lista *ricetta*
ricetta[[3]]    # estrarrà l'oggetto che costituisce il 3° elemento della lista *ricetta*
ricetta[[1]]    # estrarrà l'oggetto che costituisce il 1° elemento della lista *ricetta*

#... Alcuni esempi della situazione #3: le parentesi `[[]]` seguite da parentesi `[]`:
# Negli esempi qui sotto, come usare le parentesi `[]` dipenderà dal tipo di oggetto
# selezionato dalla lista attraverso l'uso delle parentesi `[[]]`. Ad esempio:

ricetta[[1]][4]    # selezionerà il 4° elemento del vettore *Ingredienti*
                   # che costituisce il 1° elemento della lista *ricetta*

ricetta[["Quantita"]][2,]  # selezionerà la 2a riga della matrice *Quantita*
                         # che costituisce il 2° elemento della lista *ricetta*

#--> domanda per te: prova ora tu ad estrarre dalla lista *ricetta*
#  la 2a e 3a colonna del data frame "Info_nutrizionali"

# Infine, puoi anche selezionare un elemento da una lista utilizzando il simbolo `$`.
# Ad esempio, selezioniamo l'elemento *Info_nutrizionali* dalla lista *ricetta* con `$`:

ricetta$Info_nutrizionali

#--> domandaccia per te: utilizzando la funzione `class()` per verificare la classe dell'oggetto
#    che hai appena selezionato con il comando qui sopra, equipareresti l'estrazione mediante
#    simbolo `$` alla estrazione con le parentesi `[]` o a quella con le parentesi `[[]]`?

## Aggiungere un nuovo elemento ad una lista

# Possiamo aggiungere un nuovo elemento in coda ad una lista con due sintassi alternative:
# `c(lista_attuale, nuovo_elemento)`  # cioè, utilizzando la funzione `c()` [NB: creerà una lista!]
# `lista_attuale$nuovo_nome <- nuovo_elemento`  # cioé, utilizzando `$` per creare e valorizzare una
#                                      posizione successiva all'ultima presente nella lista attuale

# Aggiungiamo ad esempio il tempo di cottura della ricetta, utilizzando le due sintassi alternative:
ricetta_completa <- c(ricetta, tempo_cottura = 30)
ricetta$tempo_cottura = 30

```
