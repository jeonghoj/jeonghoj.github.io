---
layout: page
title: Category
permalink: /category
---
# Category

{% for category in site.categories %}
  {% capture category_name %}{{ category | first }}{% endcapture %}
<h2 class="c-archives__year" id="{{ category_name }}-ref">{{ category_name }}</h2>
<ul class="c-archives__list">
    {% for post in site.categories[category_name] %}
<li class="c-archives__item">
  <a class="post-title" href="{{ post.url | relative_url }}" title="{{ post.title }}">{{post.title | escape}}</a>
</li>
    {% endfor %}
</ul>
{% endfor %}
