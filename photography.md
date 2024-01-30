---
layout: page
title: Photography
description: Sharing a few pictures I have snapped
image: assets/images/halforc.webp
nav-menu: true
---

<div id="main" class="alt">
	<section id="pre">
		<h1>Photography</h1>
		<p>Sometimes I take pictures. Well, I take a lot of pictures. Occasionally I'll share one or two</p>
	</section>
    <section id="one">
        {% assign sorted = site.photography | reverse %}
        {% for post in sorted %}
            <p >
	          {% if post.title != 404 %}
	            <header class="major">
	              <h3><a href="{{ post.url | relative_url }}" class="link">{{ post.title }}</a></h3>
	            </header>
	            {% if post.image %}<span class="image left"><img src="{{ site.baseurl }}/{{ post.image }}" alt="" /></span>{% endif %}
	            {% if post.date %}<p>{{ post.date | date: "%-d %B %Y" }}</p>{% endif %}
	            <p>{{ post.description }}</p>
	          {% endif %}
            </p>
        {% endfor %}
    </section>	
</div>
<div style="clear:both"></div>