---
layout: page
title: Fiction
description: Stories I have written
image: assets/images/halforc.webp
nav-menu: true
---

<div id="main" class="alt">
	<section id="pre">
		<h1>Fiction</h1>
		<p>Below you can find a few stories I have written. </p>
	</section>
    <section id="one">
        {% assign sorted = site.fiction | reverse %}
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