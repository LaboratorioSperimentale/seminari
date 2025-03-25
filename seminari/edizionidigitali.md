---
 title: "Introduzione alle edizioni digitali"
 author: giuliamarmo
---

# Introduzione alle edizioni digitali

## Indice
  - Introduzione: cosa sono le edizioni digitali
  - 1. Concetti di base della filologia digitale
  - 2. Edizioni digitali vs. cartacee
  - 3. Storia ed evoluzione delle edizioni digitali
  - 4. Tipologie di edizioni digitali
  - 5. Tecnologia e formati per le edizioni digitali
  - 6. Codifica e marcatura testuale
  - 7. Problemi e sfide delle edizioni digitali
  - 8. Il ruolo del filologo digitale
  - 9. Conclusioni
  - 10. Che cos'è la TEI
  - 11. Metodi di collegamento
  - 12. Metodo parallel segmentation



  ## Introduzione: cosa sono le edizioni digitali
  Il seminario è tenuto da Alberto Rosselli Del Turco e si concentra su quali sono le *edizioni digitali*, la *filologia digitale* e il loro impatto sugli studi umanistici.

  ## 1. Concetti di base della filologia digitale
  La filolgia digitale è definita come l'applicazione di strumenti e metodi informatici alla critica testuale per la creazione di edizioni digitali (diplomatiche, critiche, filologia d'autore, ecc). l'obiettivo principale è produrre un *testo affidabile* per lo studio accademico, come avviene nella filologia tradizionale.

   1.1 Differenze con la filologia computazionale

   La *filologia computazionale* si concentra sullo sviluppo di strumenti software per l'analisi automatizzata dei testi. La *filologia digitale* utilizza strumenti digitali per realizzare edizioni accademiche.

   1.2 Evoluzione della terminologia

 Nel tempo sono stati usati diversi termini per descrivere le edizioni digitali:

- *Filologia computazionale* (Bozzi) focalizzata sul software;
- *Edizione elettronica*, termine usato negli anni '90;
- *Edizione digitale*, termine attuale che sottolinea la specificità accademica.

## 2. Edizioni digitatali vs. cartacee
Le edizioni digitali differiscono da quelle cartacee in vari aspetti:

- *Struttura ipertestuale*: permettono di navigare tra testo, immagini e metadati.
- *Interazione con il lettore*: possono includere strumenti di ricerca avanzata.
- *Aggiornabilità*: è possibile aggiornarle e modificarle nel tempo.
- *Accessibilità*: possono essere distribuite su web senza limiti fisici.

2.1 Vantaggi rispetto alle edizioni cartacee

| Aspetto  |  Edizione cartacea  | Edizione digitale   |   |   |
|---|---|---|---|---|
|Struttura    |  Lineare  | Ipertestuale  |
| Spazio per il testo   |Limitato   | Illimitato  |
|Apparati critici   |Sintetici   | Completi e navigabili  |
| Costi di produzione | Elevati | Ridotti |
| Facilità di aggiornamento | Difficile | Immediato |


2.2 Limiti delle edizioni cartacee:

- Spazio fisso per testo e apparti critici.
- Linguaggio di apparato sintetico e compresso.
- Mancanza di varianti ortografiche.
- Costo elevato della stampa di edizioni sinottiche.

## 3. Storia ed evoluzione delle edizioni digitali
Negli anni '90 le prime edizioni digitali erano su supporti ottici (CD\DVD), spesso limitate e dipendenti da software proprietario. Con il passaggio al web si elimina il problema della compatibilità con vecchi software e si ha una diffusione più ampia.

## 4. Tipologie di edizioni digitali
- Biblioteche digitali e database testuali (es. Oxford Text Archive)
- Edizioni ipertestuali (es. Electronic Beowulf con immagini e trascrizioni)
- Edizioni basate su immagini (riproduzioni facsimilari con trascrizione diplomatica)
- Edizioni collaborative e sociali (es. crowdsourcing per trascrizioni)
- Aggregatori di edizioni digitali (es. MESA per il Medioevo, NINES per il Novecento)

  ## 5. Tecnologie e formati per le edizioni digitali
  - Formato testo: XML-TEI (Text Encoding Initiative) è lo standard per la codifica testuale accademica.
  - Formato immagini: JPEG, TIFF, IIIF (International Image Interoperability Framework).
  - Software di pubblicazione: Oxygen XML Editor, EVT (Edition Visualization Technology).
  - Indipendenza da hardware/software: XML garantisce accessibilità su qualunque piattaforma.

  ## 6. Codifica e marcatura testuale
  Il testo deve essere marcato per il suo significato, non per il suo aspetto. *XML* permette di descrivere la struttura del testo (capitoli, paragrafi, versi), gli elementi critici (varianti, correzioni, annotazioni), i collegamenti ipertestuali tra documenti. Ovviamente, XML ha anche dei limiti poichè non supporta gerarchie multiple e ciò richiede a volte soluzioni complesse.

  ## 7. Problemi e sfide delle edizioni digitali
  - Durata nel tempo: le edizioni devono essere conservate in formati standard per garantirne la leggibilità futura.
  - Riconoscimento accademico: le edizioni digitali devono essere riconosciute e valutate alla pari delle pubblicazioni cartacee.
  - Formazione: i filologi devono acquisire competenze digitali per poter creare e gestire edizioni digitali in autonomia.

## 8. Il ruolo del filologo digitale
Il filologo digitale deve avere competenze in:

- filologia tradizionale (critica testuale, stemmatica, trascrizione).
- XML-TEI per la marcatura testuale.
- tecnologie web (HTML, CSS, JavaScript per la pubblicazione).
- metodi di analisi dati (ontologie, linguaggi di programmazione come Python o JavaScript).

Inoltre, il filologo digitale deve collaborare con informatici umanisti: il filologo non deve essere un programmatore, ma deve conoscere le basi delle tecnologie digitali per lavorare in team interdisciplinari.

## 9. Conclusioni
Le edizioni digitali sono strumenti di ricerca, non di lettura. sono più flessibili delle edizioni cartacee, ma richiedono un cambio di mentalità e competenze. Il filologo deve adattarsi a nuove metodologie e strumenti digitali. Ovviamente, le edizioni digitali non sostituiscono le edizioni cartacee, ma le integrano, permettendo una fruizione più ampia e interattiva.

## 10. Che cos'è la TEI
La *Text Encoding Initiative* è uno standard internazionale per la codifica e la rappresentazione digitale di testi in ambito umanistico, archivistico e bibliografico.
Ha divesi tipi di moduli, tra cui quelli utili per un'edizione diplomatica:

- msdescription, per la descrizione del manoscritto;
- transcr, per la trascrizione di fonti primarie;
- textcrit, per la gestione dell'apparato critico;
- analysis, elementi per l'analisi del testo;
- gaiji, modulo che permette di gestire caratteri non standard.

Il modulo *textcrit* (Critical Apparatus) è il più datato di tutti i moduli TEI.
Questo modulo offre elementi per la codifica dell'apparato critico (gestione dei testimoni) e metodi per collegare le voci dell'apparato critico al testo.

Tra gli elementi per l'apparato critico troviamo:

- *app* voce di apparato critico
- *lem* indica la lezione del testo base
- *rdg* una variante rispetto al testo base
- *note* nota critica, può contenere un'intera, più discorsiva voce d'apparato.

## 11. Metodi di collegamento
TEI predispone tre metodi diversi per collegare l'apparato critico con il testo base:

- metodo *location-referenced*
- metodo *double-end-point-attached*
- metodo *parallel segmentation*

Ognuno presenta vantaggi e svantaggi, il più usato è il metodo *parallel segmentation* per vari motivi.

Tra i vantaggi:

- codifica in-line, più intuitivo rispetto al metodo *double-end-point-attached*
- varianti possono annidarsi (si può provare a sovrapporle, con un po' di creatività, ma non è raccomandato!)
- consente di ricostruire il testo di tutti i testimoni (come il metodo double-end-point-attached)
- supporta < app > senza < lem > ovvero si può fare a meno di un testo base

## 12. Metodo parallel segmentation
Il più popolare e diffuso perchè è il più semplice e conveniente. Ha anche degli svantaggi:

- le varianti possono annidarsi (ma non possono sovrapporsi)
- solo in-line, niente apparato esterno (markup di tipo *stand-off*)
- meno adatto per tradizioni complesse.








