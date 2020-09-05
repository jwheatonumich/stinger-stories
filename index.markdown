---
layout: home
name: index
paginate:
  category: blog
---

<i>Stinger Stories</i> is a digital literary magazine dedicated to short works fantastic and unusual fiction.

<ul>
    {% for post in paginator.blog %}
      <div class="story-summary">
        <a class = "post-title" href="{{ post.url }}">{{ post.title }}</a>
        <p><i>By {{ post.author }}</i></p>
        {{ post.excerpt }}
        <a class = "post-link" href="{{ post.url }}">Read more...</a>
        <br>
      </div>
    {% endfor %}
</ul>

<!-- Pagination links -->
<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="previous">
      Previous
    </a>
  {% else %}
    <span class="previous">Previous</span>
  {% endif %}
  <span class="page_number ">
    {{ paginator.page }} of {{ paginator.total_pages }}
  </span>
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}" class="next">Next</a>
  {% else %}
    <span class="next ">Next</span>
  {% endif %}
</div>

<p>test5</p>