---
layout: seminar
title: "traduzione del parlato,la rivoluzione del modello diretto"
author: leonardozannoli
speaker: marco turchi
---
# traduzione del parlato,la rivoluzione del modello diretto

In questo seminario viene spiegato cosa si intende per traduzione del parlato, analizzando i due metodi principali, ovvero il cascade e il metodo diretto. Successivamente, viene presentata una comparazione fra i due metodi, la prima a livello mondiale, ma soprattutto vengono presi in esame due casi d'uso: il primo riguardante il bias di genere e il secondo il sottotitolaggio.   

## Cosa si intende per traduzione del parlato?

La traduzione del parlato è il processo tramite il quale un discorso orale in una lingua viene tradotto in un testo in un'altra lingua. È importante fare una distinzione fra traduzione da audio a testo e traduzione da audio ad audio.

La traduzione del parlato ha attratto negli anni un interesse a livello accademico, con molte università che hanno lavorato per far sì che questo tema avesse un ruolo fondamentale nella ricerca, ma ha anche avuto negli ultimi anni un sbocco aziendale, con aziende che hanno messo ha disposizione servizi di traduzione del parlato.

## Perchè è importante la traduzione del parlato?

Perchè il parlare è una delle principali fonti di comunicazione ed è fondamentale per evitare che le barriere linguistiche diventino ostacoli. Avere uno strumento che ci permette di trasformare una lingua che non conosco in un testo in un'altra lingua può permettere a due persone che parlano lingue diverse di comunicare.

Si può avere un tipo di comunicazione uomo-uomo come nel caso del sottotitolaggio ma negli ultimi anni si è sviluppata notevolmente la comunicazione uomo-macchina

## La storia della traduzione del parlato

I primi sistemi per la traduzione del parlato risalgono alla fine degli anni 80. Si trattava di sistemi con un vocabolario molto ristretto, con uno stile molto semplice.
Negli anni si è iniziato a rilassare queste condizioni e quindi di testare questi sistemi in ambienti sempre più complessi. Si inizia alla fine degli anni 90 con un parlato spontaneo per arrivare a un open domain, ovvero una comunicazione che si può avere per strada fra due persone. Infine nel 2006 si arriva ad utilizzare questi modelli in real time, ovvero che mentre uno parla il sistema comincia automaticamente a tradurre.

Dal 2016 cambia tutto con l'introduzione dei sistemi e2e, che sono architetture molto compatte che hanno un unico modello che prende un audio in una lingua e produce un testo in un'altra. 

## Traduzione del parlato: un problema a molte facce

Tradurre il parlato può essere molto complicato perchè, a differenza della traduzione di un testo, subentra la voce, che può variare da persona a persona o avere rumori di fondo che possono disturbare o esserci anche accenti diversi.

Per esempio, possiamo avere una situazione offline in cui l'audio viene messo integralmente a disposizione per tradurlo oppure in simultaneo dove abbiamo pezzi di audio che devono essere tradotti.

Ci può essere un parlatore unico ma anche situazioni in cui ci sono vari parlatori. In quest ultimo caso c'è il problema di capire chi parla poichè ci potrebbero anche essere sovrapoposzioni.

Spesso l audio può anche essere disturbato da agenti esterni come ad esempio il vento.

Inoltre, ci possiamo tropvare in un dominio ristretto, come nel caso dei bollettini meteo, in cui i termini sono sempre più o meno quelli come anche le aree geografiche, oppure trovarsi in un dominio aperto, dove le persone possono parlare di qualunque cosa


Un altro problema può essere legato anche alle lingue, poichè alcune come l inglese o il francese godono di molte risorse per addestrare questi modelli, mentre altre come quelle africane ne hanno poche e il sistema può andare in difficoltà.

Fra i problemi della traduzione, oltre alla complessità che può avere un messaggio, troviamo anche la variabilità del parlatore, che può avere vari accenti, ma si possono anche trovare difficoltà se il parlatore è un uomo o una donna o se è un bambino o una persona anziana.

Infine, si può incontrare il problema della traduzione vincolata, come nel caso del sottotitolaggio, dove la traduzione deve rispettare dei vincoli imposti dal problema.

## Approccio classico: il cascade

Nel modello detto a cascata si mettono in moto una sequenza di processi che permettono di passare da un audio in una lingua ad un testo in un'altra lingua. 

Questi processi si possono dividere in due blocchi: quello del riconoscimento del parlato e uno è quello della traduzione testuale. Questi modelli si sono sviluppati a partire dagli anni 80, affinandosi nel tempo e al giorno d'oggi entrambi usano l'intelligenza artificiale. 

Nel caso del riconoscimento del parlato, si ha una conversione del parlato in testo nella stessa lingua. La difficoltà è che l audio è un continuum, cioè non risulta diviso in segmenti di parole ben definiti. L' audio è un continuum nel tempo e il sistema deve capire come isolare le parole.

La cosa positiva nel riconoscimento del parlato è che abbiamo una relazione temporale fissa, monotonica, tra l'audio e il testo.

Per quanto riguarda invece la machine translation vengono convertite le trascrizioni automatiche in un testo nella lingua target.

A differenza del riconoscimento del parlato, il testo è diviso a parole, però non c' è un rapporto monotonico tra il testo sorgente e target perchè possiamo incontrare regole grammaticali diverse fra le due lingue.  

## I pro e i contro del cascade

Un vantaggio è che ormai si tratta di un approccio consolidato nel tempo e si conosce come organizzare i sistemi di traduzione. Inoltre, essendo il riconoscimento del parlato e la machine translation due aree di ricerca molto grandi si possono sfruttare grosse quantità di dati per addestrare il sistema.

Purtroppo però ci sono anche diversi problemi:
- il primo è senza dubbio la propagazione dell errore, ovvero se un sistema di riconoscimento sbaglia, soprattutto con le parole omofone, si ottiene qualcosa di completamente diverso dall input;
- un altro problema è la perdita di informazioni dall audio, ovvero che quando un sistema di machine translation traduce ha perso ogni contatto con l audio che invece ci può dare informazioni anche a livello di prosodia. Per esempio, c'è molta differenza se io dico una cosa sottovoce o urlando e questo può aiutare il sitema a capire come modulare la traduzione; 
- Infine, avendo molti moduli la latenza è molto alta e inoltre questi necessitano di manutenzione che ovviamente ha un costo.

## Il modello diretto

Il modello diretto non deve avere rappresentazioni discrete intermedie, come ad esempio le trascrizioni nel Cascade ma soprattutto tutti i parametri usati per tradurre devono essere addestrati all' unisono. 
Il modello diretto si appoggia sui modelli a sequenza dove si ha un encoder che prende l audio e lo trasforma in una sequenza di numeri e un decoder che partendo da questa sequenza genera un testo. 
Questi modelli sono stati arricchiti dal modello di attenzione che permette al decoder  di guardare nell' audio ogni volta che deve tradurre una parola per capire qual' è l' nformazione più funzionale per tradurre quella parola.

## I pro e i contro del modello diretto

Uno dei vantaggi più grossi è che si ha un accesso diretto all' audio durante la traduzione, poichè il decoder è direttamente collegato all' encoder. Ma soprattutto non c'è propagazione dell'errore perchè non ci sono rappresentazioni intermedie discrete. Infine, un altro vantaggio è che in fase di produzione si ha un solo sistema da gestire.

Tuttavia anche con il modello diretto si riscontrano delle problematiche.
Innanzitutto, si tratta di una tecnologia non ancora consolidata come il Cascade, ma soprattutto si ha ancora una scarsità di dati di training.
Inoltre, il modello diretto non allinea in maniera monotonica l'audio e le parole, quindi in fase di produzione, oltre alla comprensione dell' audio, bisogna anche procedere ad un riordino delle parole.

Per migliorare la comprensione dell' audio, sono state sviluppate delle tecniche che riducono l'audio tramite l'uso di CNN. Oppure sono state sviluppate strategie specifiche basate sull'attenzione, in cui non si guarda tutto l' input perchè troppo lungo, ma ci si focalizza su delle zone ben precise. 

## Cascade vs Modello Diretto

Secondo la Campagna di Valutazione IWSLT, nel giro di tre anni, dal 2018 al 2020, il Modello Diretto è stato sviluppato e migliorato al punto da colmare il gap di performance che inizialmente aveva con il cascade.

La maggior parte degli articoli sul modello diretto parlano dei seguenti vantaggi, dandoli un po' per scontato, rispetto al cascade:
- non c'è propagazione dell'errore;
- c'è un accesso diretto all'audio, che permette una manipolazione migliore delle informazioni paralinguistiche e non-linguistiche durante la traduzione (es. la prosodia).
Tuttavia, la correttezza di queste due affermazioni non sono mai state verificate empiricamente. Da qui, l'importanza di studiare le vere differenze, se ci sono, tra il cascade e il Diretto, che è il vero obiettivo di questa presentazione.

## Primo caso d'uso: il bias di genere

Quando si parla di Machine Bias, si fa riferimento a quei sistemi automatici che sistematicamente e in modo ingiusto discriminano contro certi individui o gruppi di individui in favore di altri. Lo stesso natural language processing (NLP), non è esente da questo problema, anzi questi algoritmi tendono ad amplificare le differenze di tanti bias e uno di questi e il genere.  
Ovviamente, questa situazione ha creato notevoli problemi sia dal punto di vista etico sia dal punto di vista di chi sviluppa questi sistemi.

Ma perchè questi sistemi tendono a com piere questi errori? Perchè loro sono quello che imparano dai dati. 
Ad esempio, nei dibattiti del Parlamento Europeo, che è una delle fonti principali di dati per addestrare i sistemi per la traduzione del parlato, il 70 % sono speaker maschi. Quindi succede che questi sistemi imparano che il 70% delle volte devono produrre una traduzione che è maschile o tendente al maschile, discriminando in maniera evidente la clase femminile.

## Gender e traduzione

Come gestiscono il genere le lingue? Esistono lingue gender neutral come l'inglese che tendono a non marcare il genere nella maggior parte dei casi, mentre altre, come l'italiano e lo spagnolo, sono lingue che marcano in ogni loro essenza il genere. Quindi ci sono notevoli parti del discorso dove cambia la forma della parola a seconda che ci si riferisce ad un maschio o ad una femmina.
I sistemi, traducendo dall'inglese frasi come "i'm a good friend", tendenzialmente lo renderanno al maschile. Questo avviene perchè è già presente un bias nei dati di training che spinge i sistemi verso una forma maschile di default, amplificando le asimmetrie sociali.

## Perchè analizzare il gender bias?

Perchè, mentre nella Machine Translation il testo sorgente non sempre fornisce informazioni sul genere, nella Speech Translation(ST), l'audio ci può aiutare a capire se si deve tradurre al maschile o al femminile.  