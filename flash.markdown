---
layout: "exerpts"
title: "FLASH FICTION"
---

<ul>
  {% for post in site.posts %}
    <div class="story-summary">
      <a class = "post-title" href="{{ post.url }}">{{ post.title }}</a>
      <p><i>By {{ post.author }}</i></p>
      {{ post.excerpt }}
      <a class = "post-link" href="{{ post.url }}">Read more</a>
    </div>
  {% endfor %}
</ul>