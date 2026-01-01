---
layout: default
title: Blog
permalink: /blog/
---

## Writing & Thinking

This is a living log of my journey — technical deep dives, lessons learned,
and thoughts worth articulating.

---

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url | relative_url }})
<small>{{ post.date | date: "%B %d, %Y" }}</small>

{{ post.excerpt }}

---
{% endfor %}
