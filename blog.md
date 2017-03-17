---
layout: post
title: blog
description: All blog posts
image: 
nav-menu: true
---
<div align="center">
{% for post in site.posts %}
	{% if site.tiles-source == 'posts' %}
        <article>
                <span class="image">
                        <img src="{{ site.baseurl }}/{{ post.image }}" alt="" />
                </span>
                <header class="major">
                        <h3><a href="{{ post.url  | relative_url }}" class="link">{{ post.title }}</a></h3>
                        <p>{{ post.description }}</p>
                </header>
        </article>
	{% endif %}
{% endfor %}
</div>