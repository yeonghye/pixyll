---
layout: page
title: Work 
permalink: work/
tags: work
---


<div class="home">
  {% if posts_count > 0 %}
    <div class="posts">
      <!-- {% for post in paginator.posts %} -->
      {% for post in site.tags[page.tag] %}
        <div class="post py3">
          <p class="post-meta">{{ post.date | date: site.date_format }}</p>
          <a href="{{ post.url | prepend: site.baseurl }}" class="post-link"><h3 class="h1 post-title">{{ post.title }}</h3></a>
          <span class="post-summary">
            {% if post.summary %}
              {{ post.summary }}
            {% else %}
              {{ post.excerpt }}
            {% endif %}
          </span>
        </div>
      {% endfor %}
    </div>

    {% include pagination.html %}
  {% else %}
    <h1 class='center'>{{ site.text.index.coming_soon }}</h1>
  {% endif %}
</div>