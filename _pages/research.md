---
title: "Research | SEU NetSI"
layout: textlay
excerpt: "Welcome to the SEU NetSI Group! We conducts research in the area of Internet of Things and Swarm Intelligence. Our goal is to provide theoretically sound analysis as well as build practically working systems."
sitemap: false
permalink: /research/
---

<div class="page-container">

# Research
<div style="margin-bottom: 45px;">
{% for item in site.data.research %}
<p style="display: inline; font-size:19px"><a href="#{{ item.id }}-title"><span class="label label-info">{{ item.topic }}</span></a></p>
{% endfor %}
</div>

<div class="research-list">
{% for item in site.data.research %}
<div class="panel panel-{{ item.color }}">
 <div class="panel-heading">
  <h3 class="panel-title">
   <span id="{{ item.id }}-title" class="title_placeholder">
    {{ item.topic }}
   </span>
  </h3>
 </div>
 
 <div class="panel-body">
  <div class="row clearfix">
   <div class="col-sm-6 ">
   <img class="img-responsive img-rounded" src="{{ site.url }}{{ site.baseurl }}/images/researchpic/{{ item.image }}" class="img-thumbnail" />
   </div>

   <div class="col-sm-6 clearfix research-card-intro">
   {{ item.introduction}}
   <div>
   {% assign has_related = 0 %}

   {% for publi in site.data.publist %}
   {% if item.id == publi.category %}
   {% assign has_related = 1 %}
   {% endif %}
   {% endfor %}

   {% if has_related == 1 %}
   <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ item.id }}-collapse" aria-expanded="false" aria-controls="collapseExample">
   See More
   </button>
   {% elsif item.video != "placeholder" %}
   <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ item.id }}-collapse" aria-expanded="false" aria-controls="collapseExample">
   See More
   </button>
   {% endif %}
   </div>
   </div>
  </div>

 <div class="collapse" id="{{ item.id }}-collapse">

 {% if has_related == 1 %}
 <h3>Related Research</h3>
 {% endif %}
 <ul class="list-group">
 {% for publi in site.data.publist %}
 {% if item.id == publi.category %}
 {% assign has_related = 1 %}
 <li class="list-group-item">{{ publi.authors }}, {% if publi.link.paper and publi.link.paper != "placeholder" %} <a href="{{ publi.link.paper}}" target="_blank"><span class="label label-success pull-right pub-label">Paper</span></a>{% endif %}{% if publi.link.slide and publi.link.slide != "placeholder" %} <a href="{{ publi.link.slide}}" target="_blank"><span class="label label-warning pull-right pub-label">Slide</span></a>{% endif %}{% if publi.link.video and publi.link.video != "placeholder" %} <a href="{{ publi.link.video}}" target="_blank"><span class="label label-danger pull-right pub-label">Video</span></a>{% endif %}{% if publi.link.code and publi.link.code != "placeholder" %} <a href="{{ publi.link.code}}" target="_blank"><span class="label label-primary pull-right pub-label">Code</span></a>{% endif %}<br />
  "{{ publi.title }}," <br />
  {{ publi.pubinfo }}{% if publi.bibtex and publi.bibtex != "placeholder" %} <a role="button" data-toggle="collapse" href="#{{ publi.id }}"><span class="label label-default pull-right pub-label">Bibtex</span></a>{% endif %}{% if publi.link.doi and publi.link.doi != "placeholder" %} <a href="{{ publi.link.doi}}" target="_blank"><span class="label label-info pull-right pub-label">DOI</span></a>{% endif %}</li>
  <div class="collapse well-sm" id="{{ publi.id }}" style="padding: 10px;">
  {{ publi.bibtex }}
  </div>
 {% endif %}
 {% endfor %}
 </ul>
 </div>
</div>

</div>
{% endfor %}
</div>

</div>
