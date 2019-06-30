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


{% for post in site.publications %}
  {% capture current_year %}{{ post.date | date: "%Y" }}{% endcapture %}
  {% if current_year != previous_year %}
    {% unless forloop.first %}
      </ul>
    {% endunless %}
    <h2>{{ current_year }}</h2>
    <ul>
    {% assign previous_year = current_year %}
  {% endif %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>

  {% if forloop.last %}
    </ul>
  {% endif %}
{% endfor %}


