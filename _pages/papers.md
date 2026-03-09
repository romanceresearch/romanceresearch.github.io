---
layout: single
title: "Papers"
permalink: /papers/
author_profile: false
---

Romance Research working papers, research notes, and essays.

## Working Papers

{% assign papers = site.publications | sort: "date" | reverse %}

{% for post in papers %}
### [{{ post.title }}]({{ post.url }})

{% if post.venue %}*{{ post.venue }}*{% endif %}
{% if post.date %} · {{ post.date | date: "%B %Y" }}{% endif %}

{{ post.excerpt | strip_html | truncate: 220 }}

{% if post.paperurl %}
[Download PDF]({{ post.paperurl }})
{% endif %}

---
{% endfor %}
