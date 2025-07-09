---
title: "新闻动态"
layout: textlay
excerpt: "Welcome to the SEU NetSI Group! We conducts research in the area of Internet of Things and Swarm Intelligence. Our goal is to provide theoretically sound analysis as well as build practically working systems."
sitemap: false
permalink: /allnews.html
slug: allnews
---

# 新闻动态

{% for article in site.data.news %}
<p><b>{{ article.date }}</b><br>
<span>{{ article.headline }}</span></p>
{% endfor %}
