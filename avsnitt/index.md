---
layout: default
---
<p>Detta är våra jättebra avsnitt:</p>

<div class="card-grid">
<!--     -->
    
    {% assign first_post = site.posts.first %}
    <div class="cards">
        <h2>
            <a class="post-link" href="{{ first_post.url | prepend: site.baseurl }}">{{ first_post.title }}</a>
        </h2>
        <p class="meta">{{ first_post.date | date: "%b %-d, %Y" }}</p>
        <p>{{ first_post.summary }} </p>
    </div>
     
    {% for post in site.posts offset:1 %}
    <br>
    <div class="cards">
        <h2>
            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <p class="meta">{{ post.date | date: "%b %-d, %Y" }}</p>
        <p>{{ post.summary }} </p>
    </div>
    {% endfor %}
    
</div>

<div class="container center-content extra-padding">
</div>
