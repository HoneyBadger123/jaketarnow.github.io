---
layout: post
title: blog
description: All blog posts
image: assets/images/pic11.jpg
nav-menu: true
---
<div align="center">
<ul>
{% for post in site.posts %}
<li>{{ post.image }}<br><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
</div>