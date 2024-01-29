---
layout: page
title: Trains
description: Some of my trains content
image: assets/images/cropped-southern-daylight.webp
nav-menu: true
---

<div id="main" class="alt">
	<section id="pre">
		<h1>Trains</h1>
		<p>Here are my posts about trains and model railroading. It's my favorite hobby.</p>
	</section>
    <section id="one">
        {% assign sorted = site.trains | reverse %}
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