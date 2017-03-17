---
layout: post
title: blog
description: All blog posts
image: assets/images/pic11.jpg
nav-menu: true
---
{
    "posts": [
        {% for post in site.posts %}
        {
            "title": "{{ post.title | xml_escape }}",
            "url": "{{ site.url }}{{ post.url }}",
            "date": "{{ post.date | date_to_xmlschema }}"
        }{% unless forloop.last %},{% endunless %}
        {% endfor %}
    ]
}