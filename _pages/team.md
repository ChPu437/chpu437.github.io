---
title: "Team | SEU NetSI"
layout: gridlay
excerpt: "Welcome to the SEU NetSI Group! We conducts research in the area of Internet of Things and Swarm Intelligence. Our goal is to provide theoretically sound analysis as well as build practically working systems."
sitemap: false
permalink: /team/
---

<div class="page-container">

# Group Members

Jump to [staff](#staff), [PhD](#phd), [master](#master), [undergraduate](#undergraduate), [alumni](#alumni).

<div class="title_placeholder" id="staff"></div>
<h2>Staff</h2>
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row" style="margin-bottom: 0;">
{% endif %}

<div class="col-sm-9 clearfix">
  <img class="img-responsive img-rounded" src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" width="25%" style="float: left" />
  <h4><a href="{{member.link}}" target="_blank">{{ member.name }} {% if member.chinese != "placeholder" %} | {{member.chinese}}{% endif %}</a></h4>
  <i>{{ member.info }}
  <br>Email: <{{ member.email }}>
  <br>Website: <a href="{{member.link}}" target="_blank">{{ member.link }}</a>
  <br>Room: {{ member.office }}</i>

  {% if member.id != "placeholder" %}
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ member.id }}" aria-expanded="false" aria-controls="collapseExample">
    See More
  </button>
  {% endif %}
  <br>
  <div class="collapse" id="{{ member.id }}">
  <h3>Biography</h3>
  {{ member.biography }}
  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<div class="title_placeholder" id="phd"></div>
<h2>PhD</h2>
{% assign number_printed = 0 %}
{% for member in site.data.phd_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img class="img-responsive img-rounded" src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" width="25%" style="float: left" />
  <h4><a href="{{member.link}}" target="_blank">{{ member.name }} {% if member.id != "placeholder" %} | {{member.chinese}}{% endif %}</a></h4>
  <i>{{ member.info }} 
  <br>Email: <{{ member.email }}></i>
  {% if member.id != "placeholder" %}
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ member.id }}" aria-expanded="false" aria-controls="collapseExample">
    See More
  </button>
  {% endif %}

  <div class="collapse" id="{{ member.id }}">

  <h3>Biography</h3>
  <div>
  <ul>
  {% for item in member.education %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  <h3>Interests</h3>
  <div>
  <ul>
  {% for item in member.interest %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  <h3>Correspondence</h3>
  <div>
  <ul>
  {% for item in member.correspondence %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<div class="title_placeholder" id="master"></div>
<h2>Master</h2>
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img class="img-responsive img-rounded" src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" width="25%" style="float: left" />
  <h4><a href="{{member.link}}" target="_blank">{{ member.name }} {% if member.id != "placeholder" %} | {{member.chinese}}{% endif %}</a></h4>
  <i>{{ member.info }} 
  <br>Email: <{{ member.email }}></i>
  {% if member.id != "placeholder" %}
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ member.id }}" aria-expanded="false" aria-controls="collapseExample">
    See More
  </button>
  {% endif %}

  <div class="collapse" id="{{ member.id }}">

  <h3>Biography</h3>
  <div>
  <ul>
  {% for item in member.education %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  <h3>Interests</h3>
  <div>
  <ul>
  {% for item in member.interest %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  <h3>Correspondence</h3>
  <div>
  <ul>
  {% for item in member.correspondence %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<div class="title_placeholder" id="undergraduate"></div>
<h2>Undergraduate</h2>
{% assign number_printed = 0 %}
{% for member in site.data.undergraduate_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img class="img-responsive img-rounded" src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" width="25%" style="float: left" />
  <h4><a href="{{member.link}}" target="_blank">{{ member.name }} {% if member.id != "placeholder" %} | {{member.chinese}}{% endif %}</a></h4>
  <i>{{ member.info }} 
  <br>Email: <{{ member.email }}></i>
  {% if member.id != "placeholder" %}
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ member.id }}" aria-expanded="false" aria-controls="collapseExample">
    See More
  </button>
  {% endif %}

  <div class="collapse" id="{{ member.id }}">

  <h3>Biography</h3>
  <div>
  <ul>
  {% for item in member.education %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  <h3>Interests</h3>
  <div>
  <ul>
  {% for item in member.interest %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  <h3>Correspondence</h3>
  <div>
  <ul>
  {% for item in member.correspondence %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<div class="title_placeholder" id="alumni"></div>
<h2>Alumni</h2>

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img class="img-responsive img-rounded" src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" width="25%" style="float: left" />
  <h4>{{ member.name }} | {{member.chinese}}</h4>
  <i>{{ member.info }}</i>
  {% if member.id != "placeholder" %}
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ member.id }}" aria-expanded="false" aria-controls="collapseExample">
    See More
  </button>
  {% endif %}

  <div class="collapse" id="{{ member.id }}">

  <h3>Biography</h3>
  <div>
  <ul>
  {% for item in member.education %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  <h3>Thesis</h3>
  <div>
  <ul>
  {% for item in member.thesis %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  <h3>Correspondence</h3>
  <div>
  <ul>
  {% for item in member.correspondence %}
  <li>{{ item }}</li>
  {% endfor %}  
  </ul>
  </div>

  </div>  
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}



## Other Alumni
{% for member in site.data.alumni_others %}

<div class="row" style="margin-bottom: 5px;">
<div class="col-sm-3">
{{ member.name }} \| {{ member.chinese }}
</div>
<div class="col-sm-8" style="padding: 0px;">
{{ member.attr }}
</div>
<div class="col-sm-1">
{% if member.id != "placeholder" %}
<button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ member.id }}" aria-expanded="false" aria-controls="collapseExample">
  See More
</button>
{% endif %}
</div>
<div class="col-sm-12">
<div class="collapse well" id="{{ member.id }}">
{{ member.biography }}
</div>
</div>
</div>
{% endfor %}

## From NetSI, to the world!
<div class="row">
{% for pic in site.data.pics.memberlogo %}
<div class="col-sm-2 col-xs-4 clearfix">
<a href="{{ pic.link }}" target="_blank">
<img class="img-responsive img-rounded" src="{{ site.url }}{{ site.baseurl }}/images/teampic/memberlogo/{{ pic.image }}" width="100%" style="float: left" />
</a>
</div>
{% endfor %}
</div>

</div>
