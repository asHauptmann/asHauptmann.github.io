---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

You can also find my articles on <u><a href="{{"https://scholar.google.fi/citations?user=y8nRmTYAAAAJ&hl=en"}}">my Google Scholar profile</a>.</u>

<font size="4">
<u><b>Submitted</b></u>
</font>

<font size="4">
<u><b>Published</b></u>
</font>

{% for post in site.publications reversed %}
  {% capture current_year %}{{ post.date | date: "%Y" }}{% endcapture %}
  {% if current_year != previous_year %}
  <b>{{ current_year }}</b>
    {% assign previous_year = current_year %}
  {% endif %}
  {% include archive-single-publications.html %}
{% endfor %}

