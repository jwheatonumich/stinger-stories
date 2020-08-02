---
layout: "exerpts"
title: "FLASH FICTION"
---

<ul>
  {% for post in site.posts %}
    <div class="story-summary">
      <a class = "post-title" href="{{ post.url }}">{{ post.title }}</a>
      {{ post.excerpt }}
      <a class = "post-link" href="{{ post.url }}">Read more</a>
      {{post.categories | capitalize | join: ', '}}
    </div>
  {% endfor %}
</ul>