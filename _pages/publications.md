---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}


{% for post in site.publications reversed %}
  {% capture current_year %}{{ post.date | date: "%Y" }}{% endcapture %}
  {% if current_year != previous_year %}
    <b>{{ current_year }}</b>
    {% assign previous_year = current_year %}
  {% endif %}
  {% include archive-single-publications.html %}
{% endfor %}

