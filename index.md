---
layout: page
title: Welcome to R15Cookie
tagline: There's always a cookie on the R15 resistor...
---
{% include JB/setup %}

Welcome to the R15Cookie Blog!  This is Steve Miller's space for thoughts about devops, security, electronics, and other random topics.  The site is currently transitioning [from my old site](https://www.r15cookie.com/doku.php)

<ul class="posts">
  {% for post in site.posts %}
    <li><h1><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h1>
    <p><span>{{ post.date | date_to_string }}</span> &raquo;</p>
    {{ post.content | truncatewords:75 }}
    </li>
  {% endfor %}
</ul>

