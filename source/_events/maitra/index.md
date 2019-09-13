---
title: Martin Luther Jr. Convocation
layout: full-page
---
<section id="main-content">
<div class="grid-container large">
<section class="heading">
<h2 class="underline">{{ page.title }}</h2>
</section>

<div class="events-card-list fade-out-siblings">
{% assign event-list = site.events | sort: 'date' | where: 'tags','Maitra' | reverse %}
{% for event in event-list %}
<a class="events-card" href="{{site.baseurl}}{{ event.url }}.html">
<div class="events-card-content">
<div class="date">
    <div class="month">
    {% assign m = event.billboard.month %}
    {% case m %}
        {% when 'January' %} Jan
        {% when 'February' %} Feb
        {% when 'March' %} Mar
        {% when 'April' %} Apr
        {% when 'May' %} May
        {% when 'June' %} Jun
        {% when 'July' %} Jul
        {% when 'August' %} Aug
        {% when 'September' %} Sept
        {% when 'October' %} Oct
        {% when 'November' %} Nov
        {% when 'December' %} Dec
    {% endcase %}
    </div>
    <div class="day">{{ event.billboard.date }}</div>
</div>

<div class="inner">
<div class="image">
<img src="{{ site.baseurl }}{{ event.billboard.image }}" alt="{{ event.title }}"/>
</div>
<div class="card-content">
<h4 class="header underline">{{ event.title }}</h4>
<p class="event-description">{{ event.description }}</p>
<div class="tags">
<span class="topics-title">
<div class="time">
<i class="fa fa-clock-o turquiose-text"></i> {{ event.billboard.date }} at {{ event.billboard.starttime}} to {{ event.billboard.endtime }}
</div>
<div class="location">
<i class="fa fa-map-marker turquiose-text"></i> {{ event.location.address }}
</div>
</span>
</div>
</div>
</div>   
</div>
</a>
{% endfor %}
</div>
</div>

<div class="more no-border">
<a class="primary button" href="https://events.ucsc.edu/">
See More Events
</a>
</div>

</section>