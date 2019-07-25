---
permalink: /
title: "Page under construction"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Publications are now updated.

{% for post in site.posts reversed %}
  {% include archive-single.html %}
{% endfor %}