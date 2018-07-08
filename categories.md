---
layout: page
title: 分类
---
{% for category in site.categories %}[{{ category | first }}](#{{ category | first }})  {% endfor %}

{% for category in site.categories %}
<h2><a name="{{ category | first }}">{{ category | first }}</a></h2>

{% for post in category.last %}
* {{ post.date | date: '%y-%m-%d' }} &raquo; [{{ post.title }}]({{ post.url }} "{{ post.title }}"){:.archive-item-link}

{% endfor %}

{% endfor %}
