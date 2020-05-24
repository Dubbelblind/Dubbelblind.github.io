---
layout: default
---

<!-- This can be used to redirect the index page to another page.
	<html>
		<head>
			<meta http-equiv="refresh" content="0; url=./avsnitt/" />
		</head>
	</html>
-->

<p>Detta är våra jättebra avsnitt:</p>
<br>

<div class="card-grid">
<!--     -->
    
    {% assign first_post = site.posts.first %}
    <div class="cards">
        <h2>
            <a class="post-link" href="{{ first_post.url | prepend: site.baseurl }}">{{ first_post.title }}</a>
        </h2>
        <p class="meta">{{ first_post.date | date: "%Y-%m-%d" }}</p>
        <p>{{ first_post.summary }} </p>
    </div>
     
    {% for post in site.posts offset:1 %}
    <br>
    <div class="cards">
        <h2>
            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <p class="meta">{{ post.date | date: "%Y-%m-%d" }}</p>
        <p>{{ post.summary }} </p>
    </div>
    {% endfor %}
    
</div>

<div class="container center-content extra-padding">
</div>
