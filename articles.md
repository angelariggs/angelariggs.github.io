---
redirect_from: "/blog/"
layout: page
permalink: /articles
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

		    	<!-- <div class="articles-page-tags">
			      {% for tag in site.tags %}
			      <h3>{{ tag[0] }}</h3>
			      {% endfor %}
		  		</div> -->

		    </article>
		{% endfor %}
	</div>
</div>