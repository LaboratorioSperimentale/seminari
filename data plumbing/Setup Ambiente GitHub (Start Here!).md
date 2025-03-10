
#### KEYWORDS: Progetti Collaborativi, Editor di Testo, Versioning, Markdown, Github, Visual Studio Code

# 3 STRUMENTI FONDAMENTALI PER PROGETTI COLLABORATIVI 
Un progetto collaborativo presuppone, innanzitutto, di poter condividere risorse (files). A tal fine esistono strumenti che consentono la condivisione in maniera efficiente e affidabile. 

Una soluzione possibile si basa su Gitbub un repository (spazio cloud) centralizzato che consente di condividere files e, nel caso di file in formato testuale, consente il "versioning" (cioè, ogni operazione di salvataggio sul repository centralizzato è come fosse un punto di backup specifico cui è possibile ritornare in caso di necessità). 

# PREPARAZIONE DELL'AMBIENTE DI LAVORO
Procediamo quindi con:
1. creazione di un un account **Github**;
2. installare **Visual Studio Code** (editor di testo evoluto!) sul proprio computer;
3. installare un **client Git** da sul proprio computer
isto.

### CREAZIONE ACCOUNT GITHUB
- Andare sul sito https://github.com/ e creare un proprio **account github** ("Sign up for Github")

![](attachment/9066b619504b39fb26cf907c1b632f80.png)

### INSTALLAZIONE VISUAL STUDIO CODE (VSC)
- scaricare ed installare la versione di Visual Studio Code adatta al proprio sistema operativo da:
	- https://code.visualstudio.com/Download
- dopo aver scaricato il software effettuare l'usuale doppio-click col mouse sul file eseguibile (**Windows**) normalmente disponibile nella cartella **Download** 

![](attachment/c2d15c1f0ada905c71a914894734702f.png)

### INSTALLAZIONE CLIENT GIT
- scaricare ed installare la versione di **Git** adatta al proprio sistema operativo da:
	- https://git-scm.com/downloads
  - dopo aver scaricato il software effettuare l'usuale doppio-click col mouse sul file eseguibile (**Windows**) normalmente disponibile nella cartella **Download**

![](attachment/b427e1ab5bdbd8f0d4b6eb818374f700.png)

- Il client git sul nostro computer ci consentirà di interagire, utilizzando Visual Studio Code, con il repository GitHub centralizzato.

# CONFIGURAZIONE DELLA COLLABORAZIONE DELL'AMBIENTE DI LAVORO
Ora che disponiamo di un account Git possiamo configurare VSC e GIT in modo da interagire con il repository GitHub.


### CONNESSIONE DI VISUAL STUDIO CODE A GITHUB (viene fatta una sola volta poi resta attiva... fino a disconnessione esplicita)
- Vogliamo consentire a Visual Studio Code di interagire col repository Github, utilizzando le utility (comandi) che il pacchetto Client Git ci mette a disposizione.

![](attachment/852ef0ea433f7a4853090b9481038566.png)

![](attachment/38b788d02d7aadae805968616d65ef56.png)

![](attachment/8bdc382bc24df3089033315274182b04.png)
- Viene richiamata la pagina web di login del browser di default
![](attachment/c623d5faf7ed1728f9b8fea02034d730.png)

### VOGLIAMO ORA CLONARE LA CARTELLA PRESENTE SU GITHUB IN LOCALE
1. Accediamo al nostro github (dopo che abbiamo accettato l'invito via mail conseguente a qualcuno che ci condivide una cartella github!) e andiamo nella cartella condivisa (click sul pulsante CODE -verde- e copiamo la path HTTPS, che è il link alla specifica cartella "formazione-knowledge base"):
![](attachment/29a0caf14e22512fc5c0c56562035928.png)
1. Da Visual Studio Code apriamo un terminale: menu Terminal > New Terminal 
![](attachment/f80cd989ca2923b49bd60bd49bca0525.png)
1. Ora vogliamo clonare il repository github, che non è una semplice cartella poiché contiene una serie di elementi che consentono poi di ereditare tutte le funzionalità proprie di github (fra cui il versioning!!):
   Nel terminale apriamo un **githbash (o bash)** che ora disponibile in VSC grazie all'installazione del componente **Git Client**.
   - sceliamo gitbash o bash:
  ![](attachment/8fe2346357bf4a98a44ee10b981e7876.png)
- ora è visibile bash (a fianco della tendina):
![](attachment/80f5b305bc7066536dd995f6e179d4fc.png)
- digitiamo il comando **git clone** + spazio poi la path https:
![](attachment/48cbdc5156ddf3dcb8ddf4af45d57282.png)
- quindi ci viene richiesto di attivare il processo di **sign in usando GitHub**
![](attachment/99bc91d022c5579ee53565ca78458278.png)

- procediamo; quando diamo "allow" il processo di sign in resta in attesa in VSC che sia fatto sul browser di default (che viene aperto). Se siamo già loggati la procedura di cloning si avvierà... altrimenti procediamo alla login:
![](attachment/724d766d744eb873f5da3ca36e046904.png)

![](attachment/fc0c6413a0a97bfccaf5d1d25791eb5f.png)

![](attachment/f166a603033caef3533b32f1fa9f073a.png)
- Al termine il browser ci chiede autorizzazione ad aprire l'app che deve eseguire il cloning... clicchiamo open:
![](attachment/3d97b37adcaebf48b9df7d2cd6b998cb.png)
- la procedura di cloning si conclude nel terminale aperto in VSC:
![](attachment/04d4231cba5e169e66e325844bf0900b.png)
- notiamo, alla terza riga:
	- **Cloning into *'Formazione-knowledge_base'***



### APERTURA E VISUALIZZAZIONE DELLA CARTELLA GITHUB CLONATA (ORA DISPONIBILE IN LOCALE)
 - per aprire il clone locale la dobbiamo trovare entro il nostro file system
- nel terminale digitiamo: **pwd**. Questo comando da come risposta dove ci troviamo 
- nel mio caso mi restituisce la mia home: /home/car 
![](attachment/99a6e48e1ddaeed35be78a0eca1f89f4.png)
- torniamo a VSC e apriamola: menù File > Open Folder e identifichiamo la cartella nell'esplora risorse che viene aperto.
![](attachment/2d02646df8bda44a58f66e056be12b4c.png)
- facciamo open (nell'immagine in alto a destra):
![](attachment/234d16f7c372a5461156a57e465610c1.png)
- ultimo step... di sicurezza: conosciamo chi è che ha creato la cartella e possiamo fidarci dell'autore (nota che durante il cloning TUTTO quello che è nel repository viene copiato in locale... occorre sapere chi è che ha condiviso cosa!!!)
![](attachment/e171ca628a1abe3ab5222d7cd01d8732.png)


# CREAZIONE DI FILE IN LOCALE E COPIA (UPLOAD) NEL REPOSITORY COMUNE (GITHUB)

- procedo creando una cartella denominata Carmelo e ci creo all'interno un file prova.md:
![](attachment/33aa92711f361af2c8c16edb9c096981.png)
![](attachment/1c338eed80d053a2954ef633bbceee2d.png)
- passo a **SOURCE CONTROL** (nota che già appare "1", cioè c'è una modifica che può/richiede di essere committata):
![](attachment/9105978cfc1dacb8dd8f478094e2eb5b.png)
- quello che può essere committato appare anche ora (nel source control);
![](attachment/0de6b3a0e7911e38aba85ac84518c65c.png)
![](attachment/207f64f90a01792cbf3d7c024e877b4d.png)
- prima di eseguire il commit assegno un nome e premo invio:
![](attachment/8a7ddfcfb6e1a0aad81bdc2a7bae087c.png)
- 
- se ottengo una richiesta posso anche ottemperare, altrimenti procedo otre(vedi:https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup):
![](attachment/ad44e836743c2c288c9244c02c16a249.png)
![](attachment/95ffd3c8e74e852d8f4aa1e3d9b3f0ef.png)

- Ora il file è entrato nel repository (da questo momento il file eredita tutte le funzionalità proprie di github, fra qui il source control)... ma è presente solo in locale... gli altri utenti non lo vedono. Procedo col **Sync Changes** 

![](attachment/6c910dd0c54a8490a943bab5875921d5.png)

![](attachment/dedb39c21c0192b2aea9707f40a70202.png)



# COME APPARE ORA IL REPOSITORY
![](attachment/bfdd9289116d4b8e413f68863303012d.png)
![](attachment/537ee3b361a2fe98c7683c6318d892b2.png)