---
layout: page
title: Jack Collins
tagline: Aspiring Ruby on Rails Developer
---
{% include JB/setup %}
    
## Recent Posts


<ul>
  {% for post in site.posts %}
    <li><a style="font-size:30px" href="{{ post.url }}">{{ post.title }}     </a><span style="font-size:16px">{{ post.date | date_to_string }}</span>
      {% if post.content contains '<!--more-->' %}
        {{ post.content | split:'<!--more-->' | first }}
      {% endif %}
    </li>
  {% endfor %}
</ul>
<!--
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
-->



