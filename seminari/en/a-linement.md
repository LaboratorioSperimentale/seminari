---
layout: seminar
title: "A-linement: Un tool di importazione e allineamento sottotitoli per la ricerca scietifica"
author: letiziastrocchi
speaker: Francesco Vitucci, Michele Zangheri 
---

# "A-linement": Un tool di importazione e allineamento sottotitoli per la ricerca scientifica

## Che cos'è A-linement

A-linement è un software, che esiste in versione open access online, utilizzato nell'ambito della traduzione audiovisiva interlinguistica.

A-linement è un **tool** che aiuta, chi lo utilizza, nell'analisi qualitativa e poi quantitativa delle traduzioni interlinguistiche. Questo strumento nasce dalla necessità di concentrarsi su alcuni aspetti delle lingue, in particolare sulle traduzioni e sottotitolazioni interlinguistiche. A-linement si concentra anche, in modo particolare, sull'analisi comparativa della punteggiatura tra lingue diverse.

A-linement lavora per *frame*, ovvero fotogrammi all'interno dei quali vengono visualizzati le stringhe contenenti i sottotitoli. Il risultato finale sarà una tabella dove vengono comparati ed allineati i vari sottotitoli. il **tool** di A-linement può essere  utilizzato per l'analisi, sia di scene brevi tratte da film contenenti per esempio 35 battute, sia per interi film/docufilm. 

inserire foto tabella da chiedere a vitucci

Grazie a questo strumento è alla fine possibile capire come è avvenuta la sottotitolazione a livello diacronico. 

## Come utilizzare A-linement

Lo strumento di A-linement comunica con il software Excel, ovvero produce in automatico delle tabelle Excel che possono essere subito incluse nelle proprie varie ricerche linguistiche. 

immagine interfaccia vitucci

(A-linement, ancora sottoforma di link, è raggiungibile trammite il profilo Github di Paolo Pirruccio, sarà però presto disponibile in versione software accessibile anche senza connessione ad Internet.)

A-linement si presenta con una interfaccia principalmente bianca caratterizzata da diversi tasti verdi, al disotto di questi ci sono varie colonne (dieci per l'esattezza) in cui verrano poi inserite le varie traduzioni in lingue diverse.

### I *pulsanti* di A-linement e come utilizzarli

- "**Convert to table**": motore del tool, è il pulsante tramite il quale è possibile convertire i dati in tabella, tabella che verrà poi importata su Execel, e che sarà possibile utilizzarla nel medesimo istante per la propria ricerca.

*Primo Step*:
importare i dati all'interno di A-linement, questo è possibile grazie al pulsante "**Scegli il file**": selezionando il file desiderato dalla cartella di appartenenza, questo apparirà al fianco destro di tale pulsante. (Il file deve essere in formato SRTOASS.)

  Successivamente cliccando sul pulsante "**Convert subs file**" apparirà una finestra contenente il "**Conversion output**" ovvero il testo da analizzare. (Con testo si intende il dialogo di qualsiasi contenuto audiovisivo.) Tramite il pulsante "**Copy subtitles**" verrà copiato l'intero contenuto, nel caso si volesse andare a studiare solo una parte di testo, basta selezionarla e copiarla con Ctrl+C. 

*Secondo Step*: 
incollare il contenuto sulla prima colonna di A-linement con Ctrl+V. Le colonne possono essere rinominate, per esempio: Column1 in , Column2 in , Column3 in , e così via. 

  Se si vuole già trasformare questo contenuto in tabella serve utilizzare il pulsante "**Convert to table**", ma facendo ciò il passaggio da una stringa di testo ad un'altra viene letto come un'ulteriore nuova stringa, che in tabella viene visualizzata come una stringa vuota. 

inserire immagine stringa vuota tra testo 

*Terzo Step*: per risolvere va inserito il simbolo *asterisco* (*), questo grazie al pulsante "**Replace newline**" che sostiuisce tutti gli *a capo* creati nel passaggio da una stringa ad un'altra. 

Cliccando "**Convert to table**" ora ogni stringa è al suo posto. 

Altri comandi:

- "**Reset**": come dice il nome stesso, per eliminare ogni contenuto e ricominciare da capo. 

- "**Bold text**": per evidenziare parti di testo specifiche, cliccando questo pulsante si apre una casella di testo dove va digitato il testo desiderato, il quale riappare inscritto tra <b> e </b> ... Successivamente copiare ed incollare il testo in tabella, ed una volta convertito in tabella il testo appare già in **grassetto**. 

- "**Save**": per salvare in local sul device con cui si opera. 

- "**Load**": per ricaricare l'ultima versione di testo salvata in caso di reset o cancellazione di quest'ultima. 

- "**Export json**": per creare un file di salvataggio esportabile da spostare tra device diversi o da condividere a qualcuno. Cliccando sul pulsante, viene chiesto di salvare il file con estension .json e per caricarlo sul programma cliccare "**Scegli il file**" ed in seguito "**Convert subs file**". 

## Come importare grandi quantità di file su A-linement 
