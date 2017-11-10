<!-- 
---
layout: default
---
{% assign posts_count = paginator.posts | size %}


<div class="home">
  {% if posts_count > 0 %}
    <div class="posts">
    {% for post in paginator.posts %} 
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
</div> -->


---
layout: default
---

<div class="post">
  <header class="post-header">
    <h1 class="h2">Posts tagged with <em>"{{ site.data.tags[page.tag].name }}"</em></h1>
  </header>

  <article class="post-content">
    <ol>
      {% for post in site.tags[page.tag] %}
      <li>
        <a class="post-link" href="{{post.url | prepend: site.baseurl}}"><h3 class="post-title mb0">{{post.title}}</h3></a>
        <p class="post-meta small">{{ post.date | date: site.date_format }}</p>
        <div class="small">
          {% include post_tags.html tags-class="small" %}
        </div>
      </li>
      {% endfor %}
    </ol>
  </article>
</div>