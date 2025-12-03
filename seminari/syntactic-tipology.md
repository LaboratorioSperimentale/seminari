---
layout: seminar
title: "Doing corpus-based syntactic typology with spoken language corpora"
author: leonardozannoli
speaker: geoffrey haig
---
# Doing corpus-based syntactic typology with spoken language corpora

In this seminar Geoffrey Haig talks about corpus based typology as a sub discipline of linguistics. Moreover, he talks about two initiatives in corpus based typology, the Multi-CAST and the WOWA. Lastly, he goes through a couple of case studies that have been done with these initiatives, explaining some issues of annotation, what happens when someone annotated and what kind of ressearch question you can adress with this kind of data.

## Language typology

The language typology is concerned with the extent of similarities and the limits of variation across the human language. Another important issue is how different features of human language are distributed in space and time. At this point, laguage typology becomes a discipline that's related to ancient human history. Language typology approaches these questions through the systematic investigation of a maximally broad sample of attested human languages. So anything is a valid source of data for language typology.

## Domains of Investigation

It might be interested in phonological systems, tone, syllable structure, vowel inventories and so on. 
It might be interested in lexical semantics, so colour term systems, kinship systems, terms for spatial reference.
It might be interested in practices of verbal interaction.
Finally, it might be interested in morphosyntax, the grammar in the narrower sense of the world. 

## Methods: Grammar-based Typology 

Traditionally, the researchers take grammars as descriptions of the structure of languages, they investigate them and they extract certain features out of the grammar. That might be, for example, word order, the tense system, the system of tones. So, on this view a language is represented by its grammar. The grammar-based typology has traditionally established classes, based on the values that are assigned to languages for a pre-defined set of features, as the order of objects and verbs or the order of adpositions.

## Methods: Corpus-based or token-based typology

On this view a language would be conceived as a population of utterances, so that's the primary object of comparison. The researcher takes what he thinks is a reasonable population of utterances. In theory, they wouldn't even need a grammar. 
The Corpus-based typology takes into account the language-internal variability of primary linguistic data ("performance"), and derives probabilistic tendencies from the data, rather than a set of discrete classes. Moreover, we have a focus on variation and measures of frequency, that means adopting/adapting methodologies developed in corpus linguistics, and in variation socio-linguistics. This method is intended to complement rather than replace grammar-based typology. 

## Problems of the Corpus-based typology

The first problem is which languages (or doculects) you're going to look at. Basically, here we need widely distributed, genetically distributed and genetically distributed languages to be compared. That means that we are going to have to handle spoken language.
Then, we have the issue of how much data do we need to represent one language and from how many speakers. Basically, the nature and dimensions of our corpus need to match the nature of our research questions. The most important thing is that whatever data we compile, remember we should keep it reusable, accountable, accesible and sustainable.

## Types of data

When we are gathering data, the first question is how much content control do we want. The maximum degree of content control is a translation. The alternative is to let people speak or write whatever they want, that would be content independent. And in the middle there are the so-called parallax corpora, that are based on non-verbal stimulus.
The second thing is the medium. Are we going to go written or spoken? And if we have spoken data are we going to have monologues or conversations?

### Multi-CAST (Multilingual Corpus of Annotated Spoken Tests)

In this particular corpus we have six levels of annotation. We start with a transcription of actual recording that are segmented into utterance units and time-aligned with the sound file. Than there's a second layer of morpheme for morpheme glossing. Finally, there'll be an idiomatic translation in English. This are the three principal tiers that when we take a text into multicultural corpus is pretty well what we assumed we'll already have.
And then we add three tiers to it. The first one is the so-called GRAID (Grammatical Relations and Animacy in Discourse). The second is Refind (Referent indexing), that assigns a unique numerical index to each referent. And the third one is ISNRef that is only used for newly introduced referents.

EXAMPLE: Northern Kurdish 

### Annotations with GRAID: Form classes of referring expressions 

In this kind of annotations we distinguish three (main) form classes of NP (noun phrase). The first one is a 0, so there is a referential expression that is recoverable from context, but there's no overt noun phrase which expresses it. The second one is a pronoun (pro), and finally we can have a full noun phrase with a lexical head. Subsequently, this main classes are combined with an indicator of person and animacy (first person, second person, H, which is third person human). 
When we annotate the form, we also need to say something about what that item is doing in the clause. So it has some sort of syntactic function.

TAGS FOR FUNCTION

### WOWA: Word Order in Western Asia

WOWA is a new project that has a different aim to Multi-CAST but there are also a number of similitaries. First of of all, we are working with content-independent, spoken, monological data. Secondly, we have unrestricted accessibility of all data. And finally, we have a similar size of individual corpora.
On the other side we have also some difference between this two systems. The first is that WOWA is not typology on a global scale and the choice of documents is aereally restricted. In WOWA the focus is on the word order typology rather than discourse and grammar. But the fundamental difference is that in WOWA we don't have a comprehensive annotation. The focus here is on certain tokens of interest in the text and we a codification of them, while the rest is left uncoded. And that means that is used a spreadsheet format, and not ELAN. 
The big advantage is that data can be annotated much more quickly, the analysis is simpler, and there is less pre-processing because it's in a table format. 
On the other side we have some disadvantages. For example, the data in WOWA are less versatile and that means that there will be more restrictions on future re-usability. The other disadvantage is that the categories are predefined more than in Multi-CAST, rather than building up categories from the data.

### Work flow with WOWA

Firstly, we select a doculect and we go through a rough segmentation into utterance units. Secondly, we enter them into spread-sheet, so each utterance unit goes into a single cell in a spread-sheet. Usually we apply a translation and then we identify all the non-subject constituents in the text, and we enter them into spread-sheet: these are the tokens. Finally, we code each for a variety of features and we can analyze them in R. 

### Summary

If you want to compare usage rather than grammars across typologically diverse languages, you have to do a huge laborious task of collection, transcription and translation of the material from a typologically diverse range of languages. Moreover, you have to annotate them in a way that comparison across different languages is meaningful and practicable. This work is only worth if it's done in such a way that your labour is preserved for future research, even though you have no idea what future researchers will be interested in.

### Recommendations by Geoffrey Haig

Firstly, it's important to pick a research question that initially guide your practice, without imposing too many restrictions on future output. Secondly, you need to work bottom-up and incrementally and above all work collaboratively with socio-linguists, corpus linguists, statisticians and modellers, and so on. Another important thing is that annotation is always work-in-progress, you never finish. Finally, is fundamental to keep it simple.

FINE