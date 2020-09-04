---
layout: home
name: index
---

<i>Stinger Stories</i> is a digital literary magazine dedicated to short works fantastic and unusual fiction.

<ul>
  {% for post in site.categories.blog %}
      <div class="story-summary">
        <a class = "post-title" href="{{ post.url }}">{{ post.title }}</a>
        <p><i>By {{ post.author }}</i></p>
        {{ post.excerpt }}
        <a class = "post-link" href="{{ post.url }}">Read more...</a>
        <br>
      </div>
  {% endfor %}
</ul>