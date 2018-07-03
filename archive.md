---
layout: page
title: /存档
permalink: /archive
---

<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y_%m_%d" }}</time>
    <a href="{{ post.url }}"> {{ post.title }}</a>
    </li>
{% endfor %}
</ul>
