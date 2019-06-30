---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

You can also find my articles on <u><a href="{{"https://scholar.google.fi/citations?user=y8nRmTYAAAAJ&hl=en"}}">my Google Scholar profile</a>.</u>

{% for post in site.publications reversed %}
  {% capture current_year %}{{ post.date | date: "%Y" }}{% endcapture %}
  {{ current_year }}
  {% include archive-single-publications.html %}
{% endfor %}

