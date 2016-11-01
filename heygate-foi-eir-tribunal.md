---
layout: page
title: "Heygate FOI/EIR Tribunal"
---

<h2 id="categories">Blog posts about Heygate viability assessment FOI 
Tribunal</h2>
  <li>
    <ul>
    {% for post in site.categories.viability %}
       {% if post.url %} <li><a href="{{ post.url }}">{{ post.title }}</a></li>
       {% endif %}
    </ul>
  </li>
{% endfor %}
