---
title: Through the Back Gate
description: Through the Back Gate event listing
layout: full-page
---
<section id="main-content">
<div class="grid-container large">
<section class="heading">
<h2 class="underline">{{ page.title }}</h2>
</section>

<div class="events-card-list fade-out-siblings">
{% assign event-list = site.events | sort: 'date' | where: 'tags','Through the Back Gate' | reverse %}

{% include event-listing.html %}