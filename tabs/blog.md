---
title: Otbivnoe's blog
permalink: /
layout: default
---

{% for post in site.posts | sort: "date" %}
<article class ="article" onclick="location.href='{{ post.url }}';" style="cursor: pointer;">
	<div class="article-first-line-container">
		<p class="article-date">{{ post.date | date_to_long_string }}</p>
		{% if post.badge %}
		<div class="badge">
			{{ post.badge }}
		</div>
		{% endif %}
	</div>
	<h1 class="article-title">{{ post.title }}</h1>
	<p class="article-description">{{ post.subtitle }}</p>
</article>
{% endfor %}
