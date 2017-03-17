---
layout: post
title: blog
description: All blog posts
image: assets/images/pic11.jpg
nav-menu: true
---
<ul>
{% for post in site.posts %}
<li><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>{{ post.date }}</li>
{% endfor %}
</ul>