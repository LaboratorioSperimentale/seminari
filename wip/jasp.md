---
layout: seminar
title: "Analisi dei dati linguistici con R e Jasp: dalla sintesi dei dati alla statistica inferenziale"
author: esmeraldadivenere
---

* Table of Contents
{:toc}
{:.no_toc}

## Analisi dei dati linguistici con Jasp

> [Analisi dei dati linguistici con R e JASP dalla sintesi dei dati alla statistica inferenziale.mp4](https://liveunibo.sharepoint.com/:v:/s/Labsperimentaleprova873/EUy_5AgykQlPkkiCgUIEznkBSFPAX7H67Lx8KrVijHTMIQ?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=RDznAe)
> Durata intera: 04:00:00. Porzione di video su Jasp: 03:08:06-03:35:08.
> Conferenza del 21/10/2024. Speaker: Dott. Flavio Pisciotta.
> Ulteriori materiali: https://github.com/LaboratorioSperimentale/Formazione-seminario_R_Jasp


## Introduzione: Cos'è Jasp?

[JASP](https://jasp-stats.org/) un programma open source gratuito, supportato dall’università di Amsterdam.

JASP offre procedure di analisi standard sia nella forma classica che in quella bayesiana. Presenta un layout del foglio di calcolo e un'interfaccia intuitiva drag-and-drop, una divulgazione progressiva per una maggiore comprensione e un output annotato per comunicare i risultati.


## Caricare Dataset su Jasp

Per caricare un dataset su Jasp: cliccare le tre linee > Open > Computer – e da lì scegliere il proprio dataset.

Per effettuare modifiche, si può cliccare su “Edit Data”.

Per assegnare un tipo diverso a una variabile, si clicca su “Analyses”.



## Sintesi

A partire da *Descriptives > Descriptive statistics > Statistics*, è possibile effettuare diversi tipi di sintesi, come segue.

Media: *Descriptives > Descriptive statistics > Statistics > Central Tendency > Mode*

Mediana: *Descriptives > Descriptive statistics > Statistics > Central Tendency > Median*

Deviazione standard: *Descriptives > Descriptive statistics > Statistics > Dispersion > Std. Deviation*

Range interquartile: *Descriptives > Descriptive statistics > Statistics > Dispersion > IQR*



## Rappresentazione

Per la rappresentazione delle **variabili nominali**, è utile la sezione Frequencies > Contingency tables. I grafici per le variabili nominali non sono disponibili quando si ha un incrocio di due variabili, ma solo valore per valore delle celle.

Per la rappresentazione delle **variabili ratio**, esistono diversi tipi di grafici, in base alla tipologia di variabili.

Grafico a barre (una variabile): *Descriptives > Flexplot (inserire solo variabile dipendente nominale)* oppure *Descriptives > Descriptive statistics > Basic Plots > Distribution Plots*

Grafico a torta: *Descriptives > Descriptive statistics > Basic Plots > Pie charts*

Istogramma: *Descriptives > Flexplot (inserire solo variabile dipendente ratio)* oppure *Descriptives > Descriptive statistics > Basic Plots > Distribution Plots*

Boxplot: *Descriptives > Descriptive statistics > Customizable Plots > Boxplots*

*inserire immagini???*

## Test

La sezione T-Test permette di scegliere fra diversi tipi di T-Test (Classical / Bayesan), che si usano per confrontare le medie di più gruppi, ma esistono diversi modi per effettuare test.

Test di Shapiro-Wilk: *T-Tests > One Sample T-Test > Assumption checks > Normality*

Chi square for Independence: *Frequencies > Contingency tables > Statistics > χ2*

Test esatto di Fisher: *Frequencies > Contingency tables > Statistics > Odds Ratio (2x2 only)*

One sample t-test: *T-Tests > One Sample T-Test > Tests > Student* (Lo Student Test può essere effettuato anche come *paired* e *Indipendent*)

One sample Wilcoxon signed-rank test: *T-Tests > One Sample T-Test > Tests > Wilcoxon signed-rank* (Piò essere effettuato anche come *Paired*, per il confronto di misurazioni ripetute).

Mann-Whitney U test: *T-Tests > Independent Sample T-Test > Tests > Mann-Whitney*

One way ANOVA: *ANOVA*

Kruskal-Wallis test: *ANOVA > Nonparametrics*

Coefficiente di correlazione di Pearson (r): *Regression > Correlation > Sample Correlation Coefficients > Pearson’s r e Additional options > Display pairwise*

Coefficiente di correlazione di Spearman (rho): *Regression > Correlation > Sample Correlation Coefficients > Spearman’s rho e Additional options > Display pairwise*

Coefficiente di correlazione di Kendall (tau): *Regression > Correlation > Sample Correlation Coefficients > Kendall’s tau e Additional options > Display pairwise*