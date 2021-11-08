---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
title: Blog - Product Jobs India
---
{% for post in site.posts %}
<div class="blog-post-listing">
	<div class="blog-post-date">{{ post.date | date: "%-d %b %Y" }}</div>
        <div class="blog-post-title">
	<a href="{{site.url}}{{site.baseurl}}{{post.url}}">
		{{post.title}}
        </a>
	</div>
	<div class="blog-post-excerpt">
		{% if post.excerpt %}
			{{ post.excerpt }}
		{% else %}
			{{ post.content }}
		{% endif %}
  	</div>
	<div>
		<a href="{{site.url}}{{site.baseurl}}{{post.url}}">
		Read more
        </a>
	</div>
</div>
{% endfor %}
