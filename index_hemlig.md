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

<img src="./images/Logo.jpg" class="logo">

Dubbelblind är en podd om psykologisk vetenskap och de metoder som används för att ta reda på hur saker och ting faktiskt ligger till. Vi som gör podden heter Robin Fondberg och Martin Asperholm, och vi är doktorander på Avdelningen för psykologi på Karolinska Institutet. Du kan lyssna på podden genom att söka på "Dubbelblind" i din poddspelare (vi rekommenderar [Overcast](https://overcast.fm) på iOS och har ingen aning om vad som är bra på Android) eller genom att spela upp enskilda avsnitt direkt på den här hemsidan. Om du vill använda dig av RSS-feeden så hittar du den [här](./podcast.xml).

Du kan kontakta oss på <a href="mailto:dubbelblind@gmail.com">dubbelblind.podcast@gmail.com</a> eller genom Twitter där vi heter [@RobinFondberg](https://twitter.com/RobinFondberg) och [@MAsperholm](https://twitter.com/MAsperholm).

Nedan följer en lista på de avsnitt vi hittills har släppt:

{% assign first_post = site.posts.first %}
<div class="avsnitt">
	<div class="avsnitt_titel"><a href="{{ first_post.url | prepend: site.baseurl }}" class="avsnitt_titel_länk">{{ first_post.title }}</a></div>
	<div class="avsnitt_info"> 
		Längd: {{ first_post.duration }} • Utgiven: <time datetime="{{ first_post.date | date_to_xmlschema }}" itemprop="datePublished">{{ first_post.date | date: "%Y-%m-%d" }}</time> • <a href="{{ site.baseurl }}{{ first_post.file }}" download="{{ first_post.title }}">Ladda hem</a>
	</div>
	<div class="avsnitt_uppspelare">
       		<audio controls>
        		<source src="{{ first_post.file }}" type="audio/mp3">
        	</audio>
    	</div>
	<div class="avsnitt_summering">{{ first_post.summary }} </div>
	<div class="avsnitt_beskrivning">{{ first_post.description }} </div>
</div>

{% for post in site.posts offset:1 %}
<div class="avsnitt">
	<div class="avsnitt_titel"><a href="{{ post.url | prepend: site.baseurl }}" class="avsnitt_titel_länk">{{ post.title }}</a></div>
	<div class="avsnitt_info"> 
		Längd: {{ post.duration }} • Utgiven: <time datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">{{ post.date | date: "%Y-%m-%d" }}</time> • <a href="{{ site.baseurl }}{{ post.file }}" download="{{ post.title }}">Ladda hem</a>
	</div>
	<div class="avsnitt_uppspelare">
       		<audio controls>
        		<source src="{{ post.file }}" type="audio/mp3">
        	</audio>
    	</div>
	<div class="avsnitt_summering">{{ post.summary }} </div>
	<div class="avsnitt_beskrivning">{{ post.description }} </div>
</div>
{% endfor %}
