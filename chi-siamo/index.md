---
title: Chi siamo
nav:
  order: 4
  tooltip: Email, address, and location
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


{% include section.html %}
## Referente Scientifico

<!-- {% include list.html data="members" component="portrait" filter="role == 'pi'" %} -->
{% include list.html data="members" component="portrait" filter="role == 'Lab Scientific Coordinator'" %}

{% include section.html %}
## Staff del Laboratorio
<!-- {% include list.html data="members" component="portrait" filter="role == 'pi'" %} -->
{% include list.html data="members" component="portrait" filter="role == 'lab-manager'" %}


{% include section.html %}
## {% include icon.html icon="fa-solid fa-users" %} Componenti Board del Laboratorio
{% include list.html data="members" component="portrait" filter="role == 'Lab Board Member'" %}


{% include section.html %}
## {% include icon.html icon="fa-solid fa-users" %} Membri Passati e in Visita
{% include list.html data="members" component="portrait" filter="role == 'old - Lab Manager' or role == 'old - Lab Board Member' or role == 'old - Visiting'" %}

