---
  title: Annotazione e Analisi di Testi Digitali con CATMA 7
  Author: Marco
---

# Annotazione e Analisi di Testi Digitali con CATMA 7


## 1. Introduzione: Cos'è Catma?
[CATMA](https://catma.de/) (Computer Assisted Text Markup Analysis) è un **tool di annotazione gratuito e open-source**, particolarmente utile per l'annotazione manuale di testi. A differenza di altri tool, CATMA consente anche di lavorare su progetti di gruppo. I testi e le annotazioni possono essere analizzati con diversi criteri e query, quali ad esempio la frequenza di una parola, la categoria di annotazione o la prossimità fra parole.

{%
  include figure.html
  image="images/seminar-images/catma_final/1 Catma Logo.PNG"
  caption="Logo di CATMA"
  width="400px"
%}
<!-- ![plain image{caption=Logo di CATMA}](/images/seminar-images/catma_final/1 Catma Logo.PNG)
*Fig. 1: Logo di CATMA* -->

Il programma è composto da **quattro moduli**, qui brevemente descritti (ma saranno maggiormente approfonditi in seguito):

| Modulo | Descrizione|
|--------|------------|
|PROJECT | La sezione in cui gestisci le risorse del tuo progetto|
| TAGS   | Consente di aggiungere, modificare o eliminare i tagset|
| ANNOTATE | Consente di annotare il testo, così come modificare o eliminare le annotazioni|
| ANALYZE | Permette di analizzare un testo, offre diverse opzioni di visualizzazione e di annotazione semi-automatica|


## 2. Registrazione and Log-in
Anzitutto, bisogna creare il proprio [account CATMA](https://app.catma.de/): puoi scegliere di usare il tuo **account Google** o una **e-mail privata**. Dopo la registrazione verrà inviata una e-mail di verifica all'indirizzo usato in fase di registrazione. Dopo aver verificato l'indirizzo e-mail, sarà possibile completare il profilo scegliendo uno username e una password.
![alt text](images/seminar-images/catma_final/2 Sign up Options.PNG)
*Fig. 2: Opzioni di registrazione su CATMA*


## 3. Panoramica Generale
Una volta effettuato l'accesso, sarà possibile scegliere fra *"Nuovo Progetto"* o *"Unisciti ad un progetto"* (in quest'ultimo caso, il proprietario del progetto dovrà aggiungerti tramite il tuo username o mediante un invito in tempo reale). Sul lato sinistro dello schermo vi è una barra laterale con tutti i moduli precedentemente menzionati, che saranno attivati non appena si sceglie il progetto su cui si vuole lavorare.
![alt text](images/seminar-images/catma_final/3 Project Overview.PNG)
*Fig. 3: Schermata Home di CATMA*


## 4. Modulo Progetto
Una volta selezionato il progetto su cui si vuole lavorare, è possibile entrare nel **Modulo Progetto** (**_Project Module_**). In questa sezione potrai vedere e gestire le diverse parti del tuo progetto, mostrate in riquadri differenti (*Documenti & Annotazioni*, *Tagsets*, *Membri*).
![alt text](images/seminar-images/catma_final/4 Project Module.PNG)
*Fig. 4: Modulo Progetto di CATMA*

Vediamo le funzioni principali di ciascun riquadro:
- **Documenti & Annotazioni**: In questo riquadro è possibile caricare testi dal tuo computer o aggiungere un URL (cliccando sul pulsante "+"), così come esportare o eliminare raccolte di annotazioni o documenti. Da questa sezione è anche possibile creare la tua raccolta personale di annotazioni in un progetto di gruppo. insRicorda che per annotare i documenti bisogna sempre creare prima una raccolta di annotazioni/ins (che consiste in una sorta di copia del testo da annotare). Le annotazioni su CATMA sono conservate separatamente rispetto al testo originale. Potrai anche vedere quale membro ha creato una determinata risorsa.
![alt text](images/seminar-images/catma_final/5 Add documents to your project.PNG)
*Fig. 5: Aggiungere un nuovo documento su CATMA*

- **Tagsets**: Nel secondo riquadro è possibile vedere quali tagset sono stati creati per un determinato progetto. Da questa sezione puoi creare o eliminare tagset, ma bisogna necessariamente andare nel Modulo Tag per aggiungere dei tag a un tagset esistente. Ciononostante, nel Modulo Progetto è possibile caricare un tagset esistente in formato XML.

- **Membri**: In questo riquadro vengono mostrati i membri del progetto. Se il proprio ruolo lo consente, è possibile aggiungere nuovi membri al progetto: lo si può fare manualmente (tramite lo username) o tramite invito in tempo reale. Se si sceglie quest'ultima opzione, apparirà un pop-up con un codice; tutte le persone che hanno accesso a tale codice potranno unirsi al progetto. Il codice sarà valido finché si tiene la finestra pop-up aperta, dopodiché non sarà più valido. Inoltre, da questo riquadro è possibile eliminare dei membri o modificarne il ruolo.

### 4.1 Membri e Ruoli
Va tenuto a mente che le azioni che si possono svolgere su CATMA dipendono dal proprio ruolo nel progetto (che viene mostrato nel riquadro "Membri" accanto al proprio username): ogni ruolo corrisponde a [permessi specifici](https://catma.de/documentation/roles-and-permissions/). Ad esempio:
- **Proprietario**: Il proprietario ha ogni diritto possibile sul progetto, come ad esempio creare/eliminare documenti, tagset, raccolte di annotazioni o aggiungere/rimuovere membri dal progetto.
- **Partner**: Un partner ha quasi gli stessi diritti del proprietario, fatta eccezione per alcuni aspetti: ad esempio, non può aggiungere o rimuovere membri, né tantomeno può eliminare il progetto.
- **Osservatore**: Un osservatore può solo visionare i documenti, i tagset o le raccolte di annotazioni, ma non possono modificarli o aggiungerli in nessun modo.

### 4.2 Tasti "_Sync_" e "_Switch View_"
Nell'angolo in alto a destra dello schermo è possibile trovare due importanti funzioni di CATMA:
- **Tasto “_Sync_”**: In un lavoro di gruppo, questo pulsante consente a ogni membro del team di sincronizzare i propri progressi sul progetto, in modo da condividere i propri documenti caricati, le proprie annotazioni o i nuovi tag (in altre parole, tutto ciò che è stato fatto dall'ultima sincronizzazione).
- **Tasto “_Switch View_”**: Questo pulsante  consente di alternare tra due modalità di visualizzazione, che sono "_sincronizza_" (che mostra lo stato attuale di tutto il lavoro che è stato integrato più tutto ciò che hai fatto in aggiunta a quello, come individuo) e "_ultimo contributo_" (il progetto entra in uno stato di sola lettura che ti permette di vedere cosa hanno fatto gli altri membri)


## 5. Modulo Tag
Una volta caricate le proprie risorse, è possibile creare un **tagset** (ossia un insieme di tag con cui puoi lavorare sul tuo progetto).
![alt text](images/seminar-images/catma_final/6 Tags Module.PNG)
*Fig. 6: Modulo Tag di CATMA*

Cliccando sul pulsante “+” nella parte in alto a destra dello schermo, puoi creare un **nuovo tagset** o aggiungere **nuovi tag** a un tagset esistente (per fare ciò, bisogna prima selezionare il tagset in questione). Mentre si crea un tag, è possibile anche specificare le sue proprietà in modo da qualificarlo meglio.
![alt text](images/seminar-images/catma_final/7 Add tag.PNG)
*Fig. 7: Aggiungere un nuovo tag a un tagset esistente*

CATMA offre anche la possibilità di creare una gerarchia fra i tag, creando dunque dei **sotto-tag** (vale a dire un tag che è subordinato ad un altro tag per qualificarlo meglio). Esattamente come per i tag, nella creazione dei sotto-tag è possibile aggiungere proprietà e valori.

## 6. Modulo Annotazione
Una volta che il tuo progetto contiene almeno un documento, una raccolta di annotazioni e un tagset, puoi cominciare ad annotare un documento in questo modulo. Per fare ciò, insbisogna selezionare una raccolta di annotazioni e il tagset con cui si vuole lavorare/ins. Mentre lavori in questa sezione, avrai il testo sulla parte sinistra dello schermo e il tagset che hai scelto sulla parte destra.
![alt text](images/seminar-images/catma_final/8 Annotation Module.PNG)
*Fig. 8: Modulo Annotazione di CATMA*

Se si vuole annotare una parola o un passaggio di testo con un tag, bisogna semplicemente selezionare la parola o il passaggio in questione e premere il tasto destro del mouse: in questo modo apparirà il tagset che hai selezionato, affinché tu possa scegliere il tag che preferisci.

Vediamo alcune funzioni importanti di questo modulo:
- **Passaggi Discontinui**: Cliccando sull'icona a forma di libro nell'angolo in basso a sinistra e selezionando i passaggi del testo che ti interessano, potrai aggiungere una singola annotazione a parole o passaggi discontinui nel documento.
- **Overlapping tags**: Puoi anche applicare tag diversi ad uno stesso passaggio di testo.
- **Commenti**: Un'altra importante funzione è la possibilità di scrivere commenti su un passaggio di testo presente nel documento. Per farlo è necessario semplicemente selezionare il passaggio di testo in questione e cliccare sull'icona del commento che appare.


## 7. Modulo Analisi
In questa sezione puoi esplorare i testi e le annotazioni con le **query** e le **opzioni di visualizzazione**. Avrai il query builder sul lato sinistro dello schermo e le opzioni di visualizzazione sul lato destro.
![alt text](images/seminar-images/catma_final/9 Analyze Module.PNG)
*Fig. 9: CATMA's Analyze Module*

Le query ti permettono di analizzare, esplorare o valutare dati relativi al testo o alle annotazioni. Per [eseguire una query](https://catma.de/how-to/query-language/) sui documenti o sulle raccolte di annotazioni hai tre opzioni:
- Puoi selezionare una **query predefinita**, come mostrato nella figura in basso: ad esempio, la query “_Wordlist (freq0)_” mostrerà tutte le parole del documento analizzato la cui frequenza è superiore a zero (dunque otterrai tutti i token nel tuo testo e le loro frequenze corrispondenti).
![alt text](images/seminar-images/catma_final/10 Existing Queries.png)
*Fig. 10: Selecting an existing query*

- Puoi usare il **query builder** sul lato sinistro dello schermo per creare la tua query. Questa opzione è particolarmente utile quanto vuoi analizzare dei insdati molto specifici riguardo il tuo testo/ins (ad esempio: le parole che appaiono più di 20 volte nel tuo documento, quante volte appare una parola specifica, quante volte appare un tag e così via). Puoi usare il query builder sulla base di 5 criteri: per modello di parola o frase, per grado di somiglianza, per tag, per collocazione o per frequenza. Con questa funzione, CATMA offre la possibilità di creare query anche molto complesse (ad esempio, quante volte una specifica parola appare in prossimità di un'altra).
![alt text](images/seminar-images/catma_final/12 Build your query.PNG)
![alt text](images/seminar-images/catma_final/13 Query about collocation.PNG)
*Fig. 11-12: Crea la tua query (in questo caso, ho creato una query per collocazione in modo da vedere quante volte la parola "he" appare in prossimità della parola "has" in un intervallo di 5 token).*

- Puoi **scrivere direttamente una query**, se hai una certa familiarità con il linguaggio delle query su CATMA. Ad esempio, se si ha intenzione di vedere solo le parole del documento con una frequenza maggiore di 20, bisogna semplicemente digitare “*freq20*” nell'apposito spazio.

Dopo aver scelto una query o averne creata una, i risultati appariranno in un riquadro al di sotto del campo delle query. Tale riquadro ha anche un titolo che contiene la query stessa, un marcatore temporale e il numero totale di risultati.
![alt text](images/seminar-images/catma_final/11 Query Results.PNG)
*Fig. 13: Risultati della query*

### 7.1 Opzioni di Visualizzazione
insCATMA offre quattro diverse possibilità di visualizzazione per i risultati della tua query/ins (che appaiono sul lato destro dello schermo in questo modulo):
- **Visualizzazione KeyWord in Context (KWIC)**: Quest'opzione mostra i tuoi risultati nel loro contesto testuale (sia a destra che a sinistra) sotto forma di tabella. Cliccando due volte su una riga della tabella KWIC, puoi passare direttamente al Modulo Annotazione per vedere quel passaggio specifico. Puoi anche usare la visualizzazione KWIC per creare annotazioni semi-automaticamente (ne parleremo più nel dettaglio in seguito). Assicurati di selezionare la query esatta sul lato sinistro dello schermo.
![alt text](images/seminar-images/catma_final/14 KeyWord in Context.PNG)
*Fig. 14: Visualizzazione KWIC*

- **Visualizzazione di Distribuzione**: è un grafico che mostra la distribuzione dei risultati della query attraverso il testo. Per esempio, puoi creare la tua query (magari riguardo le occorrenze di una specifica parola o di un tag) e vedere con un grafico quante volte tali entità appaiono nel testo. CATMA permette anche di salvare il grafico in formato SVG o PNG.
![alt text](images/seminar-images/catma_final/15 Distribution Graph.PNG)
*Fig. 15: Visualizzazione di Distribuzione*

- **Visualizzazione Wordcloud**: Quanto più alta è la frequenza della parola nel documento, tanto più grande apparirà nel Wordclous. Proprio come nel punto precedente, puoi salvare l'immagine in formato SVG o PNG.
![alt text](images/seminar-images/catma_final/16 Wordcloud.PNG)
*Fig. 16: Visualizzazione Wordcloud*

- **Visualizzazione Doubletree**: Mostra la parola chiave e il suo contesto come un albero, i cui rami corrispondono al contesto della parola sia a destra che a sinistra. Il Doubletree può anche dispiegarsi, mostrando più contesto su entrambi i lati della parola.
![alt text](images/seminar-images/catma_final/17 Doubletree.PNG)
*Fig. 17: Visualizzazione Doubletree*

### 7.2 Annotazione Semi-Automatica
pUn'ultima funzione interessante nel Modulo Analisi è l'annotazione semi-automatica. Immaginiamo di voler taggare tutte le occorrenze di una specifica parola: se le occorrenze sono molte, farlo manualmente richiederebbe molto tempo. Questo è il motivo per cui su CATMA puoi farlo semi-automaticamente./p
Anzitutto, bisogna creare una finestra di visualizzazione KWIC e selezionare la query che ti permette di vedere tutte le occorrenze della parola che hai intenzione di taggare. Dopo aver selezionato i risultati che vuoi mostrare tramite la visualizzazione KWIC, bisogna cliccare sul pulsante con le tre righe (nell'angolo in alto a sinistra della tua finestra di visualizzazione KWIC), il che ti permette di selezionare le righe che vuoi selezionare: puoi selezionarle tutte o anche solo alcune di esse. A tal punto bisogna semplicemente cliccare sul pulsante con i tre punti (nell'angolo in alto a destra della finestra di visualizzazione KWIC) e cliccare su "Annota Righe Selezionate", che ti permette di scegliere il tag che preferisci.

![alt text](images/seminar-images/catma_final/18 Semi Automatic Annotations.PNG)
![alt text](images/seminar-images/catma_final/19 Semi Automatic Annotations Add Tag.PNG)
*Fig. 18-19: Creare annotazioni semi-automatiche e scegliere un tag*

Infine, ti verrà chiesto di scegliere una raccolta di annotazioni per documento. Dopo aver confermato, la tua annotazione semi-automatica è completata: le parole selezionate risultano ora annotate col tag che hai scelto.
![alt text](images/seminar-images/catma_final/20 Semi Automatic Annotations Select Annotation Collection.PNG)
*Fig. 20: Selezionare una raccolta di annotazioni durante la creazione di annotazioni semi-automatiche*


## 8. Export and Further Exploration
If you will want to use your results in an essay or presentation, you can export and download your data on CATMA. Here you can see what is the section you have to go to depending on what you want to download:
- **Export annotations**: Project Module
  (available in .txt, .xml and .csv)
- **Export query results**: Analyze Module (available in .txt, .xml and .csv)
- **Export visualization options**: Analyze Module
(The Wordcloud and the Distribution Graph are available in .svg and .png, whereas the KWIC Visualization is available in .csv).