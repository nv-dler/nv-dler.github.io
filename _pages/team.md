---
title: "NVIDIA DLER - Team"
layout: gridlay
excerpt: "NVIDIA DLER Team members"
sitemap: false
permalink: /team/
---

# Group Members

Jump to [members](#members), [interns](#interns).

## Members
{% assign number_printed = 0 %}
{% for member in site.data.members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4> 
  {{ member.name }}
  </h4>
  <i>{{ member.info }}</i>
  <ul style="overflow: hidden;list-style-type: none;margin: 0;padding: 0;">
  {% if member.webpage %}
   <li> <a href="{{ member.webpage }}"> Webpage </a> </li> 
  {% endif %}
  {% if member.scholar %}
   <li> <a href="{{ member.scholar }}"> Google Scholar </a>  </li> 
  {% endif %}
  <!-- {% if member.webpage == 1 %}
  <br><a href="{{ member.webpage }}"> webpage </a>
  {% endif %} -->

  </ul>

  <ul style="overflow: hidden">
  

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 | markdownify}} </li>
  <li> {{ member.education2 | markdownify}} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}

  </ul>
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


## Interns

<ul style="overflow: hidden">

{% for member in site.data.interns %}

<li>
<strong>{{ member.name }}</strong>, {{ member.info }}, 
{% if member.webpage %}
  <a href="{{ member.webpage }}"> webpage </a>
{% endif %}
</li>

{% endfor %}

</ul>
