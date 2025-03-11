---
title: Seminari del Laboratorio
nav:
  order: 1
  tooltip: Software, datasets, and more
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

<!-- {% include tags.html tags="tool, resource, methodology" %} -->

<!-- {% include search-info.html %} -->
<!-- {% include search-box.html %} -->

{% include section.html size="card"%}
## Seminari 2025
{% include list.html component="card" style="small" data="projects" filter="group == '2025'" %}

{% include section.html size="card" %}
## Seminari 2024
{% include list.html component="card" style="small" data="projects" filter="group == '2024'" %}

{% include section.html size="card" %}
## Seminari 2021
{% include list.html component="card" style="small" data="projects" filter="group == '2021'" %}