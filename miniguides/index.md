---
title: Miniguides
layout: default

menu_tagline: Miniguides are shorter articles concentrating on a specific theme or technology.
---

<div class="row">
	<div class="two-thirds">
		<h1>{{ site.data.miniguides.title }}</h1>
		<h2 class="descriptive">{{ page.menu_tagline }}</h2>
	</div>
</div>
<div class="row">
	<div class="three-thirds columnise-lists">
		{% include miniguides_menu.html %}
	</div>
</div>