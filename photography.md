---
layout: page
permalink: /photography/
---
<div>
  <div>
    {% for photography in site.photographies %}
      <div>

        <h1><a href="{{ site.baseurl }}{{ photography.url }}">{{ photography.title }}</a></h1>

        <div class="entry">
          {{ photography.excerpt }}
        </div>

        <a href="{{ site.baseurl }}{{ photography.url }}" class="read-more">Read More</a>
      </div>
    {% endfor %}
  </div>
</div>