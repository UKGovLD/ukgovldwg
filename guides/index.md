---
title: Guides
layout: default

menu_tagline: Guides are articles concentrating on a specific theme or technology.
---

<div class="row">
	<div class="two-thirds">
		<h1>{{ site.data.guides.title }}</h1>
		<h2 class="descriptive">{{ page.menu_tagline }}</h2>
	</div>
</div>
<div class="row">
	<div class="three-thirds columnise-lists">
		{% include guides_menu.html %}
	</div>
</div>