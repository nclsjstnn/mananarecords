---
layout: page
title: 
permalink: /blog/
---
<h3 style="text-align:center; margin-bottom:80px;">
  EL BLOG DEL MAÑANA
</h3>
{% for blog in site.blog reversed %}
  <div class="post">
    <header class="post-header">
      <h1 class="post-title">
        <a href="{{ blog.url }}">{{ blog.title }}</a></h1>
    </header>
    <article class="post-content">
      {{ blog.content }}
    </article>
  </div>
  {% include share.html %}
  <br>
{% endfor %}
