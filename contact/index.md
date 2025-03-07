---
title: Board
nav:
  order: 4
  tooltip: Email, address, and location
---
{%
  include button.html
  type="email"
  text="lilec.lab@unibo.it"
  link="lilec.lab@unibo.it"
%}
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
  text="Studio 76, Dipartimento LILEC"
  link="https://maps.app.goo.gl/uNU8UD6skxLo29V96"
%}

{% capture col1 %}

{% include section.html %}
# {% include icon.html icon="fa-solid fa-users" %} Referente Scientifico

<!-- {% include list.html data="members" component="portrait" filter="role == 'pi'" %} -->
{% include list.html data="members" component="portrait" filter="role == 'Lab Scientific Coordinator'" %}
{% endcapture %}

{% capture col2 %}

{% include section.html %}
# {% include icon.html icon="fa-solid fa-users" %} Lab Staff
<!-- {% include list.html data="members" component="portrait" filter="role == 'pi'" %} -->
{% include list.html data="members" component="portrait" filter="role == 'lab-manager'" %}
{% endcapture %}

{% include cols.html col1=col1 col2=col2 %}



{% include section.html %}
# {% include icon.html icon="fa-solid fa-users" %} Board Members
<!-- {% include list.html data="members" component="portrait" filter="role == 'pi'" %} -->
{% include list.html data="members" component="portrait" filter="role == 'Lab Board Member'" %}

{% include section.html %}
# {% include icon.html icon="fa-solid fa-users" %} Membri Passati e in visita
<!-- {% include list.html data="members" component="portrait" filter="role == 'pi'" %} -->
{% include list.html data="members" component="portrait" filter="role == 'Lab Board Member'" %}