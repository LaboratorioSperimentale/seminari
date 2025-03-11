---
title: Tirocinanti
nav:
  order: 5
  tooltip: About our team
---

{%
  include button.html
  type="home-page"
  text="Laboratorio Sperimentale LILEC"
  link="https://site.unibo.it/laboratorio-sperimentale/"
%}
{%
  include button.html
  type="address"
  tooltip="Our location on Google Maps for easy navigation"
  text="Dove siamo"
  link="https://maps.app.goo.gl/uNU8UD6skxLo29V96"
%}
{%
  include button.html
  type="calendar"
  tooltip="Il calendario eventi del Laboratorio"
  text="Calendario"
  link="https://outlook.office365.com/calendar/published/61a2deb19726492a81d5356649f8e8c9@unibo.it/51e45a320469475d820af1d087016d154227240899176452804/calendar.html"
%}
{%
  include button.html
  type="email"
  text="Scrivici"
  link="lilec.lab@unibo.it"
%}

# {% include icon.html icon="fa-solid fa-users" %} GLI AUTORI DEL SITO

Le pagine di questo sito vengono arricchite grazie all'attività che i tirocinanti e le tirocinanti svolgono presso il Laboratorio Sperimentale.

Qui una lista per ringraziarl* tutt* &nbsp; <i class="fa-solid fa-heart fa-beat"></i> &nbsp; !


{% include section.html %}
## Anno accademico 2024/2025

{% include list.html data="members" component="portrait" filter="role == 'tirocinante'" %}