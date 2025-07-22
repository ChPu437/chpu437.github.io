---
title: "照片展示"
layout: piclay
excerpt: "欢迎加入东南大学计算机科学与工程拔尖学生培养基地，祝您在此度过四年愉快的大学生活。"
permalink: /gallery/
slug: gallery
---

<div class="page-container">

# 照片展示
<p>点击查看详情 <a href="#我们的活动">我们的活动</a>, <a href="#东南大学">东南大学</a>.</p>

<div class="title_placeholder" id="我们的活动"></div>
<h2>我们的活动</h2>
记录生活，记录我们。<br>
{% assign number_printed = 0 %}

{% for pic in site.data.pics.ourgroup %}
{% assign even_odd = number_printed | modulo: 2 %}



{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix gallery-pic text-warning">
<img src="{{ site.baseurl }}/images/gallery/{{ pic.image }}" class="img-responsive img-rounded" width="100%" style="float: left" />

{{ pic.intro }} <br><span class="label label-default">{{ pic.date }}</span>
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

<div class="title_placeholder" id="东南大学"></div>
<h2>东南大学</h2>
图1-3拍摄于东南大学四牌楼校区（始于1902年）， <br>图4-9拍摄于东南大学九龙湖校区（始于2006）。<br>

{% assign number_printed = 0 %}
{% assign even_odd = 0 %}
{% for pic in site.data.pics.seuview %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-4 clearfix gallery-pic text-success">
<img src="{{ site.baseurl }}/images/gallery/{{ pic.image }}" class="img-responsive img-rounded"  width="100%" style="float: left" /> <!-- 该链接需要修改 -->

</div>

{% assign number_printed = number_printed | plus: 1 %}
{% assign even_odd = number_printed | modulo: 3 %}
{% if even_odd == 0 %}
</div>
{% endif %}

{% endfor %}

</div>
