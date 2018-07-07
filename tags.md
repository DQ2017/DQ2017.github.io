---
layout: page
title: 标签
permalink: /tag/
---
{% for tag in site.tags %}<a href="#{{ tag | first }}">{{ tag | first }}<sup>({{ tag[1].size }})</sup></a> {% endfor %}

{% for tag in site.tags %}
<h2><a name="{{ tag | first }}"># {{ tag | first }}</a></h2>

{% for post in tag.last %}
* {{ post.date | date: '%m-%d' }} &raquo; [{{ post.title }}]({{ post.url }} "{{ post.title }}"){:.archive-item-link}
{% endfor %}
{% endfor %}
