---
layout: page
permalink: /blog/
---
<div>
	<div class="posts">
	  {% for post in site.posts %}
	    <article class="post">

	      <h1 class='post-title'><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

	      <div class="entry">
	        {{ post.excerpt }}
	      </div>

	      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
	    </article>
	  {% endfor %}
	</div>
</div>