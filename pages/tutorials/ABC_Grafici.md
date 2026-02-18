---
title: ABC Grafici in R
---

```markdown
# Tutorial: Creazione di Grafici Base in R

# R offre molte funzioni per creare grafici base, utili per visualizzare i dati.
# Questo tutorial introduce le basi per creare e personalizzare grafici in R.
# In particolare, esploreremo le funzioni `plot()`, `barplot()`, `hist()`, `pie()` e `boxplot()`.
# Inoltre, vedremo alcuni esempi su come personalizzare i grafici modificando colori, legende e stili.

# 1. Funzione plot
# La funzione plot() è molto versatile e consente di creare diversi tipi di grafici.
# Di default, viene usata per scatter plot (grafici a dispersione).

# Esempio: Scatter plot
x <- 1:10
y <- x^2
plot(x, y, main = "Scatter plot", xlab = "X", ylab = "Y", col = "blue", pch = 19)

# Modifiche principali:
# - main: titolo del grafico
# - xlab, ylab: etichette degli assi
# - col: colore dei punti
# - pch: stile dei punti

#--> domande per te: prova a modificare il grafico appena fatto come segue:

#...a.) ripeti il grafico modificando il colore dei punti da blu a verde
# A proposito: puoi stampare l'intero elenco dei 657 colori a tua disposizione digitando `colors()`

#...b.) ripeti il grafico modificando l'aspetto dei punti, da pallino pieno a triangolino pieno.
# Per farlo ti sarà utile sapere che il parametro da modificare nel comando del plot per modificare
# l'aspetto dei punti è `pch` (`plotting character`), e che questo parametro può assumere valori da 0 a 25,
# ognuno associato ad un diverso simbolo per rappresentare i punti nel plot.
# A proposito: puoi visualizzare l'intero elenco dei 26 caratteri di plot a tua disposizione digitando `?pch`

#...c.) ripeti il grafico modificando sia il contenuto del titolo (da "Scatter plot" a "Primo plot"), che
#      il colore (da nero a turchese).
# Lascio a te di dedurre, guardando gli argomenti del comando `plot()` appena digitato, quale argomento
# dovrai modificare per cambiare il titolo al grafico come richiesto. 
# Invece, per modificarne il colore, ti sarà utile sapere che l'argomento che ti permette di modificare
# il colore del titolo è: `col.main`

#...d.) ripeti il grafico modificando l'aspetto dei punti, in modo che compaiano connessi da una linea
# Per farlo, ti sarà utile sapere che il paramentro per modificare l'aspetto del tracciamento dei dati
# si chiama `type`, e può assumere tra gli altri i seguenti valori:
# - "p": stampa i singoli punti (default)
# - "l": stampa linee
# - "b": (che sta per *both*) stampa punti connessi da linee
# - "o": stampa punti sormontati da linee
# - "n": Non stampa nulla riguardo i punti, mentre stampa gli assi e il sistema di coordinate in accordo con i dati.
#        Si usa ad esempio nel caso si vogliano aggiungere poi gli ulteriori dettagli del plot con funzioni specifiche
#        come `points()`, `lines()` ecc. 


# Qualche altra informazione utile:
# Con la funzione *abline()* possiamo aggiunre linee verticali o orizzontali al plot
abline(h=3, lty=2, col=3)


# 2. Funzione barplot
# La funzione barplot() è usata per creare grafici a barre.

# Esempio: Grafico a barre
values <- c(4, 7, 9, 6)
names <- c("A", "B", "C", "D")
barplot(values, names.arg = names, main = "Grafico a barre", col = "red", border = "black")

# Modifiche principali:
# - names.arg: nomi delle barre
# - col: colore delle barre
# - border: colore del bordo

# 3. Funzione hist
# La funzione hist() è utilizzata per creare istogrammi.

# Esempio: Istogramma
set.seed(123)
data <- rnorm(1000)
hist(data, main = "Istogramma", xlab = "Valori", col = "lightblue", border = "darkblue")

# Modifiche principali:
# - col: colore delle colonne
# - border: colore dei bordi
# - xlab: etichetta dell'asse x

# 4. Funzione pie
# La funzione pie() crea grafici a torta.

# Esempio: Grafico a torta
slices <- c(40, 30, 20, 10)
labels <- c("A", "B", "C", "D")
pie(slices, labels = labels, main = "", col = c("orange", "green", "purple"))

# Modifiche principali:
# - labels: etichette delle sezioni
# - col: colori delle sezioni


## Aggiungere una legenda, un titolo o un sottotitolo
# In R, possiamo ulteriormente modificare un grafico con funzioni cosiddette di "basso livello"
# che ci permettono di aggiungere dettagli specici.
legend("topright", legend = c("Gruppo A", "Gruppo B", "Gruppo C"), fill = c("orange", "green", "purple"))
title("Grafico a torta", col="cyan")


# 5. Funzione boxplot
# La funzione boxplot() è usata per creare box plot.

# Esempio: Box plot
group1 <- rnorm(50, mean = 5)
group2 <- rnorm(50, mean = 7)
data <- list(Group1 = group1, Group2 = group2)
boxplot(data, main = "Box plot", col = c("orange", "green"), names = c("Gruppo 1", "Gruppo 2"))

# Modifiche principali:
# - col: colori delle scatole
# - names: nomi dei gruppi

# Personalizzazione generale
# I grafici possono essere ulteriormente personalizzati con:

# Modificare i margini:
par(mar = c(5, 5, 4, 2))

# Salvare i grafici in un file:
png("grafico.png")
plot(x, y, main = "Scatter plot salvato", xlab = "X", ylab = "Y", col = "blue", pch = 19)
dev.off()

## Per finire... di inziare!
# La grafica in R è un mondo! Ti basterà digitare in un motore di ricerca delle parole chiave in proposito per
# trovare una marea di guide e videotutorial.
# Per non perdervi in questo mare, vorrei concludere con un paio di indicazioni utili:
# 1. Puoi continuare ad esplorare la funzione `plot()` e altre funzioni grafiche ad esempio nel capitolo 12
# `Graphical procedures` del [Manuale in formato PDF **Introduction to R**](href="https://cran.r-project.org/doc/manuals/r-release/R-intro.pdf)
# 2. Puoi esplorare la **galleria grafica di R** (enorme risorsa!!), dove per ogni grafico di tuo interesse troverai
# esempi di codice per realizzarlo, che potrai adattare ai tuoi dati.
# 3. In questo tutorial abbiamo utilizzato un approccio classico (e più semplice) ai grafici. Esiste un approccio più compelsso,
# ma anche molto più potente, per costruire grafici strutturandoli e definendoli livello dopo livello. Questa modalità di approccio
# è abilitata dal pacchetto R `ggplot2`.
# Per esplorarne le potenzialità, potresti inziare da qui:
# https://cran.r-project.org/web/packages/ggplot2/vignettes/ggplot2-in-packages.html
# oppure da qui: https://ggplot2.tidyverse.org/.

#-------------

## Quanto appreso fin qui in questo tutorial soddisfa pienamente i requisiti di un corso di base di R.
## Se hai appena iniziato a conoscere questo linguaggio, il mio consiglio è di congratularti con te stessa/o
## per aver raggiunto la fine di questo tutorial, e fermarti qui!
## Se invece:
# - hai particolare dimestichezza con la statistica e sogni di poter aggiungere una retta di regressione al tuo plot
#     oppure
# - sei un utente medio-avanzato di R e vorresti cimentarti con sistemi più avanzati di plotting, come *ggplot2*
# puoi provare ad avventurarti in questi due blocchi di informazione EXTRA.


## EXTRA #1:

# Una retta spesso utile da aggiungere ad un grafico di dispersione per cogliere la relazione tra due variabili
# è la *retta di dispersione lineare*, cioé la linea che “si avvicina il più possibile” a tutti i punti, 
# minimizzando la somma dei quadrati delle distanze tra ciascun punto e la linea stessa.
# Per approfondire gli aspetti teorici di una retta di regressione lineare, puoi vedere ad esempio la relativa pagina su Wikipedia:
# https://cran.r-project.org/doc/manuals/r-release/R-intro.pdf](https://it.wikipedia.org/wiki/Regressione_lineare

# Qui di seguito vediamo un codice R essenziale per calcolarla e aggiungerla ad un plot.

# Ipotizziamo di avere due variabili numeriche *x* e *y* così definite:
set.seed(123)  # questa funzione serve a rendere i risultati riproducibili
x <- 1:20
y <- 2 * x + rnorm(20, mean = 0, sd = 5)  # questo comando genera del "rumore casuale" intorno a ciascun punto

# ora facciamo uno scatterplot di queste due variabili:
plot(x, y, main = "Scatterplot con retta di regressione lineare", xlab = "Variabile X",  ylab = "Variabile Y", pch = 19)

# Utilizziamo la funzione *lm()* (per "linear model") di R per calcolare il modello di regressione lineare
# che meglio descrive l'eventuale relazione tra la variabile dipendente *y*
# e la variabile indipendente *x*.
modello <- lm(y ~ x)

# Aggiungiamo la retta di regressione allo scatter plot, utilizzando la funzione *abline()*
abline(modello, col = "red", lwd = 2, lty = 2)

# dove:
# - l'argomento *lwd = 2* (line width) aumenta lo spessore della linea rispetto al valore di default, che è 1
# - l'argomento *lty = 2* (line type) disegna la linea tratteggiata anziché continua, che è il default


## EXTRA #2:
# Lo stesso scatter plot con retta di regressione lineare, fatto con il sistema ggplot2, si potrebbe fare con il seguente codice:

# prima di tutto, carichiamo il pacchetto ggplot2
library(ggplot2)

# poi, arrangiamo le nostre variabili x ed y in un dataframe:
dati <- data.frame(x = x, y = y)

# ora il codice per creare uno scatterplot con la retta di regressione lineare
ggplot(dati, aes(x = x, y = y)) +                                # definiamo i dati
  geom_point(color = "blue", size = 3) +                         # aggiungiamo i punti e definiamone lo stile (colore, grandezza)
  geom_smooth(method = "lm", color = "red", se = FALSE) +        # aggiungiamo la retta di regressione lineare
  labs(title = "Scatterplot con retta di regressione lineare",   # aggiungiamo titolo e etichette degli assi
       x = "Variabile X",
       y = "Variabile Y") +
  theme_minimal()                                                # scegliamo lo stile grafico del plot (*minimal*)


## cenni sulla "filosofia ggplot2"

# Il sistema grafico in R basato su ggplot2 si ispira al concetto di "Grammar of Graphics", teorizzato da Leland Wilkinson nel 1999.
# In sintesi, un grafico si costruisce *strato dopo strato*, adottando un approccio modulare.

# A livello di codice, il grafico si costruisce combinando varie funzioni del pacchetto ggplot2:
# - ggplot(): inizializza lo spazio del grafico e definisce l'oggetto che contiene i dati da visualizzare
# - aes() (aesthetics): mappa le variabili dei dati a caratteristiche visive (colore, dimensione, forma, assi x e y)
# - funzioni "geoms" (forme geometriche), es. geom_point() per scatter plot, geom_bar() per grafici a barre; qui si definiscono anche le caratteristiche estetiche (es. colore dei punti)
# - labs(): specifica titolo e etichette degli assi (opzionale)
# - funzioni "theme", es. theme_minimal() o theme_dark(): personalizzano l'aspetto del grafico (font, sfondo, griglie) (opzionale)

# Per un’introduzione rigorosa e approfondita al sistema di grafica basato su ggplot2, consulta il sito ufficiale: https://ggplot2.tidyverse.org/.
# A seconda del livello di confidenza con il sistema di pacchetti tidyverse (di cui ggplot2 fa parte), può essere molto utile comprendere la struttura
# dei dati tidy leggendo il bellissimo libro R for Data Science (https://r4ds.hadley.nz/), disponibile anche in italiano: https://it.r4ds.hadley.nz/index.html

```
