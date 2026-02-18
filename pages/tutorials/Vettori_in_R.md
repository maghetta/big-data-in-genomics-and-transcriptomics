---
title: Vettori in R
---

```markdown
# Tutorial introduttivo all'oggetto di classe vettore in R

# Introduzione
# Questo tutorial ti guiderà nella scoperta dei vettori in R.
# Più precisamente, imparerai a:
# - Creare e manipolare vettori
# - Assegnare nomi agli elementi
# - Effettuare calcoli aritmetici e confronti
# - Selezionare specifici elementi di un vettore

# Creazione di vettori

# I vettori sono array monodimensionali che possono contenere dati di tipo
# numerico, carattere o logico. 
# Per creare un vettore in R abbiamo a disposizione la funzione `c()`,
# versione essenziale che sta per `concatenate`.

## A proposito cos'è una funzione?
# In R, **una funzione** è un blocco di codice progettato per eseguire
# un compito specifico. Le funzioni sono strumenti fondamentali per ridurre
# la duplicazione del codice, migliorare la leggibilità e organizzare le
# operazioni in modo modulare. Una funzione in R si riconosce sintatticamente
# perché il suo nome è immediatamente seguito da parentesi tonde, che possono
# contenere eventuali argomenti, ciascuno separato da virgola, da passare alla funzione.
# Ad esempio: `sum(7, 2)` restituisce la somma dei due numeri forniti come input.

# La funzione `c()` vuole come argomenti gli elementi che si vogliono
# concatenare per formare il vettore. Ad esempio:
vettore_numerico <- c(1, 2, 3)
vettore_carattere <- c("a", "b", "c")

# Ad esempio, creiamo un vettore  delle distanze e uno dei costi settimanali
# per diversi spostamenti fatti durante un viaggio:
vettore_distanze <- c(140, 50, 120, 300, 240) # in chilometri
vettore_costi <- c(30, 10, 50, 100, 80) # in euro

# Assegnazione dei nomi agli elementi di un vettore

# Usiamo la funzione `names()` per assegnare un nome agli elementi di un vettore.
# Ad esempio, potremmo nominare gli elementi dei vettori appena creati con i
# giorni della settimana.
giorni <- c("Lunedì", "Martedì", "Mercoledì", "Giovedì", "Venerdì")
names(vettore_distanze) <- giorni
names(vettore_costi) <- giorni

# Operazioni con i vettori

# Vettori di tipo numerico possono essere trattati in R come potrebbero essere
# trattati dei semplici numeri. Ad esempio, possono essere usati per effettuare
# delle operazioni. Una nota importante: in R se effettui una operazione matematica
# tra due vettori, questa viene effettuata `elemento per elemento`. Vediamo alcuni esempi.

# Dividiamo i costi per le distanze utilizzando l'operatore `/`.
# La divisione tra due vettori viene effettuata elemento per elemento,
# ovvero il primo elemento del primo vettore viene diviso per il primo
# elemento del secondo vettore, il secondo elemento per il secondo, e così via.
# Ad esempio, se `vettore_costi` è c(30, 10, 50) e `vettore_distanze` è c(140, 50, 120),
# il risultato sarà c(30/140, 10/50, 50/120).
costo_medio_km <- vettore_costi / vettore_distanze

#--> domanda per te: cosa succede invece in questo comando R?
vettore_costi / 5


# Utilizziamo ora la funzione `sum()` per calcolare le somme totali.
totale_distanze <- sum(vettore_distanze)
totale_costi <- sum(vettore_costi)
costo_totale_medio <- totale_costi / totale_distanze

# Per comprendere meglio le operazioni appena compiute, stampa a video
# il contenuto della variabile risultato
# Per stampare il contenuto di una variabile puoi usare la funzione `print()`
# dando come argomento il nome della variabile di cui vuoi stampare il contenuto.
# Alternativamente, puoi anche digitare semplicemente il nome della variabile
# e premere invio.

#--> domanda per te: prova a utilizzare la funzione `print()` per stampare a video
# il contenuto della variabile totale_distanze


# Selezione degli elementi dai vettori

# Esistono varie modalità per selezionare elementi di interesse da un vettore,
# elencati qui di seguito. Nota come ogni volta che si voglia estrarre
# degli elementi da un vettore, compariranno le parentesi quadre.
# Sintatticamente troverai sempre il nome del vettore da cui vuoi estrarre
# elementi seguito immediatamente da parentesi quadre, con all'interno specificati,
# esplicitamente o in forma di condizione, gli elementi da estrarre.

# 1. Tramite indici di posizione degli elementi di interesse
vettore_distanze[1:3]  # Seleziona i primi tre elementi

# Piccolo inciso: nel codice qui sopra, nota il simbolo `:` che viene utilizzato
# in R per generare sequenze di numeri interi continui, creando un intervallo
# con incrementi di uno tra un valore iniziale e uno finale.
# Esempio:
1:5 # Genera la sequenza 1, 2, 3, 4, 5
5:1  # Genera la sequenza 5, 4, 3, 2, 1 (decrescente)

# 2. Tramite i nomi degli elementi (se presenti)
vettore_distanze[c("Lunedì", "Martedì")]  # Seleziona elementi con i nomi specificati

# 3. Tramite condizioni logiche
vettore_distanze[vettore_distanze > 100]  # Seleziona elementi maggiori di 100

# 4. Utilizzando funzioni come which()
vettore_distanze[which(vettore_distanze == max(vettore_distanze))]  # Seleziona l'elemento massimo
vettore_distanze[which(vettore_distanze == min(vettore_distanze))]  # Seleziona l'elemento minimo

#--> domanda per te: seleziona gli elementi del vettore_costi corrispondenti
# ai giorni di Martedì, Mercoledì e Giovedì.
# Scrivi qui di seguito il codice R che puoi utilizzare per farlo.


# Usiamo gli indici o i nomi per selezionare elementi specifici.
distanze_metà_settimana <- vettore_distanze[2:4]
costi_metà_settimana <- vettore_costi[2:4]
distanze_inizio_settimana <- vettore_distanze[c("Lunedì", "Martedì", "Mercoledì")]
media_distanze_inizio <- mean(distanze_inizio_settimana)

# Operatori di confronto e selezione di elementi basata su condizioni

# Quanto sopra visto riguardo alla possibilità di applicare operazioni
# matematiche a vettori numerici vale anche per gli operatori di confronto
# (`<`, `>`, `==`, `!=`, `<=`, `>=`). Anche qui, i confronti verranno
# eseguiti elemento per elemento.  

# Filtriamo i giorni con distanze superiori a 100 km.
vettore_selezione <- vettore_distanze > 100
giorni_distanze_lunghe <- vettore_distanze[vettore_selezione]

#--> domande per te:
# che tipo di vettore è il vettore_selezione?
# sapresti spiegare come R stia usando gli elementi del
# vettore_selezione per estrarre alcuni elementi del vettore distanze?

# Ripetiamo la selezione per i costi.
vettore_selezione <- vettore_costi > 50
giorni_costi_alti <- vettore_costi[vettore_selezione]

#--> domandona per te: se `mean()` è una funzione che restituisce
# la media dei valori di un vettore dato come suo argomento,
# sapresti scrivere il codice R che assegna ad un vettore chiamato
# `sopra_media` gli elementi del vettore_costi che eccedono
# la media dei costi registrati nella settimana?

# Mettiamo ora insieme confronti e selezione di elementi.
# Ad esempio, individuamo in quali giorni della settimana
# si sono registrati il costo massimo e minimo.
costo_massimo <- max(vettore_costi)
costo_minimo <- min(vettore_costi)
giorno_costo_max <- names(vettore_costi)[vettore_costi == costo_massimo]
giorno_costo_min <- names(vettore_costi)[vettore_costi == costo_minimo]

#--> domande per te:
# in quale giorno della settimana si è registrato il costo massimo?
# in quale giorno il costo minimo?

```
