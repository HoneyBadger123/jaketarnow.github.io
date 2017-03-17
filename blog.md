---
layout: post
title: blog
description: All blog posts
image: assets/images/pic11.jpg
nav-menu: true
---
<div align="center">
<ul style="list-style: none;">
{% for post in site.posts %}
<li><span class="image main"><img src="{{ site.baseurl }}/{{ post.image }}" alt="" /></span><br><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a><br><br></li>
{% endfor %}
</ul>
</div>