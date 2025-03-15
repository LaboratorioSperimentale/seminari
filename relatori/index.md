---
title: Relatori
nav:
  order: 3
  tooltip: About our speakers
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

# {% include icon.html icon="fa-solid fa-users" %}Speakers

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

{% include section.html %}

{% include list.html data="members" component="portrait" filter="role == 'speaker'" %}
<!-- {% include list.html data="members" component="portrait" filter="role != 'pi'" %} -->

{% include section.html background="images/background.jpg" dark=true %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

<!-- {% include section.html %} -->

<!-- {% capture content %} -->

<!-- {% include figure.html image="images/photo.jpg" %} -->
<!-- {% include figure.html image="images/photo.jpg" %} -->
<!-- {% include figure.html image="images/photo.jpg" %} -->

<!-- {% endcapture %} -->

{% include grid.html style="square" content=content %}
