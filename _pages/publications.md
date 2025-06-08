---
title: "Publication | SEU NetSI"
layout: gridlay
excerpt: "Welcome to the SEU NetSI Group! We conducts research in the area of Internet of Things and Swarm Intelligence. Our goal is to provide theoretically sound analysis as well as build practically working systems."
sitemap: false
permalink: /publication/
---

<div class="page-container">

# Publication
## Group Highlights

For a full list of publications and patents can be found at [homepage](https://fengshan.seu-netsi.net/#publications) or go to [Google Scholar](https://scholar.google.com/citations?user=7N_fRVwAAAAJ).

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight and publi.highlight.attr and publi.highlight.attr == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img class="img-responsive img-rounded" src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.highlight.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.highlight.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p style="font-weight: bold"><a href="{{ publi.highlight.link }}" target="_blank">{{ publi.highlight.source }}</a>

{% if publi.link.paper != "placeholder" %} <a href="{{ publi.link.paper}}" target="_blank"><span class="label label-success pull-right pub-label">Paper</span></a>{% endif %}
{% if publi.link.slide != "placeholder" %} <a href="{{ publi.link.slide}}" target="_blank"><span class="label label-warning pull-right pub-label">Slide</span></a>{% endif %}
{% if publi.link.video != "placeholder" %} <a href="{{ publi.link.video}}" target="_blank"><span class="label label-danger pull-right pub-label">Video</span></a>{% endif %}
{% if publi.link.code != "placeholder" %} <a href="{{ publi.link.code}}" target="_blank"><span class="label label-primary pull-right pub-label">Code</span></a>{% endif %}
</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Full List of Publications
{% assign thisyear = 0 %}

{% for publi in site.data.publist %}
  {% if thisyear != publi.year%}
  <h3>{{ publi.year }}</h3>
  {% endif %}
  {% assign thisyear = publi.year%}

  <div class="well-sm">
  {{ publi.authors }}, {% if publi.link.paper and publi.link.paper != "placeholder" %} <a href="{{ publi.link.paper}}" target="_blank"><span class="label label-success pull-right pub-label">Paper</span></a>{% endif %}{% if publi.link.slide and publi.link.slide != "placeholder" %} <a href="{{ publi.link.slide}}" target="_blank"><span class="label label-warning pull-right pub-label">Slide</span></a>{% endif %}{% if publi.link.video and publi.link.video != "placeholder" %} <a href="{{ publi.link.video}}" target="_blank"><span class="label label-danger pull-right pub-label">Video</span></a>{% endif %}{% if publi.link.code and publi.link.code != "placeholder" %} <a href="{{ publi.link.code}}" target="_blank"><span class="label label-primary pull-right pub-label">Code</span></a>{% endif %}<br />
  "{{ publi.title }}," <br />
  {{ publi.pubinfo }}{% if publi.bibtex and publi.bibtex != "placeholder" %} <a role="button" data-toggle="collapse" href="#{{ publi.id }}"><span class="label label-default pull-right pub-label">Bibtex</span></a>{% endif %}{% if publi.link.doi and publi.link.doi != "placeholder" %} <a href="{{ publi.link.doi}}" target="_blank"><span class="label label-info pull-right pub-label">DOI</span></a>{% endif %}

  <div class="collapse well-sm" id="{{ publi.id }}" style="background-color: #fff">
  {{ publi.bibtex }}
  </div>
  </div>
{% endfor %}
</div>
