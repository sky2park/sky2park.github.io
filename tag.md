---
layout: page
title: "Tags"
permalink: /tag/
main_nav: true
nav_order: 3
---

{% if site.tags.size > 0 %}
{% for tag in site.tags %}
{% capture tg %}{{ tag | first }}{% endcapture %}
<h2 id="{{tg}}">{{ tg | capitalize }}</h2>
<ul class="posts-list">
{% for post in site.tags[tg] limit:site.limit %}
  <li>
    <strong>
      <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    </strong>
    <span class="post-date">- {{ post.date | date_to_long_string }}</span>
  </li>
{% endfor %}
{% if site.tags[tg].size > site.limit %}
  <li><a href="{{ site.baseurl }}/tag/{{ tg }}">...And more</a></li>
{% endif %}
</ul>

{% if forloop.last == false %}<hr>{% endif %}
{% endfor %}
{% else %}
포스트가 없습니다. 아직은요..
{% endif %}
<br>