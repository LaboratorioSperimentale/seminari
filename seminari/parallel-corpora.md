---
layout: seminar
title: "Designing and compiling parallel aligned corpora for SketchEngine"
seminar_title: "Designing and compiling parallel aligned corpora for SketchEngine"
date: "16.04.2021"
author: silviamantovani
speaker: jorgeleiva
video_title: "Designing and compiling parallel aligned corpora for SketchEngine"
video: ""
length: 4h
unibo: yes
---

#### Table of Contents
- [Designing and compiling parallel aligned corpora for Sketch Engine](#designing-and-compiling-parallel-aligned-corpora-for-sketch-engine)
  - [Basic considerations](#basic-considerations)
    - [Parallel aligned (or translation corpora)](#parallel-aligned-or-translation-corpora)
    - [Already-compiled corpus or DIY corpus?](#already-compiled-corpus-or-diy-corpus)
      - [Already-compiled corpus: Disadvantages](#already-compiled-corpus-disadvantages)
      - [Already-compiled corpus: Advantages](#already-compiled-corpus-advantages)
  - [Using already-compiled corpora in Sketch Engine for translators](#using-already-compiled-corpora-in-sketch-engine-for-translators)
    - [Review of tasks with monolingual corpora in Sketch Engine](#review-of-tasks-with-monolingual-corpora-in-sketch-engine)
    - [Available corpora in Sketch Engine](#available-corpora-in-sketch-engine)
  - [Introduction](#introduction)
    - [Main advantages and drawbacks](#main-advantages-and-drawbacks)
      - [Compiling your own parallel corpus: Advantages](#compiling-your-own-parallel-corpus-advantages)
      - [Compiling your own parallel corpus: Disadvantages](#compiling-your-own-parallel-corpus-disadvantages)
    - [Setting the basis for corpus compilation](#setting-the-basis-for-corpus-compilation)
    - [Some conditioning factors and text types](#some-conditioning-factors-and-text-types)
      - [Literary texts](#literary-texts)
      - [Journalistic texts](#journalistic-texts)
      - [Websites](#websites)
      - [User manuals and online help files](#user-manuals-and-online-help-files)
      - [Tweets](#tweets)
      - [Subtitles](#subtitles)
      - [Press releases](#press-releases)
      - [Translation memories](#translation-memories)
  - [Compiling a parallel corpus](#compiling-a-parallel-corpus)
    - [Selecting and finding your texts](#selecting-and-finding-your-texts)
      - [A case study: a parallel corpus of museum texts](#a-case-study-a-parallel-corpus-of-museum-texts)

# Designing and compiling parallel aligned corpora for Sketch Engine

## Basic considerations

### Parallel aligned (or translation corpora)
According to Baker, parallel corpora consist "of original, source language texts in language A and their translated versions in language B" (Baker, 1995: 230). For that reason, parallel corpora are also called "translation corpora". In this workshop, language A will be Italian and language B will be English.
Currently, **corpus linguistics** is a relevant methodology in Translation Studies research, as revealed by Fantinuoli and Zanettin: "in the last ten years or so about 1 out of 10 publications in the field [of Translation Studies] has been concerned with or informed by corpus linguistics methods" (Fantinuoli and Zanettin, 2015:8). Despite the relevance of parallel corpora, available tools either have limited features or have been developed for specific, not-accessible research or projects.
Furthermore, aligned parallel corpora are not frequently addressed  by research in corpus linguistics.
<!-- We will explore the reasons for this later. -->
Beyond the challenges of finding suitable tools, another obstacle in the creation of parallel corpora is **alignment**. One of the first definitions of alignment is "finding correspondences, in bilingual parallel corpora, between textual segments that are translation equivalents" (Kraif, 2002:273). This means that, for example, if one extracts text from a brochure from a museum and it says "Informazione sulla mostra", one will have to align it to the corresponding translation equivalent, namely "Information on the exhibition".

Although not new, Kraif's definition is still valid.
However, it's important to note that alignment does not necessarily have to be only bilingual: parallel corpora can include more than two languages (EAGLES, 1996: 9; Frankenberg-Garcia, 2009: 57; Zanettin, 2012: 150).
If the corpus is bilingual (such as in this seminar), then the text resulting from alignment will be a "bitext" (Harris, 1988), even though "bilingual text" or "aligned text" are also acceptable.

Different degrees of parallelism (alignment) are possible: since correspondence on a text level to correspondence on a word level (Véronis, 2000: 6-ff; Zanettin, 2012: 149; Faya Ornia, 2025: 352).

- **Text-level alignment** involves matching entire texts. For example, considering the museum brochure mentioned earlier, this would mean aligning the entire Italian text with the entire English text. In general, this approach is not preferred because it is often too coarse for research purposes. Finer alignment is generally required.

- **Paragraph-level alignment** matches corresponding paragraphs. For instance, paragraph one in Italian would be aligned with paragraph one in English, paragraph two with paragraph two, and so on. This provides a more refined alignment than text-level, but may still lack precision.

- **Sentence-level alignment** matches individual sentences. This is a common and often effective approach.

Word-level alignment seeks to match individual words and even though it is also considered, it may not yield reliable results, due to linguistic differences and ambiguities. linguistic or structural differences??

Among these, sentence-level alignment is widely recognized as the *de facto* standard (Zanettin, 2012: 155). In translation memory terminology, this corresponds to alignment at the translation unit or segment level, depending on the specific translation software employed. This type of alignment will be the focus of today's demonstration.

Since the first work on sentence-level alignment performed by Kay and Röscheisen in 1987 (Kay, 2000: XV), a number of tools and increasingly automated processes has emerged (cf. Section 4.2 in this seminar).

Complexity of the process results from the type of alignment desired or, in other words, "[t]he finer the alignment, the more complex it becomes" (Frankenberg-Garcia, 2009:61).
But the complexity of the alignment process is also due to the type of text involved. Consider, for instance, the alignment of an Italian-English user guide. In this case, the alignment is usually easier because the target text closely mirrors the source text, with near-complete correspondence. However, when the translated text has missing paragraphs or some of the paragraphs are summaries of the source text content, the alignment procedure will be more challenging.

### Already-compiled corpus or DIY corpus?

When using parallel corpora, is it preferable to use an already-compiled corpus or to build one by scratch (a sort of DIY corpus)? This section will explain the perks and drawbacks of both approaches.

#### Already-compiled corpus: Disadvantages

One primary drawback of already-compiled corpora is their limited availability (Granger, 2010: 5; Zanettin, 2012: 153-154), a consequence of the effort required for their compilation (Véronis, 2000b: 15; Sharoff, 2002: 449). The complexity and time-consuming nature of creating parallel corpora, compared to monolingual corpora, result in fewer available options.
Furthermore, parallel corpora are usually smaller compared to monolingual and comparable corpora for the following reasons:

- compilation time: the process of sourcing and aligning parallel texts is exceptionally time-consuming.
- domain specialization: the more specialized the domain is, the smaller the corpus will be (Zanettin, 2012: 152). For example, while a corpus of translated literature might be extensive, a corpus focusing on 19th-century Philippine literature translations will be considerably more limited.
- translation dependency: the nature of the texts themselves, since they are translations, is a determinant factor (Nádvorníková, 2017: 3). Even though parallel corpora require both source and translated texts, the availability of translations is often restricted, with only a small fraction (1% or less) of texts being translated, thus affecting corpus size.

#### Already-compiled corpus: Advantages

Already-compiled corpus: Advantages
Creating parallel corpora is difficult and not many people do it.
Furthermore, the increasing availability of texts in specialized domains, alongside advancements in technology, has made the creation of corpora focused on less common areas more accesible/achievable/possible to achieve than previously (McEnery and Hardie, 2012: 4; Fantinuolli and Zanettin, 2015: 1).
A significant shift in corpus linguistics is the reduced emphasis on corpus size. While large corpora were once considered essential, recent research indicates that size is less critical than initially believed. Consequently, the smaller size of parallel corpora, due to their nature, is no longer considered a significant drawback.
Being specialized and aligned corpora, they will be smaller than general or monolingual corpora. Current trend not to prevail the size of corpora (Anthony, 2013: 146; Scheer, 2013: 1; Rojo, 2015: 376, Nádvorníková, 2017: 3-ff). In fact, Arbach y Ali very clearly mention the "necessité de corpus moins grands, plus spécifiques" (2013: 11).
One of the advances in corpos linguistics that we could not foresee was that corpora were going to be not only bigger but also smaller.

## Using already-compiled corpora in Sketch Engine for translators

### Review of tasks with monolingual corpora in Sketch Engine

Sketch Engine offers a variety of options. Some of them are listed below ([documentazione](https://www.sketchengine.eu/quick-start-guide/)):

- Word sketch: to analyze a word, for example "exhibition", and find out adjectives, nouns, or verbs that are usually associated with that word;
- Word sketch difference: to compare two similar words within our corpus, e.g. "exhibition" and "exhibit", and to identify the frequency with which the two words are associated with certain verbs, adjectives, nouns, etc.
- Thesaurus: to generate a synonym-based glossary;
- Corpus creation: enabling the creation of both monolingual and bilingual corpora;
- Single word keywords and multi-word terms (available for user-created corpora);
- Word lists: to identify frequent words, and to filter by specific word categories (e.g., frequent adjectives) due to Sketch Engine's text tagging.
- Concordance: to view keywords in context.

### Available corpora in Sketch Engine

Select corpus > Advanced > Corpus Category: Parallel

Primary: Italian
Aligned: English

9 already-compiled corpora available on Sketch Engine to date
<!-- (magari può essere la didascalia allo screenshot con tutti i parallel corpora dall'italiano all'inglese??) -->
If you change the order, from English into Italian, you're going to have the same because Sketch Engine doesn't really care about the direction of the translations, which might be a problem. It's not the same to have Italian as the source language and Italian as a target language.

By clicking on one of them, for example EUR-Lex 2/2016 parallel – Italian, you will access a new feature, "Parallel Concordance", which is not available for monolingual corpora. Selecting this feature redirects you to this page (inserisci screenshot). In the "Search" box you can enter a word in Italian, e.g. "scadenza", and find out its English equivalent. Make sure the source language is set to Italian and the target language to English, then click on 'Search'.

The time needed for the page to load depends on the size of the corpus. In this case the corpus is quite large as it contains 606,070,097 words. Once the page has loaded, it's possible to know the number of occurrences or "hits" in the box at the upper left corner (71,311 for "scadenza").

Sketch Engine highlights the suggested English equivalent in yellow. Once "scadenza" appears in Italian "date" is a recurring word appearing in the English translation.
<!-- Also, note that the alignment in this corpus is not precise as it often matches multiple Italian sentences with multiple English sentences, rather than a one-to-one correspondence. -->
<!-- forse al posto di "not precise" potrei mettere "non è molto utile ai fini della ricerca" o una cosa del genere, perché per essere preciso sembra preciso. ?? -->

If you wish to examine the English translations of 'scadenza' within this parallel corpus, use the filter function. Given the 71,311 results, manually reviewing each occurrence is impractical.

<!-- To use a more limited and therefore manageable corpus, we are going to switch to [purtroppo il corpus indicato dal professore non è stato ancora reso pubblico. Non so se mettere le slide del suo esempio oppure cercare un altro esempio in italiano poiché l'esempio in spagnolo non potrebbero vederlo nella pratica??]

- the recall releases corpus created by professor Jorge Leiva, called "Alertas alimentarias 2020, English" , even though it is not accessible yet and we can share only some screenshots of it.
For example, let's say I want to see how "beef" is translated into Spanish. There are 2661 occurrences of "beef" translated as "carne".
But often there is also "res" together with "carne", in the expression "carne molida de res", which means "ground beef" in English. "Res" is as they call beef in Mexico and other parts of Latin America and instead of "ternera". If I want to see how many equivalents of "beef" are in Spanish... [qui non ha spiegato come si fa] -->

<!-- - the EUR-Lex judgments 12/2016 parallel – English.

Un'altra opzione sarebbe di riportare l'esempio, o del corpus del professore o del corpus EUR-Lex judgments 12/2016 parallel – English, già dall'inizio, escludendo l'esempio di scadenza dato che le hits erano troppe. Per il corpus EUR-Lex judgments 12/2016 parallel – English posso portare l'esempio di "beef", come fatto dal professore, ma anche di altre parole.
altra cosa: le parole come res, ternera ecc. sarebbe meglio metterle tra virgolette o in corsivo? -->

<!--
the corpus is: MUSA21, 07.04.2021, English [anche questo corpus non c'è perché il professore non lo ha reso disponibile, ad ogni modo per questo va benissimo anche un corpus monolingue] -->
To identify the adjectives commonly associated with "exhibition," particularly those that immediately come before the term, you can use the "Frequency" feature. By selecting the lemmas of the first word to the left, it becomes possible to determine the most frequently used adjectives. Upon doing so, the results reveal that the most common adjective paired with "exhibition" is "special," followed by "major," "new," and others in descending frequency.
When identifying the Spanish equivalents of "exhibition", you'll notice there are mainly two possible words, "exposición" and "exhibición". frequency analysis feature is accessible for the English side of the corpus but does not function for the Spanish side. Even though it is not possible to arrange the Spanish translations by frequency, filtering remains an option. In  is also essential to consider the total number of occurrences, which in this case amounts to 2902.  We can filter by asking Sketch Engine to tell me how many times "exposición" appears but also how many times it doesn't appear because I know there are going to be many occurrences. So I can select "does NOT contain", so filter by paragraphs not containing "exposición" and I have to substract the number of hits with a result. Now exposición is gone and I can have all the occurrences not cointaining "exposición", which are 991. So the occurrences of "exposición" are 2902-991, which is 1911. And I can do the same with "exhibition".

<!-- (Copilot)
When identifying the Spanish equivalents of "exhibition," you'll notice two primary options: "exposición" and "exhibición." While the frequency analysis feature is available for the English side of the corpus, it doesn't work for the Spanish side. This means we can't rank Spanish translations by frequency, though filtering is possible. It's also important to consider the total number of occurrences, which in this case is 2902.
To filter, Sketch Engine can show how many times "exposición" appears and how many times it doesn't. Since "exposición" is expected to have numerous occurrences, you can choose the "does NOT contain" filter to exclude paragraphs containing "exposición." By subtracting the filtered results from the total hits, you can determine the remaining occurrences. For example, excluding "exposición" leaves 991 occurrences. Subtracting this from the total 2902 occurrences reveals that "exposición" appears 1911 times. A similar approach can be applied to analyze "exhibition."


When seeking the Spanish equivalents of "exhibition," two primary options emerge: "exposición" and "exhibición." Although the frequency analysis feature is available for the English side of the corpus, it does not function for the Spanish side. Consequently, while it is not possible to arrange the Spanish translations by frequency, filtering remains an option. It is also essential to consider the total number of occurrences, which in this case amounts to 2902.
To apply filtering, Sketch Engine can indicate how many times "exposición" appears and how many times it does not. Since "exposición" is expected to occur frequently, one can utilize the "does NOT contain" filter to exclude paragraphs that include "exposición." By subtracting the filtered results from the total occurrences, the number of instances of "exposición" can be determined. For example, excluding "exposición" results in 991 occurrences. Subtracting this figure from the total of 2902 reveals that "exposición" appears 1911 times. A similar method can be employed to analyze "exhibition."
I hope this strikes the right balance! Let me know if you'd like me to refine it further.

Ci ritorno più avanti 47:08 fino a 53:36

Qui spiega l'utilità di tre dei corpora che si trovano su Sketch Engine quando si cerca un corpus parallelo dall'Italiano all'Inglese (o viceversa). Il problema è che ho trovato corpora con nomi diversi e non so quindi se siano gli stessi.

56:08

59:13 comincia a spiegare come compilare un corpus parallelo per proprio conto -->

## Introduction

### Main advantages and drawbacks

#### Compiling your own parallel corpus: Advantages

Firstly, **the design is entirely customizable**, allowing researchers to precisely define the desired characteristics of the data. For instance, one could specifically curate texts originating from the Philippines during the 19th century and translated by female individuals.
Consequently, this approach facilitates the **exploration of less-studied domains**, in contrast to well-researched areas such as legal discourse.  While the study of legal discourse remains valuable, creating a new corpus for it may only be necessary for highly specific sub-fields.

#### Compiling your own parallel corpus: Disadvantages

| Advantages                 | Disadvantages                                                                                                          |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Tailor-made design         | Related literature is scarse                                                                                           |
| Exploration of new domains | The corpus size will generally be small                                                                                |
|                            | Time-consuming task                                                                                                    |
|                            | Design problems can (partially or entirely) ruin your research, making a good design technique and procedure necessary |

### Setting the basis for corpus compilation

Here are listed some of the literature on the necessary procedures for building a parallel corpus:

- Frankenberg-Garcia (2009) -> Frankenberg-Garcia, A. (2009). Cross-language corpus query systems. Text, Speech and Technology (now Language Resources and Evaluation), 43(4), 371-391.
- Fantinuoli and Zanettin (2015) -> Fantinuoli, C., & Zanettin, F. (2015). Parallel Corpora. In Y. Gambier & L. van Doorslaer (Eds.), Handbook of Translation Studies (Vol. 5, pp. 97-104). John Benjamins Publishing Company.
- Serón Ordóñez (2015) -> Serón Ordóñez, M. (2015). La explotación de corpus paralelos en la investigación traductológica: recursos y aplicaciones. Onomázein, Número especial 2, 299-322.
- Zubillaga, Sanz and Uribarri (2015) -> Zubillaga, A., Sanz, I., & Uribarri, I. (2015). Developing comparable and parallel corpora for under-resourced languages: The case of Basque. In Proceedings of the 9th Workshop on Asian Language Resources (pp. 11-18).
- Molés-Cases (2016) -> Molés-Cases, T. (2016). Corpus-based translation studies: Research and applications. Íkala, Revista de Lenguaje y Cultura, 21(1), 11-30.

If possible, free and easily-operated software will be used, as opposed to frequent methods and tools used for corpus compilation: they "require considerable computational expertise, which most researchers in descriptive translation studies and translators probably do not possess" (Zanettin, 2012: 161).

{%
  include figure.html
  image="images/seminar-images/designing-parallel/alignment.png"
  caption=""
  width="400px"
%}

When selecting texts for alignment and corpus compilation, it's necessary to have both the source text and its translation. In this case, we will be using Sketch Engine, which supports specific file formats, including TMX, XLS, XLIFF, CSV, TVS, and XLSX.
Since the plan is to upload a TMX file to Sketch Engine, a translation memory is required. In general, a translation memory (TM) is essential for text alignment, whether using TMX or other formats, as it helps manage and structure bilingual content effectively. For text alignment purposes, using translation memory software—such as **Trados**—or an alignment tool like **LF Aligner** is recommended. If working with Trados, this process is straightforward. LF Aligner requires users to manually align source and target texts before creating a TM. Also, it primarily supports file formats such as DOC, TXT, RTF and DOCX.
In cases where the available text is in a different format—such as HTML, PDF, or database exports—it must first be converted to DOC. This conversion makes sure the text is compatible for alignment, allowing the creation of a bitext, which can then be uploaded to Sketch Engine.

### Some conditioning factors and text types

We are still in the process of selecting the texts for our corpus, and several key factors will influence our choices:

- Translation availability: To ensure a broad and diverse corpus, we should prioritize texts that have been widely translated. This will allow for a more extensive lexical range and a greater volume of words.
- Text length: The size of the texts plays a critical role in processing efficiency. A single text containing 10,000 words is much faster to process than ten texts of 1,000 words each. In the latter case, additional time is required for data entry, file saving, and format conversion.
- Digital vs. printed format: Digital texts are preferable to printed ones. If a text is available only in print (qui io metterei in printed form), it must first be converted into a digital format, adding an extra step to the process.
- File format considerations: Whether a text is in DOC, PDF, or HTML affects processing. If the text is in PDF or HTML, it must be converted to DOC before alignment, requiring an additional stage.
- Source and target identification: How easily can the source text be distinguished from the target text? Is this distinction relevant to the corpus's usability?
- Machine translation influence: Has the text been translated manually or by a machine? If machine-translated, does this affect its quality and suitability for the corpus?
- Domain and text type: Even when a topic seems appropriate, certain limitations may arise—such as a lack of available translations or restricted access to relevant texts due to geographical constraints. These factors may impact the compilation approach, possibly necessitating a shift to an alternative domain that remains valuable for research purposes.
The following sections will present various domains and fields for consideration, listed in no particular order.

#### Literary texts

| Advantages                                             | Disadvantages                                                             |
| ------------------------------------------------------ | ------------------------------------------------------------------------- |
| Usually easy to find                                   | If they are printed and not copyright-free, a lot of scanning is required |
| Generally long                                         |                                                                           |
| ST/TT are easy to identify                             |                                                                           |
| Machine translation is not involved on a regular basis |                                                                           |

#### Journalistic texts

Here are the advantages of using journalistic texts in parallel corpora:

- if they are web-based they are going to be typically .html, which is positive because it's a easily convertible format;
- usually the translation has been done by humans, so it's not a machine-based translation

The disadvantages are:

- Bitexts are not easy to find, except for some specific cases:

  - *Project Syndicate* (not free)
  - LENA (*Leading European Newspaper Alliance*): *El País*, *Le Figaro*, _Le Soir_, _Die Welt_, _Tribune de Genève_, _Tages Anzeiger_, _La Repubblica_, _Gazzetta_, _Wyborcza_
  - Airline in-flight magazines

| Advantages                                                                                                                  | Disadvantages                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| --------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| If web-based, texts are typically going to be in **HTML**, which is positive  because it's a **easily convertible format**. | **Bitexts are not easy to find**,  except for some specific cases: <ul><li>_Projetc Syndicate_ (not free)</li><li>LENA (_Leading European Newspaper Alliance_): _El País_, _Le Figaro_, _Le Soir_, _Die Welt_, _Tribune de Genève_, _Tages Anzeiger_, _La Repubblica_, _Gazzetta_, _Wyborcza_.</li></ul>  Airline in-flight magazines are great because it's easy to find them online and to identify what the target and the source texts are, although they cannot be labeled as "journalistic". |
| Usually **human-based translation**                                                                                         |


<!-- inoltre non se aggiungere il contributo della ricercatrice che lavora in questo campo (dott.ssa Gaia Aragrande) e quindi specificare all'inizio che questa pagina è il frutto del lavoro del prof. Leiva e di quelli che sono intervenuti durante il seminario?? -->

<!-- Contributo della dott.ssa Aragrande: -->

<!-- - I found that usually journalistic texts do not acknowledge the translator -->
<!-- - You can find repositories of multilingual journalism but you cannot align text because they don't really lend themselves to alignment. -->
<!-- - What you can do, though, is finding voluntary-based translation if semi-journalistic texts like Global Voices or similar platforms that provide bilingual and, usually, alignable texts. -->
<!-- - What I find the most effective with this type of texts is using  comparable corpora and investigating the same news item under different perspectives. This way you can pinpoint translation but they are not alignable. -->

<!-- (i primi due punti sono due svantaggi, il terzo e il quarto sono due vantaggi dati dall'uso di testi linguistici per la costruzione di corpora paralleli) -->

<!-- Poi il prof. Leiva ha aggiunto che si potrebbe utilizzare _Project Syndicate_: -->
<!-- The main issue is that it's not free (per la verità alcuni articoli sono accessibili liberamente) and you don't really know what the source text was. -->

<!-- Non dice nulla sull'ultimo punto segnalato dal punto interrogativo: "Medium-lenght texts" -->

#### Websites

| Advantages                                             | Disadvantages                                          |
| ------------------------------------------------------ | ------------------------------------------------------ |
| Ideal for **electronic corpora**                       | We don't know whether **machine translation** was used |
| If properly selected, these texts are usually **long** |                                                        |
| **ST/TT** are usually **easy to identify**             |                                                        |
| The format is usually **.html**                        |                                                        |

We need to define clear selection criteria, otherwise the amount of texts may become unmanageably large. Also, the texts would not be homogenous.

#### User manuals and online help files

| Advantages                                | Disadvantages                                                                           |
| ----------------------------------------- | --------------------------------------------------------------------------------------- |
| They are **everywhere**                   | **Machine translation/post-editing** might have been used                               |
| ST/TT are not difficult to identify       | If the manuals are paper-based, a lot of scanning is needed                             |
| This text type is perfect for terminology | If the manuals are online in .pdf format graphic normalization is necessary             |
|                                           | If the manuals are in .chm format, some technical knowledge to extract them is required |
|                                           | English is usually involved in ST                                                       |

<!-- Dice che mostrerà la "graphic normalization" più tardi (??) -->
<!-- Poi non capisco perché abbia messo "perfect for terminology" nelle cose a cui prestare attenzione piuttosto che nei vantaggi (??) -->

#### Tweets

| Advantages                     | Disadvantages                                                                       |
| ------------------------------ | ----------------------------------------------------------------------------------- |
| A _trending topic_ in research | It is difficult to find the same text written in two languages                      |
|                                | Extremely short texts: building an adequately large corpus is really time-consuming |

#### Subtitles

| Advantages                           | Disadvantages                                                      |
| ------------------------------------ | ------------------------------------------------------------------ |
| Easy to find                         | It requires some technical knowledge to extract/download subtitles |
| Usually long                         |                                                                    |
| ST/TT are typically easy to identify |                                                                    |

Interesting studies have been carried out in the last few years (e.g. Ortiz-Boix, 2016)

#### Press releases

| Advantages                                                                             | Disadvantages                                     |
| -------------------------------------------------------------------------------------- | ------------------------------------------------- |
| They are easy to find because the press section on websites are usually well organized | Possible use of manchine translation/post-editing |
| Very interesting text types                                                            | They are generally not too long                   |
| Format of texts: .html or .pdf                                                         | Too many repetitions                              |
| ST/TT are usually easy to identify                                                     |                                                   |

Some of these pros and cons could also be applied to abstracts of academic papers.

#### Translation memories

| Advantages                                                                             | Disadvantages                                                 |
| -------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| Aligned bitexts resemble translation memory files &rarr; no time needed for processing | Machine translation/post-editing may have been used           |
| Possibly vast amount of words                                                          | Companies/agencies and translator are not eager to share them |
| ST/TT can be easily identified                                                         |                                                               |

## Compiling a parallel corpus

<!-- PAUSA DA TAGLIARE [1:22:00 - 1:28:00] -->
Here are the four main stages of compiling a parallel corpus:

1. Selecting and finding your texts
2. Digitazion/graphic normalization and saving the texts
3. Aligning
4. Corpus compilation and management

### Selecting and finding your texts

<!-- 1:29:19 -->

When compiling your corpus, you need to answer these questions:

- What am I compiling my corpus for? E.g. unless specifically tagged, orthotypography cannot be studied in SketchEngine [è abbastanza chiaro il senso di questo esempio??]
- What are the limits of my corpus?
  - Text type/domain (as seen in previous section)?
  - Is the difference between ST and TT important?
  - Do I need texts from a specific location or can I work with texts from different geographical areas? E.g. Just Italy, or texts in Italian (e.g. Switzerland)?
  - Do I need texts from a specific timeframe or can I include all the material available regardless of the time they were made?
  - Just one author/ brand/company? Two of each to ease comparison? Everything?

<!-- [altra cosa: qui ho preferito scrivere tipo "you/your" ma ho paura di aver scritto "we/our" prima-> controlla e uniforma] -->

Please, also note:

- A questionable selection of sources for the corpus (being inaccurate, wrong or partial) can ruin days or weeks of your work
- Amount of resources: "It's not always possible to find translations of all texts, either beacuse of the text type -letters and email messages, for instance, are not usually translated- or because there are more translations in one direction (English to Chinese, for instance) then in another (Chinese to English)".
(Granger, 2010:5)

> **The good news is I can always make my corpus bigger or change it partially if necessary**

Some of the items needed at this point are:

- a good search strategy (also in Google) -> tips on how to do it later (questo l'ho aggiunto io)
- A file where to keep track of all the steps given
- A record of websites visited
- A logical and adequate coding strategy

{%
  include figure.html
  image="images/seminar-images/designing-parallel/passaggi corpus parallelo.png"
  caption=""
  width="400px"
%}

#### A case study: a parallel corpus of museum texts

<!-- 1:38:51 -->

In this section it will be taken into consideration a specific parallel aligned corpus:

- Gender (??): language of written museum texts
- Time: the corpus was compiled between 2006 and 2021, while the texts span from 1993 to 2021
- Place: electronic texts from museums and art centers from the United States (ST:English, TT:Spanish)
- Retrieved from appropriate websites
- Presumably human-translated (not MT), as translators are generally not indicated. (se vuoi rendere l’idea di “probabile ma non sicuro”)
- Almost 500 texts with 1.5 milion words for the English subcorpus and 1.7 milion words for the Spanish subcorpus

Search strategy

- Manual navigation of the websites of 77 museums (website navigation and search options within each site).
- **TL/TT as the starting point** (Toury, 1995). When building a parallel corpus, it makes sense to start from the target language, since that’s usually the trickiest part.

<!-- Search strategy (cont'd) io lo metterei qua anche -->

Now, we move on to the practical part of the work. Let's imagine  we want to build a corpus from English to Italian using texts from museums in the USA and more specifically the Met (Metropolitan Museum of Art). Please go to [the Met website](https://www.metmuseum.org) to follow the steps.

{%
  include figure.html
  image="images/seminar-images/designing-parallel/met homepage.png"
  caption=""
  width="600px"
%}


First of all, we need to check whether a language option is available.
*Depending on the country, translation may be clearly visible or hidden. As for the United States, for instance, translation is almost always hidden. Instead, Italian museums - such as the Vatican Museums - usually make the language menu easy to find on their websites.

{%
  include figure.html
  image="images/seminar-images/designing-parallel/musei vaticani.png"
  caption="On the upper right corner, you can clearly see the language option."
  width="600px"
%}

If this option is available, that’s great, as it makes it much easier to locate translated texts.

Going back to the Met, as there is no language option clearly visible, we need to use the search bar.

{%
  include figure.html
  image="images/seminar-images/designing-parallel/met searchbar.png"
  caption=""
  width="600px"
%}

Since we are looking for texts in Italian, we need to type "Italiano" in the search bar. If we search for "Italian" instead, the results will be related to Italy or Italian masters, but not to texts actually written in Italian.

{%
  include figure.html
  image="images/seminar-images/designing-parallel/met italiano.png"
  caption=""
  width="600px"
%}

<!-- Dato che poi dirà che questa strategia non funziona, è necessario riportarne tutto il processo?? -->

However, while browsing through the results you probably noticed that they were scarce and incomplete.
This is not only the case for the Met but also for other museum websites. Sometimes a website doesn't even have a search bar, so you need to navigate through it and try to come across some translations in other ways.

<!-- 1:44:38 -->

<!-- One effective way is:

1. Go to Google.com
2. In the bottom right corner of the page click on ""
3.
4.
1. copy paste: the website adress of the Metropolitan (https://www.metmuseum.org/) on Google search
 -->
