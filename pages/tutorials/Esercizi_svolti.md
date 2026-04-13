---
title: Esercizi Svolti
---


# Esercizio n. 1: Sequenza ignota

**Considerando la seguente sequenza di DNA umano:**

5'-ACCCCAAGGGACTAATTCATGGTTGTTCCAAAGATAATAGAAATGACACA-3'

**Rispondere alle sequenti domande:**

a. dove mappa sul genoma? e con quali coordinate genomiche?<br>
b. è parte della sequenza di un gene umano? se si, di quale?<br>
c. se è parte di un gene umano, cade in una porzione esonica o intronica?<br>
d. produrre una immagine della risorsa utilizzata per rispondere, che supporti le risposte date ai punti (b) e (c).<br><br><br>

**Riferimento:**<br>
Lezione di lunedì 30 Marzo 2026. Argomento: UCSC genome browser. [Link al materiale](https://maghetta.github.io/big-data-in-genomics-and-transcriptomics/modulo4)<br><br><br>

**Svolgimento:**<br>

(a.) *dove mappa sul genoma? e con quali coordinate genomiche?*<br>
- apri una finestra del browser e collegati allo UCSC Genome Browser: 👉 https://genome.ucsc.edu/
- dalla barra dei menù in alto seleziona “Genomes” → “Human GRCh38/hg38”, per impostare come genoma di riferimento la versione attualmente più usata del genoma umano (GRCh38)
- nella pagina del browser genomico che si apre, dalla barra dei menù in alto seleziona “Tools” → “BLAT”, lo strumento che consente di mappare una sequenza nucleotidica o proteica e ricercarne i match sul genoma umano
- nella pagina del tool Blat che si apre, incolla la sequenza ignota data nella finestra di ricerca, verifica che il genoma di riferimento sia impostato su Human (GRCh38/hg38) e avvia la ricerca premendo sul tasto "Submit"
- nella finestra dei risultati della mappatura (BLAT Search Results), si vede un unico match perfetto (IDENTITY 100%) di tutta la sequenza cercata (QSIZE == SPAN) sul genoma umano. Il che ci permette di identificare senza dubbio le coordinate genomiche richieste dalla domanda, che sono: chr17, 43093053, 43093102, strand “-“

(b.) *è parte della sequenza di un gene umano? se si, di quale?*<br>
- nella finestra dei risultati della mappatura (BLAT Search Results), fare click sulla voce "browser" in corrispondenza del match sul genoma che viene elencato → nella pagina del browser genomico che si apre, è annotato un gene - in particolare: “BRCA1 (ENST00000357654.9) from GENCODE V49“ - in corrispondenza del match della sequenza ignota che abbiamo cercato. Quindi si, la sequenza mappa sul genoma umano versione GRCh38 in corrispondenza di un gene, e questo gene è “BRCA1“, che - come indicato nella finestra del genome browser dalle frecce che puntano verso sx - è proprio codificato sul filamento “-“, lo stesso filamento da cui origina la nostra sequenza ignota.

(c.) *se è parte di un gene umano, cade in una porzione esonica o intronica?*<br>  
- cade in una porzione esonica, come indicato nella finestra del genome browser dalla rappresentazione come box spesso nel tratto di trascritto di BRCA1 visibile in corrispondenza del match trovato per la sequenza ignota cercata.

(d.) *produrre una immagine della risorsa utilizzata per rispondere, che supporti le risposte date ai punti (b) e (c).*<br>
Nella finestra di visualizzazione visualizzata a schermo:
- aggiustare lo zoom sul genoma (utilizzando i tasti “Zoom in“ [1.5x\|3x\|10x\|Base] e “Zoom out“ [1.5x\|3x\|10x\|100x]) in modo che  siano ben visibile tutta la nostra sequenza mappata con Blat
- assicurarsi che sia visibile almeno una traccia di annotazione genica (ad esempio: GENCODE V49 e HUGO Gene Nomencalture, come nell'esempio mostrato qui sotto).
- rimuovere tutte le tracce non necessarie dalla finestra di visualizzazione, impostandone la visibilità su “hide” tramite il relativo menù (menù cui si accede con clic sul tasto destro del mouse in corrispondenza della barra laterale, tutto sulla sinistra, della traccia da eliminare).
- una volta definita la finestra di visualizzazione in modo opportuno per visulaizzare sia il match della sequenza ignota cercata, sia il gene annotato in questa regione (BRCA1), fare una foto allo schermo utilizzando il tasto “Stamp“ sulla tastiera, o altra applicazione per fare foto allo schermo, come nella immagine di esempio mostrata qui sotto.

 
<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/esercizio_1.png" width="800"> <br>
</div>
<br><br>

---



# Esercizio n. 2: Sequenza ignota

**Quanti geni codificanti per proteine sono attualmente annotati nel genoma murino? Quale considereresti una buona stima del numero medio di trascritti alternativi annotati nel genoma murino per questa categoria di geni?**<br><br><br>


**Riferimento:**<br>
Lezione di giovedì 26 Marzo 2026. Argomento: la banca dati GENCODE. [Link al materiale](https://maghetta.github.io/big-data-in-genomics-and-transcriptomics/modulo1)<br><br><br>

**Svolgimento:**<br>

*Quanti geni codificanti per proteine sono attualmente annotati nel genoma murino?*<br>
- apri una finestra del browser sulla pagina principale della banca dati GENCODE: 👉 [https://www.gencodegenes.org/](https://www.gencodegenes.org/)
- dalla schermata principale, seleziona “Mouse”, per accedere alle annotazioni genomiche curate di questo organismo della banca dati GENCODE (Release M38/GRCm39)
- nella pagina delle annotazioni GENCODE curate del genoma murino, seleziona la voce “Statistics of this release” presente in alto nella pagina.
- nella pagina riassuntiva delle statistiche che si apre, individua le conte corrispondenti alla voce “Protein-coding genes“ → N=21,530 nella versione corrente (Release M38/GRCm39).

*Quale considereresti una buona stima del numero medio di trascritti alternativi annotati nel genoma murino per questa categoria di geni?*<br>
- una buona stima del numero medio di trascritti alternativi annotati per i geni di topo codificanti per proteine è data semplicemente dal rapporto tra il numero di trascritti protein-coding e il numero di geni protein-coding. Avendo già determinato il numero di geni protein-coding annotati nel topo nella versione corrente di GENCODE (Release M38/GRCm39), possiamo analogamente ottenere il numero di trascritti protein-coding annotati nello stesso genoma.
- nella stessa pagina riassuntiva delle statistiche delle annotazioni murine appena consultata, individua le conte corrispondenti alla voce “Protein-coding transcripts“ → N=58,647 nella versione corrente (Release M38/GRCm39).
- stima il numero medio di trascritti alternativi annotati per i geni di topo codificanti per proteine calcolando il rapporto tra: [numero di trascritti protein-coding] / [numero di geni protein-coding] → N≈3


