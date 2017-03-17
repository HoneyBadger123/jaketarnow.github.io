---
layout: post
title: blog
description: All blog posts
image: assets/images/pic11.jpg
nav-menu: true
---
<html>

{% include head.html %}

<body>

    {% include header.html %} 
    
    
<!-- Main -->
<div id="main" class="alt">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h1>{{ page.title }}</h1>
		</header>
		{% for post in site.posts %}	
		<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p><small><strong>{{ post.date | date: "%B %e, %Y" }}</strong> . {{ post.category }} . 
	</div>
</section>

</div>

    {% include footer.html %}

</body>

</html>