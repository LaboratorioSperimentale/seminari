---
  title: La Trascrizione del Parlato con ELAN
  author: marcoesposito
  speaker: Silvia Ballarè
  layout: seminar
---

# La Trascrizione del Parlato con ELAN

## 1. Introduzione
L’obiettivo di questo workshop è quello di presentare anzitutto alcune nozioni di base in merito alla trascrizione e al sistema Jefferson (fornendo alcune possibili soluzioni ai problemi più comuni), per poi passare alle funzioni di base del software ELAN. In questo modo verranno forniti tutti gli strumenti per poter trascrivere un file audio in autonomia.


## 2. Trascrizione
Per trascrizione s'intende una forma di **rappresentazione del parlato in forma scritta**. Ciò può essere eseguito mediante diverse convenzioni, che vengono scelte in base agli obiettivi del ricercatore. Pertanto, prima di scegliere un tipo di convenzione piuttosto che un altro, è necessario tenere bene a mente il motivo stesso per cui stiamo trascrivendo. Vediamo quelli che sono gli obiettivi più comuni: 
1.	Si vuole studiare un fenomeno; 
2.	Si ha intenzione di documentare a livello più generale il comportamento di una comunità; 
3.	Si vuole avere una traccia scritta di “che cosa succede” nel mio file audio.

In base ai nostri obiettivi e a come decidiamo di usare il nostro programma, otterremo dei risultati diversi: 
1.	Un file annotato da consultare su ELAN;
2.	Testo da consultare senza riferimento audio;
3.	Trascrizione conversazionale;
4.	Testo glossato.
Il nostro focus sarà principalmente riguardo la trascrizione conversazionale e il sistema Jefferson.

### 2.1 Principali differenze fra scritto e parlato
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/image-1.png"
  caption="Confronto fra scritto e parlato"
%}

Naturalmente, prima di iniziare la trascrizione bisogna tenere a mente alcune differenze sostanziali fra le produzioni in forma parlata e in forma scritta. Vediamo le differenze più importanti:
- **Tempo di pianificazione**: Anzitutto, il fatto che il parlato venga organizzato in diretta fa sì che ci sia poco tempo per pianificare (ad esempio, possono esserci false partenze o progetti sintattici non portati a termine). Bisogna quindi capire come rappresentare questo tipo di caratteristiche. 
- **Produzione e ricezione**: A differenza dello scritto, nel parlato la produzione e la ricezione sono contemporanee: pertanto, nel caso di compresenza di più parlanti all'interno di una registrazione, diverse produzioni in forma parlata possono sovrapporsi (e bisogna dunque trovare un modo per rappresentare anche questo tipo di situazioni).

### 2.2 Problemi più comuni nella trascrizione
Vediamo alcuni dei probemi più comuni che emergono quando ci si approccia alla trascrizione:
- **L'individuazione di unità**, ossia il corrispettivo in lingua parlata di ciò che rappresenta la frase nella lingua scritta. Discuteremo di questo punto più approfonditamente in seguito.
- **L'intonazione**: modulando l’intonazione possiamo cambiare il significato della frase stiamo pronunciando (ad esempio, da essa dipende la distinzione fra una frase interrogativa e una frase dichiarativa). Bisogna dunque capire come trasferire queste informazioni nella trascrizione. 
Lo stesso vale per le pause, le false partenze, le riformulazioni, i cosiddetti filler e così via: vanno rappresentati nella conversazione? Se sì, come? Possono esserci diverse soluzioni a tale problema.

### 2.3 Possibili soluzioni
La risposta alle domande che ci siamo posti dipende dal contesto, in quanto bisogna sempre adattare le proprie risposte in base alle proprie esigenze di trascrizione. In base alle intenzioni con cui sto trascrivendo posso effettivamente decidere il sistema di trascrizione più adatto. 
Ad ogni modo, a prescindere dall'intento, <ins>bisogna cercare di mantenere un equilibrio fra due esigenze diverse</ins>: 
- **Fedeltà al parlato**: Da un lato c'è l'esigenza di trascrivere nella maniera più fedele possibile ogni aspetto del parlato (dunque anche aspetti come pause e sovrapposizioni fra parlanti);
- **Cercabilità nel testo**: se sovraccarico la trascrizione con dei simboli per indicare tutto ciò che avviene nel parlato, c'è il rischio che il testo perda parte della propria cercabilità e leggibilità. 

In sostanza, la trascrizione è una pratica di **decision-making**: in base al sistema di convenzioni che si sceglie di adottare, di volta in volta il trascrittore deve cercare di agire in maniera più coerente possibile rispetto al modello scelto e in base agli obiettivi che vogliamo raggiungere.

Riassumendo, idealmente si trascrive quanto più possibile (anche le pause, i vari segnali discorsivi, le false partenze e talvolta anche i gesti del parlante): tuttavia, se per i nostri obiettivi non è necessario avere una trascrizione eccessivamente dettagliata, è meglio non sovraccaricare il testo di informazioni (in modo da non perdere la facilità con cui si può interrogare il testo).


### 2.4 L’Individuazione di un’unità
Come è stato accennato precedentemente, una delle cose più complicate per quanto riguarda la trascrizione del parlato è l'individuazione dell'unità, cioè l'individuazione della frase. Ciò accade proprio perché il livello sintattico è quello che, rispetto allo scritto, presenta più differenze. 

A dire il vero, ai fini della trascrizione non è importante dare una definizione precisa di “frase” nel parlato: la trascrizione è uno strumento che ci serve a rappresentare il parlato, ma in un certo senso è **pre-teorica**, cioè non ci serve per l'analisi. La trascrizione deve essere sempre funzionale all'analisi, che avviene in un secondo momento. 
Per trascrivere, si è deciso di utilizzare come unità delle **unità di trascrizione** (che non hanno nessun tipo di rilevanza per l'analisi). L'unità di trascrizione viene individuata in base a un criterio intuitivo, cioè in base a parametri come la curva intonativa e, soprattutto, le pause. 

### 2.5 Il Sistema Jefferson
Vediamo il sistema Jefferson, qui usato per la trascrizione. È sicuramente il **sistema di trascrizione più diffuso** (anche se non il migliore). Il sistema Jefferson permette una rappresentazione piuttosto dettagliata di molti dei fenomeni che occorrono nel parlato, tra cui:
- Sovrapposizioni, pause, interruzioni;
- Allungamenti delle vocali, alterazione del volume, alterazione della velocità del parlato;
- Comportamenti non verbali (come risate o starnuti).

{%
  include figure.html
  image="images/seminar-images/elantrascrizione/image-2.png"
  caption="Simboli più frequenti del Sistema Jefferson"
%}

Qui vediamo una lista dei simboli più usati nel sistema Jefferson. Bisogna però fare una precisazione: notiamo che nella lista è presente un simbolo per rappresentare una pausa breve, ma non una pausa lunga. Quest'ultima è assente nella lista poiché non viene rappresentata mediante un simbolo, ma si inseriscono direttamente due unità diverse (e quindi la pausa viene rappresentata dall'interruzione delle unità).

## 3. ELAN
**ELAN** è un **software gratuito**, la cui funzione principale è quella di permettere la **trascrizione del parlato**. Ad un livello più avanzato si può utilizzare anche per effettuare ricerche all'interno delle trascrizioni (interrogazione del corpus) e per creare annotazioni su più livelli (ad esempio, posso decidere di creare delle glosse). È uno dei software più diffusi per la trascrizione del parlato, per cui online sono reperibili molti strumenti di supporto accessibili gratuitamente (tra cui un [forum](https://archive.mpi.nl/forums/) e diversi manuali, come [questo](https://www.ling.upenn.edu/~wlabov/L560/ELAN_introduction.pdf)).

### 3.1 Scaricare il programma
Il programma è scaricabile a questo [link](https://archive.mpi.nl/tla/elan/download). Quando si scarica il programma, il sito stesso mette a disposizione molto [materiale in PDF](https://archive.mpi.nl/tla/elan/documentation) che si può utilizzare per prendere confidenza con ELAN o per risolvere moltissimi dei problemi che possono emergere con col programma. 

### 3.2 Scaricare i materiali
In allegato è possibile trovare **due file video** e **un file audio**, che possono essere utilizzati per compiere un esercizio di trascrizione e per familiarizzare con le funzioni base di ELAN.
1.	Il primo video è composto da una serie di estratti da un dibattito presidenziale tra Trump e Biden, pertanto è in inglese. Ovviamente ci sono tre partecipanti, cioè i due candidati e il moderatore. Uno dei vantaggi di questo file è che i due partecipanti sono inquadrati sempre, il che è utile in caso di sovrapposizioni (poiché vediamo “chi parla quando”).
2.	Il secondo video è un estratto di una puntata da Porta a Porta. Qui il dibattito è in italiano, ma ci sono ben cinque partecipanti. Inoltre, non sempre i parlanti sono inquadrati, per cui non sempre è facile capire chi sta parlando.
3.	Il file audio è un’intervista tratta dal corpus parlato. Ci sono solo due parlanti coinvolti, l'intervistato e l'intervistatore.

### 3.3 Qualità e Formato dell'Audio
Prima di andare avanti, è utile fare una premessa: la qualità della traccia audio, assieme ad altri fattori (come il numero di persone o il luogo in cui è stata registrata l'interazione), influisce molto sulla difficoltà della trascrizione. Per intervenire sulla qualità della traccia audio (ad esempio per alzare il volume o ridurre il disturbo) si possono usare moltissimi software, come ad esempio **Audacity** (scaricabile a questo [link](https://www.audacityteam.org/download/) gratuitamente).

Un altro aspetto che ha delle conseguenze sulla facilità della trascrizione è il formato della traccia audio.

{%
  include figure.html
  image="images/seminar-images/elantrascrizione/image-3.png"
  caption="File non compresso e file compresso"
%}

Quando si usa un formato **file non compresso**, è possibile visualizzare le onde sonore del parlato. Ciò ci aiuta molto nell’individuazione delle unità, in quanto gli spazi vuoti tra un’unità e l’altra sono resi graficamente dall’assenza di onde sonore. Invece, nel caso di un **file compresso** non abbiamo alcuna rappresentazione visiva del parlato.

### 3.4 La Struttura di ELAN
La struttura di ELAN è costruita su righe diverse, che possiamo approssimare a uno spartito musicale per più strumenti: in sostanza, <ins>su ogni riga viene riportato ciò che dice un singolo parlante</ins>.

{%
  include figure.html
  image="images/seminar-images/elantrascrizione/image-4.png"
  caption="Visualizzazione dei tier"
%}

Questa è la visualizzazione che appare una volta aperto ELAN. Le righe qui riportate si chiamano **tier**: su ciascun tier (in questo caso ne sono presenti tre) bisogna trascrivere ciò che dice un singolo parlante. 

Vediamo un esempio:
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/image-5.png"
  caption="Tier del dibattito presidenziale"
%}
In questo caso sono presenti quattro tier (Trump, Biden, il moderatore e il pubblico). Notiamo come gli applausi del pubblico siano contrassegnati dalle parentesi tonde doppie, in quanto con questo simbolo si indicano i comportamenti non verbali.

### 3.5 Aggiungere il file da trascrivere
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/7 Avviare una trascrizione nuovo.PNG"
  caption="Associazione del file audio o video"
%}

Per avviare una trascrizione, la prima cosa da fare è associare il file audio o video che dobbiamo trascrivere, seguendo il percorso *File > New > Add media file*.

In generale, per tenere in ordine i file è prassi a dare al file della trascrizione lo stesso nome del file audio o video in modo tale che rimangano sempre associati e non si non si perdano.

### 3.6 Salvare un file e impostare il Backup Automatico
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/8 backup automatico.PNG"
  caption="Impostazione del backup automatico"
%}

Ancor prima di iniziare la trascrizione è utile salvare il file quando è ancora vuoto. Fatto ciò, possiamo impostare il **backup automatico** (tramite il percorso *File > Automatic Backup*): è estremamente utile, in quanto così facendo non si perde il lavoro svolto nel caso in cui il software dovesse bloccarsi. Si consiglia di impostare il backup automatico con il minutaggio più basso possibile (quindi con un minuto).

### 3.7 Creazione dei Tier
A questo punto dobbiamo creare i Tier, affinché ciascuno di essi sia associato al parlante che vogliamo trascrivere. Anziché creare un tier nuovo, possiamo modificare il tier che ELAN ci dà di default. Nella parte bassa della schermata troviamo una riga rossa col nome di “***tier default***”: possiamo semplicemente rinominare quel tier col nome che vogliamo associare a un certo parlante. Per farlo, clicchiamo col tasto destro sul tier default e selezioniamo “*Change Attributes of default*”; così facendo si apre una finestra nella quale è possibile modificare, tra le altre cose, il nome del tier.
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/image-10.png"
  caption="Modificare il nome del tier default"
%}

A questo punto la cosa da fare è creare i tier successivi in base al numero di parlanti presenti nel file che vogliamo trascrivere. Se non sappiamo a priori quanti parlanti ci sono nel nostro file, possiamo tranquillamente aggiungere dei tier successivamente. Per aggiungere un nuovo tier basta andare sul pulsante “***Tier***” in alto e cliccare poi su “***Add New Tier***”: si aprirà dunque una finestra analoga a quella che abbiamo già visto, nella quale sarà possibile scegliere il nome del tier.
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/image-11.png"
  caption="Creare un tier nuovo"
%}

Una cosa che spesso viene fatta è scegliere un codice alfanumerico per ogni tier, mentre nello spazio “participant” scriviamo il nome vero e proprio del partecipante (nel caso in cui non volessimo poi vederlo sulla trascrizione).

### 3.8 La Trascrizione e i Comandi Essenziali
A questo punto possiamo avviare la trascrizione vera e propria. Anzitutto bisogna precisare che tutti questi comandi qui riportati possono essere eseguiti anche col mouse. L’utilizzo della tastiera può risultare difficile all’inizio, in quanto bisogna memorizzare le diverse combinazioni di tasti per ogni specifico comando, ma risulta molto più vantaggiosa in seguito. 
Vediamo dunque alcuni dei comandi che servono per la trascrizione (tra i materiali c’è un PDF in cui c’è la lista completa delle combinazioni di tasti):
- **CTRL + Spazio**: avvia/stoppa la traccia audio.
- **CTRL/⌘ + K**: Seleziona/deseleziona la selection mode. Per individuare la stringa di parlato che vogliamo trascrivere bisogna entrare in selection mode, che può essere attivata o disattivata anche spuntando la casella apposita. A questo punto, quando si avvia/stoppa la traccia audio, si avvia/stoppa anche la selezione.
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/13 Select Mode.PNG"
  caption="Casella di Selection Mode"
%}
- **ALT + N**: A tal punto dobbiamo creare la nostra unità. Ciò significa che dobbiamo individuare quella che noi consideriamo essere un'unità di parlato che vogliamo trascrivere e selezionarla con la selection mode che abbiamo visto; dopodiché, una volta che abbiamo selezionato lo spazio che vogliamo trascrivere, dobbiamo <ins>creare una sorta di campo di testo all'interno di quello spazio selezionato</ins>, così che possiamo scriverci dentro quello che vogliamo. Per creare il campo di testo nello spazio selezionato, usiamo la combinazione ALT + N (oppure, una volta selezionato lo spazio, si può cliccare col tasto destro del mouse e premere su “New Annotation”). Premendo invio, l’unità trascritta si salva.
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/14 selezione.PNG"
  caption="Inserire una casella di testo"
%}
- **ALT + Mouse (in orizzontale)**: Volendo possiamo anche allargare o stringere la nostra unità con la combinazione ALT + mouse, premendo il tasto sinistro di quest'ultimo e spostando il cursore in senso orizzontale.
- **CTRL/⌘ + su/giù**: Questa combinazione serve per spostarsi da un tier all’altro in verticale (ad esempio, quando vogliamo trascrivere ciò che dice un parlante diverso da quello associato al tier su cui ci troviamo).
- **ALT + Mouse (in verticale)**: Può capitare di trascrivere le parole di un parlante nel tier sbagliato. Premendo ALT e il tasto destro del mouse, possiamo spostare l’unità da un tier all'altro (dunque in verticale). 
- **SHIFT + ALT + C**: Questa combinazione serve p34 cancellare una selezione, che + uno step necessario per poter cominciare una nuova selezione.
- **SHIFT + Spazio**: Questa combinazione serve nel caso in cui volessimo riascoltare la singola annotazione (ad esempio, può capitare che in un determinato punto l'audio non sia chiarissimo).

### 3.9 I Problemi più comuni
- **Cambiare le combinazioni di tasti**: In alcuni casi, le combinazioni di tasti precedentemente viste possono non funzionare, in quanto non tutte le tastiere funzionano allo stesso modo. In molti casi il problema può essere risolto svolgendo semplicemente l’azione col mouse, ma volendo ELAN offre anche l’opportunità di modificare le combinazioni di tasti associate a specifici comandi. Ad esempio, supponiamo che con la combinazione ALT + N io non riesca a creare il campo di testo nell’area selezionata: eseguendo il percorso *Edit > Preferences > Edit Shortcuts*, possiamo vedere quale combinazione di tasti è associata a quella specifica funzione ed eventualmente possiamo cambiarla a nostro piacimento.
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/image-16.png"
  caption="Cambiare le Shortcut della tastiera"
%}
- **Cambiare la velocità di riproduzione**: Se l’audio è troppo lento o troppo veloce, nella sezione in alto è possibile trovare il tasto “rate”, col quale si può modificare la velocità di riproduzione.
In alcuni casi la visualizzazione di ELAN è piccola. Per ingrandire solo la visualizzazione si può cliccare col tasto destro del mouse, selezionare “font size” e regolare la grandezza del testo. 
Un'altra cosa che può aiutare nella visualizzazione è il cursore in basso a destra, grazie al quale si può modificare la visualizzazione delle unità (restringendole o allargandole). Ciò vuol dire che la durata dell’unità si mantiene sull'asse temporale, ma diventa possibile visualizzare tutte le parole che prima non si riuscivano a vedere.
- **Ingrandire la visualizzazione delle unità**: In alcuni casi la visualizzazione di ELAN è piccola. Per ingrandire solo il corpo della trascrizione si può cliccare col tasto destro del mouse, selezionare “*font size*” e regolare la grandezza del testo. 
Un'altra cosa che può aiutare nella visualizzazione è il cursore in basso a destra, grazie al quale si può modificare la visualizzazione delle unità (restringendole o allargandole). Ciò vuol dire che la durata dell’unità si mantiene sull'asse temporale, ma diventa possibile visualizzare tutte le parole che prima non si riuscivano a vedere. In sostanza, con queste funzioni si alterà la modalità di visualizzazione delle unità, ma non le unità stesse.
- **Cancellare l'unità creata**: Per cancellare un'unità creata bisogna selezionarla cliccandoci sopra (in tal modo, l’unità dovrebbe diventare blu), per poi cliccare su “Delete Annotation”.
- **Il programma non legge il file mp3**: Tra i problemi che possono emergere durante la trascrizione, può capitare che ELAN non legga il file mp3 o che si blocchi. Il modo migliore per risolvere questo problema è cambiare il formato dell'audio, quindi convertirlo in formato .wav (è possibile farlo con Audacity, di cui abbiamo già parlato). Ovviamente, una volta cambiato il formato dell'audio bisogna riassociare nuovamente la trascrizione alla nuova traccia, e per fare ciò bisogna seguire questa sequenza: *Edit > Linked Files*.

### 3.10 Funzioni Avanzate
Vediamo adesso alcune delle funzioni più avanzate di ELAN.
#### 3.10.1 Vedere tutte le unità associate a un tier
ELAN permette di vedere assieme tutto ciò che abbiamo trascritto per quanto riguarda un unico parlante. Per fare questo, bisogna andare su “***Grid***”: si apre così una visualizzazione a griglia di tutte le unità presenti all’interno di un tier.
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/16 file griglia.PNG"
  caption="Visualizzazione a griglia delle unità associate a un tier"
%}

#### 3.10.2 La strutturazione dei tier
I tier possono avere diversi tipi di struttura. La strutturazione più semplice dei tier è quella che prevede l’associazione di un unico tier ad ogni parlante. Tuttavia, è possibile anche creare un quadro molto più complesso: è infatti possibile creare una serie di **tier dipendenti** dal tier che abbiamo associato a un parlante, creando così dei “sotto-tier”. In sostanza, è possibile creare un’**architettura interna** dei tier. Vediamo alcuni casi in cui questa funzione può essere utile:
- **Comunicazione non verbale**: posso fare un tier relativo solo ai movimenti del corpo di un determinato parlante. 
- **Commenti**: Questa funzione può tornare utile anche nel momento in cui decido di lasciare dei commenti, andando dunque ad inserirli proprio in un tier dipendente (usandolo come un vero e proprio block notes)
- **IPA**: se voglio trascrivere delle parti con l’alfabeto IPA, posso farlo andando ad inserirle in un apposito tier.
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/17 strutturazione tier.PNG"
  caption="Esempio di tier complesso"
%}
Vediamo un esempio. Qui abbiamo un tier molto complesso, in quanto vediamo una serie di “sotto-tier” associati ad un unico parlante. Tali tier contengono molti tipi di informazioni: nel primo tier vi è una trascrizione ortografica; nel secondo tier le parole vengono separate; nel terzo tier le singole parole sono annotate per parte del discorso; nel quarto tier abbiamo la trascrizione IPA e così via.

Vediamo dunque come aggiungere dei tier dipendenti.
La prima cosa da fare è creare un tier che segue la scansione temporale a cui voglio poi associarlo. Anzitutto andiamo su ***Type > Add New Tier Type***. Nella finestra che si apre andiamo poi su ***Stereotype*** e selezioniamo ***Time subdivision***, inserendo anche il nome del tipo.  
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/18 tier dipendente.PNG"
  caption="Add New Tier Type"
%}

A questo punto, una volta che abbiamo creato il nuovo type possiamo creare il nuovo tier. Seguiamo dunque gli stessi passaggi di prima (Tier > Add New Tier), ma questa volta bisogna specificare a quale tier dipende il “sotto-tier” che stiamo creando. Per farlo, nella riga “***Parent Tier***” dobbiamo selezionare il tier a cui vogliamo associarlo.
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/19 tier dipendente.PNG"
  caption="Add New Tier"
%}

A questo punto, ci si ritrova con tutti i tier allineati. Per avere un tipo di visualizzazione in cui si rende evidente “quale tier dipende da quale tier”, bisogna seguire il seguente percorso: **Click destro sui tier** ***> Sort Tiers > Sort by Hierarchy***.
{%
  include figure.html
  image="images/seminar-images/elantrascrizione/20 tier dipendente.PNG"
  caption="Tier ordinati per gerarchia"
%}

#### 3.10.3 Divisione per Parola