---
layout: page
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}

Welcome to the R15Cookie Blog!

<ul class="posts">
  {% for post in site.posts %}
    <li><h1><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h1>
    <p><span>{{ post.date | date_to_string }}</span> &raquo;</p>
    {{ post.content | truncatewords:75 }}
    </li>
  {% endfor %}
</ul>

