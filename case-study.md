---
layout: page
permalink: /case-studies/
---
<div>
	<div class="posts">
	  {% for case-study in site.case-studies %}
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