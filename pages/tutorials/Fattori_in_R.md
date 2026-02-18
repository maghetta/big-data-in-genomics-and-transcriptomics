---
title: Fattori in R
---

```markdown

## Tutorial introduttivo all'oggetto di classe fattore in R

# Questo tutorial ti guiderà nella scoperta dei fattori in R. Più precisamente, imparerai a:
# - Riconoscere tipi di dati per i quali è utile ricorrere ai fattori
# - Creare e manipolare fattori, ordinati e non
# - Assegnare i nomi agli elementi di un fattore
# - Selezionare specifici elementi di un fattore


## Introduzione ai Fattori

# Certe volte i dati che ci troviamo ad analizzare possono essere raggruppati
# in un certo numero di categorie.
# Per esempio, i film possono essere raggruppati per genere (commedia, horror, avventura...).
# In R, le `variabili di tipo categorico` sono salvate in oggetti di classe `fattore`,
# cioè speciali vettori caratterizzati dalla presenza di `livelli`
# (ossia, le categorie presenti nella variabile categorica considerata). 

# Quindi, il termine `fattore` si riferisce ad un particolare tipo di oggetto utilizzato
# per immagazzinare variabili di tipo categorico. La differenza tra una variabile di
# tipo categorico e una variabile di tipo continuo consiste nel fatto che la variabile
# categorica può appartenere a un numero limitato di categorie.
# Una variabile di tipo continuo, al contrario, può assumere infiniti valori.

# Permettere a R di sapere se sta operando su variabili di tipo categorico o continuo può essere
# molto importante ad esempio nel caso di modelli statistici che trattano i due tipi di variabile
# in modo molto diverso.

### Creare un Fattore

# Per creare un fattore in R si utilizza la funzione `factor()`.
# La prima cosa da fare è creare un vettore che contenga tutte le osservazioni di interesse.
# Per esempio, `vettore_genere` contiene il genere di 5 differenti film:

vettore_genere <- c("Commedia", "Horror", "Avventura", "Commedia", "Horror")

# Per convertire il vettore_genere in un fattore, applica la funzione `factor()`
fattore_vettore_genere <- factor(vettore_genere)

#--> domanda per te: Stampa a video il contenuto della variabile fattore_vettore_genere.
#                            Cosa noti di diverso rispetto a un vettore?


#--> domanda per te: Adatta la procedura vista qui sopra per creare un fattore dei risultati
#                            di un'ipotetica intervista a 5 neo-laureati
#                            sulla presenza o meno di lode nella loro votazione di laurea



### Tipi di Variabili Categoriche

# Esistono due tipi di variabili categoriche:
# le `variabili categoriche nominali` e le `variabili categoriche ordinali`.

# Una variabile categorica nominale è una variabile che non possiede un ordine naturale.
# Per esempio, pensa alla variabile categorica `vettore_animali` contenente le categorie
# "Elefante", "Lupo", "Cane" e "Criceto".
# In questo caso è abbastanza difficile ordinare le categorie.

# In senso opposto, le variabili categoriche ordinali hanno un ordine naturale.
# Considera la variabile categorica `vettore_gradimento` con le categorie
# "Basso", "Medio" e "Alto". Qui è abbastanza ovvio che, in un certo senso,
# "Medio" si trova sopra a "Basso" e "Alto" si trova sopra a "Medio".

### Cambiare i Livelli dei Fattori

# Alcune volte ti capiterà di voler cambiare il nome dei livelli di un fattore,
# per ragioni di chiarezza (o altro). R ti permette di effettuare questa operazione
# utilizzando la funzione `levels()`. Questa funzione può essere utilizzata sia per
# visualizzare i livelli di un fattore, sia per modificarli

# Codice per costruire un vettore che contenga - abbreviati all'iniziale - i generi di 5 film
vettore_genere <- c("C", "H", "A", "C", "H")
factor_vettore_genere <- factor(vettore_genere)

#--> domanda per te: stampa a video il contenuto della variabile
# factor_vettore_genere appena creata


# Riassegna i valori ai livelli di factor_vettore_genere
levels(factor_vettore_genere) <- c("Avventura", "Commedia", "Horror")

#--> domanda per te: cosa hai fatto con quest'ultimo comando?

#--> altra domanda per te: Stampa a video i livelli della variabile
# factor_vettore_genere utilizzando la funzione `levels()`.
# Che cosa ti ricorda? Che tipo di oggetto?
# (Suggerimento: in R tutto è un oggetto, e tutto si ricicla!)


# Assegnare i nomi agli elementi di un fattore

# In modo del tutto simile a quanto visto per i vettori,
# possiamo assegnare nomi agli elementi
# di un fattore in R utilizzando la funzione `names()`.
# Ecco un esempio di codice R che illustra come farlo:

# Creiamo un vettore fattore di esempio
factor_vettore_gradimento <- factor(c("Alto", "Medio", "Basso", "Alto", "Medio", "Alto"))

# Assegniamo nomi agli elementi del fattore
names(factor_vettore_gradimento) <- c("Algebra", "Informatica", "Storia Contemporanea", "Biologia", "Genetica", "Fisica")


# Selezione di elementi da un fattore

# Anche in questo caso, possiamo selezionare elementi di un fattore
# in modo del tutto simile a quanto visto per i vettori.
# A questo proposito, mettiti alla prova: utilizzando il vettore
# factor_vettore_gradimento appena creato, e le modalità di selezione
# apprese nel tutorial sui vettori, prova a completare tu con il codice
# appropriato un esempio del il tipo di selezione indicata nei commenti. 

# 1. Estrazione di un singolo elemento per indice di posizione
# Ad esempio, estrai il primo elemento del fattore factor_vettore_gradimento


# 2. Estrazione di un singolo elemento per nome
# Ad esempio, estrai l'elemento nominato "Fisica" del fattore factor_vettore_gradimento

# 3. Estrazione di più elementi per posizione
# Ad esempio, estrai gli elementi da 3 a 5 del fattore factor_vettore_gradimento

# Ora esageriamo: pensando che tutto è un oggetto in R, ti viene in mente come estrarre
# gli elementi 1, 3, e 5 del fattore factor_vettore_gradimento?

# 4. Estrazione di elementi con una condizione logica
# Ad esmpio: estrai gli elementi del fattore factor_vettore_gradimento che contengono
#  come valore "Alto"



# Ottenere un Sommario di un Fattore

# In R, la funzione `summary()` ti permette di ottenere un'overview
# del contenuto di una variabile. Vediamo ad esempio quale risultato
# dia questa funzione applicata ad un oggetto di classe fattore.

# Crea factor_vettore_genere
vettore_genere <- c("C", "H", "A", "C", "H")
factor_vettore_genere <- factor(vettore_genere)
levels(factor_vettore_genere) <- c("Avventura", "Commedia", "Horror")

# Genera sommario per vettore_genere
summary(vettore_genere)

# Genera sommario per factor_vettore_genere
summary(factor_vettore_genere)


# Fattori Ordinali

# Vediamo ora come sfruttare meglio l'ordine naturale che appartiene alle
# variabili di tipo categorico ordinale, modificando l'oggetto di classe
# fattore perché tenga conto di questa ulteriore caratteristica. Vediamo
# infatti come creare fattori ordinali. Diciamo che sei a capo di un gruppo
# che valuta il gradimento dei corsi erogati e vuoi classificare il livello
# di gradimento come "Basso", "Medio" o "Alto".
# Salvi i risultati in un vettore chiamato `vettore_gradimento`.

#---> domanda per te: Crea vettore_gradimento che contenga i risultati
# delle interviste a 5 studenti

# Converti vettore_gradimento in un fattore ordinale
factor_vettore_gradimento <- factor(vettore_gradimento, ordered = TRUE, levels = c("Basso", "Medio", "Alto"))

#--> domanda per te: Dai uno sguardo al contenuto di factor_vettore_gradimento.
# Cosa noti di diverso?
factor_vettore_gradimento


# Confrontare Due Fattori Ordinali

# Il fatto che `factor_vettore_gradimento` sia un ordinale ci permette
# di comparare i suoi elementi.
# Per effettuare il confronto, utilizza semplicemente gli operatori di
# confronto già incontrati in precedenza.


# Valore del fattore per il secondo corso
val2 <- factor_vettore_gradimento[2]

# Valore del fattore per il quinto corso
val5 <- factor_vettore_gradimento[5]

# Il secondo corso è più gradito del quinto?
val2 > val5

#--> domandaccia per te: prova a scrivere un codice R per scoprire quali elementi
# del fattore factor_vettore_gradimento hanno ricevuto un alto gradimento

```

