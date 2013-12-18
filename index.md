---
layout: page
title: Jack Collins
tagline: Aspiring Ruby on Rails Developer
---
{% include JB/setup %}
    
## Recent Posts

{% for post in site.posts %}
  <div class="post-preview">
    <div class="post-entry">
      <div class="post-head">
        <a class="post-title" href="{{ post.url }}">{{ post.title }}     </a><span class="post-date">{{ post.date | date_to_string }}</span>
      </div>
      <div class="post-summary">
        {% if post.content contains '<!--more-->' %}
          {{ post.content | split:'<!--more-->' | first }}
        {% endif %}
      </div>
    </div>
  </div>
{% endfor %}



