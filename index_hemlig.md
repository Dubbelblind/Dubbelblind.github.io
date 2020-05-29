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

Dubbelblind är en podd om psykologisk vetenskap och de metoder som används för att ta reda på hur saker och ting faktiskt ligger till. Vi som gör podden heter Robin Fondberg och Martin Asperholm, och vi är doktorander på Avdelningen för psykologi på Karolinska Institutet. Du kan lyssna på podden genom att söka på "Dubbelblind" i din poddspelare (vi rekommenderar [Overcast](https://overcast.fm) på iOS och har ingen aning om vad som är bra på Android) eller genom att spela upp enskilda avsnitt direkt på den här hemsidan. Om du vill använda dig av RSS-feeden så hittar du den [här](./podcast.xml).

Du kan kontakta oss på <a href="mailto:dubbelblind@gmail.com">dubbelblind.podcast@gmail.com</a> eller genom Twitter där vi heter [@RobinFondberg](https://twitter.com/RobinFondberg) och [@MAsperholm](https://twitter.com/MAsperholm).

Nedan följer en lista på de avsnitt vi hittills har släppt:

{% assign first_post = site.posts.first %}
<div class="avsnitt">
	<a class="avsnitt_titel" href="{{ first_post.url | prepend: site.baseurl }}">{{ first_post.title }}</a>
	<div class="avsnitt_datum">Utgivet {{ first_post.date | date: "%Y-%m-%d" }}</div>
	<div class="avsnitt_summering">{{ first_post.summary }} </div>
</div>

{% for post in site.posts offset:1 %}
<div class="avsnitt">
	<a class="avsnitt_titel" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
	<div class="avsnitt_datum">Utgivet {{ post.date | date: "%Y-%m-%d" }}</div>
	<div class="avsnitt_summering">{{ post.summary }}</div>
</div>
{% endfor %}
