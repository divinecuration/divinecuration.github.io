---
layout: page
title: Posts
---

{% for post in site.posts %}
{% assign wordCount = post.content | number_of_words %}
<div class="post_title">
  <!-- &raquo;  -->
  <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title}}</a>
  <p class="post_date">{{ post.date | date: "%d %B %Y" }}</p>
  <div class="post_subtitle">{{ wordCount }} words</div>
  <div class="post_subtitle">
  {% for category in post.categories %}
  <a class="list_tag" href="{{site.baseurl}}/{{category}}/">#{{category}}</a>
  {% endfor %}
  </div>

</div>

<hr />

{% endfor %}

<!---
<div class="home">
  <div class="post-list">

    {% for post in paginator.posts %}

    <article class="post_card post">
      <header class="post_header">
        <h2 class="post_title"><a href="{{ post.url | prepend: site.baseurl }}">{{ post.subtitle}}</a></h2>
        <time class="post_date">{{ post.date | date: "%d %B %Y" }}</time>
        <br />
        <br />

      </header>
      <div class="post_excerpt">
        <p>
          {% if post.description %}
          {{ post.description}}
          <a class="read-more" href="{{ post.url | prepend: site.baseurl }}"> read more</a> »
          {% else %}
          {{ post.excerpt }}
          {% if post.excerpt_separator  %}
          <a class="read-more" href="{{ post.url | prepend: site.baseurl }}"> read more</a> »
          {% else %}
          {% endif %}
          {% endif %}
        </p>
      </div>

      <footer class="post_meta">
        <div class="post-categories">
          {% if post %}
            {% assign categories = post.categories %}
          {% else %}
            {% assign categories = page.categories %}
          {% endif %}
          {% for category in categories %}
          <a href="{{site.baseurl}}/{{category}}/">#{{category}}</a>
          {% endfor %}
        </div>
      </footer>
      <hr/>
    </article>
    {% endfor %}

    {% if paginator.total_pages > 1 %}
    <div class="pagination-older-post">
      {% if paginator.previous_page %}
        <a href="{{ paginator.previous_page_path | relative_url }}">&laquo; Prev</a>
      {% else %}
        <span>&laquo; Prev</span>
      {% endif %}

      {% for page in (1..paginator.total_pages) %}
        {% if page == paginator.page %}
          <em>{{ page }}</em>
        {% elsif page == 1 %}
          <a href="/">{{ page }}</a>
        {% else %}
          <a href="{{ site.paginate_path | relative_url | replace: ':num', page }}">{{ page }}</a>
        {% endif %}
      {% endfor %}

      {% if paginator.next_page %}
        <a href="{{ paginator.next_page_path | relative_url }}">Next &raquo;</a>
      {% else %}
        <span>Next &raquo;</span>
      {% endif %}
    </div>
    {% endif %}
  </div>
</div>
--->