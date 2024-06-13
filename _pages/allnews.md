---
title: "News"
layout: textlay
excerpt: "NVIDIA Deep Learning Efficiency Research"
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<b>{{ article.date }}</b> <br/> {{ article.headline | markdownify}} <br/> <br/>
{% endfor %}
