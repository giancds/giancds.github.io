---
layout: default
title: Publicações
parent: About
nav_order: 1
---



{% comment %}
<!-- bibbase.org should work with following code unless you are hosting domain over https. -->

{% if page.bibtex %}
 {% if page.bibtex contains 'http' %}
  {% assign domain = '' %}
  {% else %}
  {% assign domain = site.url %}
 {% endif %}
 {% capture biburl %}{{ domain }}{{ page.bibtex }}{% endcapture %}
<script src="http://bibbase.org/show?bib={{ biburl | cgi_escape }}&amp;jsonp=1&amp;authorFirst=1"></script>
{% endif %}

{% endcomment %}

Note que as publicações mais recentes estão disponíveis apenas em Inglês.

<script src="https://bibbase.org/show?bib=https%3A%2F%2Fgiancds.github.io%2Ffiles%2Fmypubs.bib&jsonp=1"></script>