---
layout: page
title: 
permalink: /blog/
---
<h3 style="text-align:center; margin-bottom:80px;">
  EL BLOG DEL MAÑANA
</h3>
{% for post in site.blog reversed %}
  <div class="post">
    <header class="post-header">
      <h1 class="post-title">
        <a href="{{ post.url }}">{{ post.title }}</a></h1>
    </header>
    <article class="post-content">
      {{ post.content | split:'<!--break-->' | first }}
      {% if post.content contains '<!--break-->' %}
      <p class="right">
        <a href="{{site.baseurl}}{{ post.url }}">Sigue Leyendo -></a>
      </p>
      {% endif %}
    </article>
  </div>
  <br>
{% endfor %}
{% include preview.html %}
