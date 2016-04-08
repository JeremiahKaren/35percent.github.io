---
layout: page
title: Blog Archive
---

<h2>Archives</h2>
<ul>
  {% for post in site.posts %}

    {% unless post.next %}
      <h3>{{ post.date | date: '%Y' }}</h3>
    {% else %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
      {% if year != nyear %}
        <h3>{{ post.date | date: '%Y' }}</h3>
      {% endif %}
    {% endunless %}

    <li>{{ post.date | date:"%b" }} <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

<h2>Categories</h2>
<ul>
{% for category in site.categories %}
  <li><h3>{{ category | first }}">{{ category | first }}</h3>
    <ul>
    {% for posts in category %}
      {% for post in posts %}
       {% if post.url %} 
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
       {% endif %}
      {% endfor %}
    {% endfor %}
    </ul>
  </li>
{% endfor %}
