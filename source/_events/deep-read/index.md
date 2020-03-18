---
title: The Universe in Verse 2020
description: 'Join us as UC Santa Cruz presents the West Coast premiere of Universe in Verse – a charitable celebration of science through poetry created and hosted by Maria Popova.'
category: Notable
layout: full-page


#### date of the latest event to sort
date: "2020-04-18"

---
<section id="main-content">
<div class="grid-container large">
<section class="heading">
<h2 class="underline">{{ page.title }}</h2>
</section>

<div class="events-card-list fade-out-siblings">
{% assign event-list = site.events | sort: 'date' | where: 'tags','Universe' | reverse %}

{% include event-listing.html %}