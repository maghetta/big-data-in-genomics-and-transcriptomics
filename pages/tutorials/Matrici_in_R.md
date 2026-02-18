---
title: Matrici in R
---

```markdown

### **Tutorial: Introduzione all'oggetto di classe `Matrice` in R**

#### **Che cos'è una matrice in R?**
# In R, una matrice è una collezione di elementi dello stesso tipo (numerico, carattere o logico)
# disposti in un numero fisso di righe e colonne.
# In questo tutorial lavoreremo con matrici bidimensionali, e prenderemo come spunto alcuni dischi famosi dei Pink Floyd

# Per creare una matrice in R, utilizziamo la funzione `matrix()`. Ecco un esempio:

matrix(1:9, byrow = TRUE, nrow = 3)

# **Il primo argomento** (`1:9`) rappresenta la sequenza di elementi da disporre nella matrice.
# **L'argomento `byrow`** specifica se riempire la matrice per riga (`TRUE`) o per colonna (`FALSE`)
# **L'argomento `nrow`** indica il numero di righe della matrice.

#### **Creiamo una matrice di esempio**
# Costruiamo ad esempio una matrice con i dati delle vendite di alcuni mitici album dei Pink Floyd.
# La nostra matrice avrà tre righe (una per ciascun album) e due colonne (vendite in Italia e nel mondo).

vendite_italia <- c(2.1, 2.5, 1.3)      # Vendite in Italia dei tre album, in milioni
vendite_mondo <- c(200, 240, 90.5)      # Vendite nel mondo dei tre album, in milioni

# Uniamo i dati in un unico vettore
vendite_totali <- c(vendite_italia, vendite_mondo)

#--> domande per te: che classe di oggetto ha la variabile `vendite_totali`? E quanto è lungo?

# Costruisci la matrice, disponendo gli elementi della variabile `vendite_totali` per riga
matrice_vendite <- matrix(vendite_totali, nrow = 3, byrow = FALSE,
                          dimnames = list(c("The Dark Side of the Moon", 
                                            "Wish You Were Here", 
                                            "Animals"), 
                                          c("Italia", "Mondo")))

#--> domanda per te: stampa a video la variabile `matrice_vendite`


#--> domandaccia per te: crea ora una aseconda matrice, chiamata `matrice_vendite_v2`, in cui nella prima colonna
#          ci siano le vendite degli album nel mondo, e nella seconda colonna le vendite in Italia



#### **Assegnare nomi alle righe e colonne**
# Anche nel caso delle matrici, puoi aggiungere nomi (o modificarli) al tuo oggetti in R.
# Nel caso di una matrice bidimensionale, potrai aggiungere nomi sia alle righe che alle colonne.

# Nell'esempio qui sopra degli album del Pink Floyd, abbiamo assegnato nomi alle due dimensioni
# della matrice direttamente mentre la costruivamo, specificandoli con l'argomento `dimnames`.
# Ma potevamo anche creare una matrice priva di nomi, e poi aggiungerli in un secondo momento.
# Ecco ad esempio la stessa matrice costruita prima con i soli numeri:

matrice_vendite <- matrix(vendite_totali, nrow = 3, byrow = FALSE)

# stampa a video il contenuto di questa matrice
matrice_vendite 

# Aggiungi ora i nomi sia alle righe che alle colonne di questa matrice "muta".
# Le funzioni di R da utilizzare per farlo sono, rispettivamente,`rownames()` e `colnames()`.

rownames(matrice_vendite) <- c("the dark side of the moon", "wish you were here", "animals")
colnames(matrice_vendite) <- c("italia", "mondo")

# ri-stampa a video il contenuto di questa matrice per vedere cosa è cambiato
matrice_vendite 

#--> domanda per te: stampa ora solo i nomi delle righe e poi i nomi delle colonne

# Immagina di esserti reso/a conto di aver dimenticato le maiuscole. Con le stesse funzioni
# possiamo rinominare sia righe che colonne, così:

rownames(matrice_vendite) <- c("The Dark Side of the Moon", "Wish You Were Here", "Animals")
colnames(matrice_vendite) <- c("Italia", "Mondo")

# ancora una volta, stampa a video il contenuto di questa matrice per vedere cosa è cambiato



#### **Operazioni per riga e per colonna**
# Per calcolare i totali delle vendite, sommiamo i valori su ogni riga usando la funzione `rowSums()`.

totali_album <- rowSums(matrice_vendite)
totali_album

#---> domanda per te: che classe di oggetto è la variabile `totali_album`? E, ti è chiaro cosa ha fatto
# la funzione `rowSums()`?

# Esistono altre funzioni, analoghe a `rowSums()` per eseguire operazioni ricorrenti per riga o per colonna,
# quali ad esempio: `rowMeans()`, o `colSums()` e `colMeans()`

# Queste sono solo operazioni molto usate per cui qualcuno ha creato apposita funzione.
# In realtà, la sintassi estesa, che permette di applicare qualsiasi funzione per riga o per colonna, è la seguante:

apply(matrice_vendite, 1, sum)  # nota come in questo caso scrivo il nome della funzione, senza parentesi `()`
apply(matrice_vendite, 2, mean)

# La funzione di R `apply()` permette di applicare una funzione a tutte le righe o colonne di una matrice
# **Il primo argomento** (`matrice_vendite`) specifica l'oggetto cui si vuole applicare una funzione
# **Il secondo argomento** specifica se la si vuole applicare per riga (`1`) o per colonna (`2`)
# **Il terzo argomento** specifica quale funzione si vuole applicare



#### **Unire matrici per riga o per colonna**
# Immaginiamo di avere una seconda matrice con le vendite di altri tre album dei Pink Floyd.
# In R, possiamo unire per riga due (o più) matrici usando funzione `rbind()`, che sta per row-wise bind
# a patto che le due matrici abbiano lo **stesso numero di colonne**.

# Dati della seconda matrice
vendite_italia2 <- c(0.9, 1.0, 0.8)
vendite_mondo2 <- c(25, 30, 20)
vendite_totali2 <- c(vendite_italia2, vendite_mondo2)

# Costruisci la seconda matrice
matrice_vendite2 <- matrix(vendite_totali2, nrow = 3, byrow = FALSE,
                           dimnames = list(c("The Wall", "The Division Bell", "A Momentary Lapse of Reason"), 
                                           c("Italia", "Mondo")))

# stampa a video il contenuto della variabile `matrice_vendite2` che hai appena creato

# Unisci le due matrici per riga
matrice_completa2 <- rbind(matrice_vendite, matrice_vendite2)
print(matrice_completa2)

#--> domanda per te: sapresti dire perché le due matrici da unire per riga devono avere lo stesso numero di colonne?

#--> domandaccia per te: un'analoga funzione di R che si chiama `cbind()`
# permette di unire due (o più) matrici per colonna, a patto che abbiano lo stesso numero di righe (sai dire perché?)
# costruisci due matrici, chiamate X e Y, che abbiano entrambe 5 righe (e il numero di colonne che vuoi tu), poi
# uniscile per colonna a formare un'unica matrice chiamata Z


# A proposito, in R la funzione `dim()` applicata ad una matrice (o ad altro oggetto con più di una dimensione)
# ti restituisce le dimensioni del dato oggetto. Lo fa restiruendo in output (almeno) 2 numeri:
# il primo numero indica il numero delle righe del dato oggetto e
# il secondo numero ti dice il numero delle colonne (mentre eventuali altri
# numeri ti parlerebbero della lunghezza della terza dimensione, quarta, etc).

#--> domanda per te: usa la funzione dim() per scoprire le dimensioni della variabile `matrice_completa2`


#### **Aggiungere una colonna o una riga ad una matrice**
# Utilizzando le stesse funzioni `rbind()` e `cbind()`, possiamo aggiungere
# rispettivamente una riga o una colonna ad una matrice.
# Ad esempio, aggiungiamo una colonna alla matrice delle vendite dei primi tre album
# con i totali delle vendite per ogni album.

matrice_completa <- cbind(matrice_vendite, Totale = totali_album)  # Nota: inserisco anche il nome della colonna
print(matrice_completa)


#### **Calcolare i totali delle vendite per regione**
# Usiamo la funzione `colSums()` per sommare le vendite in Italia e nel mondo.

totali_regioni <- colSums(matrice_completa2)
print(totali_regioni)

#--> domanda per te: ripeti il calcolo della somma per colonna, ma utilizzando la funzione `apply()`


#### **Selezionare elementi specifici**
# Analogamente a quanto visto con gli oggetti precedenti, possiamo selezionare elementi di una matrice
# dalle sue righe e/o colonne specificando gli indici degli oggetti di interesse tra le parentesi quadre `[ ]`.
# Analogamente a quanto già visto, potremo usare vari modi per specificare le posizioni di interesse.
# Una differenza importante: ora avremo bisogno di specificare due indici:
# **il primo indice** (primo numero tra le parentesi quadre `[ ]`, seguito da `,`) per specificare quali righe
# **il secondo indice** (secondo numero tra le parentesi quadre `[ ]`, dopo la `,`) per specificare quali colonne
# Nota: lasciar vuoto lo spazio del primo o secondo indicde equivale a prendere l'intera riga o colonna, rispettivamente.


#--> domandacce per te: utilizzando la matrice `matrice_vendite2`, prova a selezionare i seguenti elementi:
# 1. tutte le righe, ma solo la colonna `Mondo`

# 2. tutte le colonne, ma solo per la riga `The Division Bell`

# 3. le righe 1 e 3, ma solo la colonna `Italia`

# 4. le righe 2 e 3, e tutte le colonne

# 5. le righe `The Wall` e `The Division Bell`, e la colonna 2


### Operazioni con le Matrici
# In modo simile a quanto visto per i vettori, in R puoi applicare a matrici numeriche (o logiche)
# tutte le operazioni che applicheresti ad un singolo elemento dello stesso tipo (es. `numeric` o `logical`). 
# Anche in questo caso, come per i vettori, un'operazione matematica o logica
# applicata ad una matrice verrà eseguita elemento per elemento.

#--> domanda per te: prova a scrivere il comando per moltiplicare per 10 la matrice `matrice_vendite`


# Sempre in modo analogo a quanto sperimentato con i vettori, posso anche compiere operazioni tra due (o più) matrici.
# Supponiamo, ad esempio, che il costo di un disco in Italia sia di 20€, e nel mondo sia di 25€.

# creiamo una matrice con i costi dei dischi
prezzo_disco <- matrix(c(20, 25), nrow = 3, ncol = 2, byrow = TRUE)

#--> domanda per te: guarda bene il comando qui sopra e i suoi argomenti. Noti nulla di strano? 

# Ora usiamo la matrice dei prezzi appena creata come divisore, per stimare il numero di dischi venduti

dischi_venduti <- matrice_completa[, c("Italia", "Mondo")] / prezzo_disco

print(dischi_venduti)

#--> domanda per te: scrivi codice analogo per stimare i dischi venduti in `matrice_vendite2`
---

```
