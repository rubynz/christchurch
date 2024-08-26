---
layout: default
---

{% include about.html %}

## Meetups

We typically meet at **7:30pm on the 3rd Thursday** of the month at [Saltworks, 4 Ash Street, Christchurch](https://maps.app.goo.gl/MYdm5WXGE1U9VDVU8). See the relevant meetup for details.

{% for event in site.events reversed %}
<div class="event-summary">
  <h3>
    <span class="date">{{ event.date | date: "%b %-d, %Y" }}</span>
    <a href="{{ event.url }}">{{ event.title }}</a>
  </h3>

  <div class="time">
    {{ event.time }}
    &middot;
    <a href="https://google.com/maps/search/{{ event.location }}" target="_blank">{{ event.location }}</a>
  </div>
  <p>{{ event.content | strip_html | truncatewords: 50 }}</p>
</div>
{% endfor %}
