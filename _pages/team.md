---
title: "基地成员"
layout: gridlay
excerpt: "Welcome to the SEU NetSI Group! We conducts research in the area of Internet of Things and Swarm Intelligence. Our goal is to provide theoretically sound analysis as well as build practically working systems."
sitemap: false
permalink: /team/
---

<div class="page-container">

# 基地成员

跳转至 [教师](#staff), [2022级学生](#2022), [2023级学生](#2023), [2024级学生](#2024).

<div class="title_placeholder" id="staff"></div>
<h2>教师</h2>
{% assign number_printed = 0 %}
{% for member in site.data.staff %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row" style="margin-bottom: 0;">
{% endif %}

<div class="col-sm-9 clearfix">
  <img class="img-responsive img-rounded" src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" width="25%" style="float: left; aspect-ratio: 1/1; object-fit: cover;" />
  <h4><a href="{{member.link}}" target="_blank">{{ member.name }}</a></h4>
  {{ member.info }}
  <i><br>电子邮箱: <{{ member.email }}>
  <br>个人主页: <a href="{{member.link}}" target="_blank">{{ member.link }}</a>
  <br>负责内容: {{ member.role }}</i>

  {% if member.id != "placeholder" %}
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#{{ member.id }}" aria-expanded="false" aria-controls="collapseExample">
    了解更多
  </button>
  {% endif %}
  <br>
  <div class="collapse" id="{{ member.id }}">
  <h3>简介</h3>
  <div>
  <ul>
  {% for item in member.biography %}
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

<div class="title_placeholder" id="2022"></div>
<h2>2022级学生</h2>
{% assign number_printed = 0 %}
{% for member in site.data.students2022 %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img class="img-responsive img-rounded" src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" width="25%" style="float: left; aspect-ratio: 1/1; object-fit: cover;" />
  <h4><a href="{{member.link}}" target="_blank">{{ member.name }} </a></h4>
  <i>年级: {{ member.grade }}
  <br>兴趣: {{ member.brief_interest }}</i>
  {% if member.id != "placeholder" %}
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#2022-{{ member.id }}" aria-expanded="false" aria-controls="collapseExample">
    了解更多
  </button>
  {% endif %}
  <br>
  <div class="collapse" id="2022-{{ member.id }}" style="clear: both;">
  <h3>简介</h3>
  <div>
  <ul>
  {% for item in member.biography %}
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


<div class="title_placeholder" id="2023"></div>
<h2>2023级学生</h2>
{% assign number_printed = 0 %}
{% for member in site.data.students2023 %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img class="img-responsive img-rounded" src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" width="25%" style="float: left; aspect-ratio: 1/1; object-fit: cover;" />
  <h4><a href="{{member.link}}" target="_blank">{{ member.name }} </a></h4>
  <i>年级: {{ member.grade }}
  <br>兴趣: {{ member.brief_interest }}</i>
  {% if member.id != "placeholder" %}
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#2023-{{ member.id }}" aria-expanded="false" aria-controls="collapseExample">
    了解更多
  </button>
  {% endif %}
  <br>
  <div class="collapse" id="2023-{{ member.id }}" style="clear: both;">
  <h3>简介</h3>
  <div>
  <ul>
  {% for item in member.biography %}
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


<div class="title_placeholder" id="2024"></div>
<h2>2024级学生</h2>
{% assign number_printed = 0 %}
{% for member in site.data.students2024 %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img class="img-responsive img-rounded" src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" width="25%" style="float: left; aspect-ratio: 1/1; object-fit: cover;" />
  <h4><a href="{{member.link}}" target="_blank">{{ member.name }} </a></h4>
   {% if member.id != "placeholder" %}
  <i>年级: {{ member.grade }}
  <br>兴趣: {{ member.brief_interest }}</i>
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#2024-{{ member.id }}" aria-expanded="false" aria-controls="collapseExample">
    了解更多
  </button>
  {% endif %}
  <br>
  <div class="collapse" id="2024-{{ member.id }}" style="clear: both;">
  <h3>简介</h3>
  <div>
  <ul>
  {% for item in member.biography %}
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




</div>
