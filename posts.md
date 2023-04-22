---
layout: page
title: "Posts"
permalink: /posts/
main_nav: true
nav_order: 1
---

<ul class="posts-list">
{% for post in site.posts %}
  <li>
    <strong>
      <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    </strong>
    <span class="post-date">- {{ post.date | date_to_long_string }}</span>
  </li>
{% endfor %}
</ul>

<!-- 
{% if site.categories.size > 0 %}<h1 id="categories">Categories</h1>{% endif %}
{% for category in site.categories %}
  {% capture cat %}{{ category | first }}{% endcapture %}
  <h2 id="{{cat}}">{{ cat | capitalize }}</h2>
  <ul class="posts-list">
  {% for post in site.categories[cat] %}
    <li>
      <strong>
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </strong>
      <span class="post-date">- {{ post.date | date_to_long_string }}</span>
    </li>
  {% endfor %}
  </ul>
  {% if forloop.last == false %}<hr>{% endif %}
{% endfor %}
{% if site.categories.size > 0 %}<br>{% endif %}
{% if site.tags.size > 0 %}<h1 id="tags">Tags</h1>{% endif %}
{% for tag in site.tags %}
  {% capture tg %}{{ tag | first }}{% endcapture %}
  <h2 id="{{tg}}">{{ tg | capitalize }}</h2>
  <ul class="posts-list">
  {% for post in site.tags[tg] %}
    <li>
      <strong>
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </strong>
      <span class="post-date">- {{ post.date | date_to_long_string }}</span>
    </li>
  {% endfor %}
  </ul>
  {% if forloop.last == false %}<hr>{% endif %}
{% endfor %}
<br> -->
