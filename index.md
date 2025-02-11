---
---

# LaboratorioSperimentale's Website

Lo scopo del Laboratorio Sperimentale è assistere i membri del Dipartimento LILEC nelle loro ricerche e di promuovere la creazione di risorse digitali presso il Dipartimento. Il Laboratorio mette a disposizione dei ricercatori gli strumenti necessari per una serie di finalità, tra cui:

- la raccolta, l’elaborazione e l’analisi di corpora di testi orali, scritti e digitali;
- lo studio empirico-sperimentale del linguaggio e del testo/discorso in tutte le sue manifestazioni;
- l’edizione critica digitale di testi manoscritti e la marcatura di testi;
- la creazione di banche dati per lo studio sincronico e diacronico di testi;
- la modellizzazione e la visualizzazione di dati linguistici e bibliografici;
- l’estrazione di dati dal web e da corpora paralleli di traduzione per l’elaborazione di dizionari plurilingui specialistici.

Il Laboratorio inoltre organizza eventi formativi che hanno l’obiettivo di dotare i membri del LILEC di un know-how (inter)disciplinare teorico-pratico negli ambiti di propria competenza, promuovendo una riflessione metodologica ampia sulla diversità dei dati linguistici e testuali.

{% include section.html %}

## Highlights

{% capture text %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

{%
  include button.html
  link="research"
  text="See our publications"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="research"
  title="Our Research"
  text=text
%}

{% capture text %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

{%
  include button.html
  link="projects"
  text="Browse our projects"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="projects"
  title="Our Projects"
  flip=true
  style="bare"
  text=text
%}

{% capture text %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

{%
  include button.html
  link="team"
  text="Meet our team"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="team"
  title="Our Team"
  text=text
%}
