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
      <div class="post-categories">
          {% if post %}
            {% assign categories = post.categories %}
          {% else %}
            {% assign categories = page.categories %}
          {% endif %}
          {% for category in categories %}
          <a href="{{site.baseurl}}/categories/#{{category|slugize}}">{{category}}</a>
          {% unless forloop.last %}&nbsp;{% endunless %}
          {% endfor %}
      </div>
    </div>
  {% endfor %}
</ul>