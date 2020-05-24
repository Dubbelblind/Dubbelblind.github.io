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

# Dubbelblind

Dubbelblind är en podd om psykologisk vetenskap och de metoder som används för att ta reda på hur saker och ting egentligen ligger till. Vi som gör podden heter Robin Fondberg och Martin Asperholm, och vi är doktorander vid Avdelningen för psykolgoi på Karolinska Institutet. Du kan lyssna på podden genom att söka på "Dubbelblind" i din poddspelare (vi rekommenderar [Overcast](https://overcast.fm) på iOS och X på Android) eller genom att spela upp enskilda avsnitt direkt på den här hemsidan. Om du vill använda dig av RSS-feeden så hittar du den [här](www.dubbelblind.github.io/podcast.xml).

Du kan kontakta oss på dubbelblind.podcast@gmail.com eller genom Twitter där vi heter [@RobinFondberg](https://twitter.com/RobinFondberg) och [@MAsperholm](https://twitter.com/MAsperholm).

Nedan följer en lista på de avsnitt vi hittills har släppt:

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
