---
layout: default
title: Home
---

<!-- Show last 5 posts here -->
{% for post in site.posts limit: 5  %}
	<article>

        <header>
            <h2><a href="{{site.baseurl}}{{post.url}}">{{ post.title }}</a></h2>
            <span class="date"><i class="icon-clock"></i><time datetime="{{post.date|date:"%F"}}">{{post.date|date:"%b %d, %Y"}}</time></span><br/>
            <span class="category"><i class="icon-tag"></i> {{ post.categories | category_links }}</span><br/>
            <span class="author"><i class="icon-user"></i> {% if post.author %}{{post.author}}{% else %}{{site.author}}{% endif%}</span>
        </header>

		<div class="entry">{{ post.excerpt }}</div>

	</article>
{% endfor %}




{% include JB/setup %}


