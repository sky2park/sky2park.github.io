---
layout: page
title: "Categories"
permalink: /category/
main_nav: true
nav_order: 2
---

{% if site.categories.size > 0 %}
{% for category in site.categories %}
{% capture cat %}{{ category | first }}{% endcapture %}
<h2 id="{{cat}}">{{ cat | capitalize }}</h2>
<ul class="posts-list">
{% for post in site.categories[cat] limit:site.limit %}
  <li>
    <strong>
      <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    </strong>
    <span class="post-date">- {{ post.date | date_to_long_string }}</span>
  </li>
{% endfor %}
{% if site.categories[cat] > site.limit %}
  <li><a href="{{ site.baseurl }}/category/{{ cat }}">...And more</a></li>
{% endif %}
</ul>
{% if forloop.last == false %}<hr>{% endif %}
{% endfor %}
{% else %}
포스트가 없습니다. 아직은요..
{% endif %}
<br>