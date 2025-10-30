---
layout: page
title: Research
---

For a complete list of publications see my [Google Scholar](https://scholar.google.de/citations?user=2HpXCQ0AAAAJ) or [Orcid](https://orcid.org/0000-0003-2766-3982) pages. My dissertation is published [here](https://kups.ub.uni-koeln.de/64465/).

## Selected Topics

Click on a topic for brief descriptions of selected publications.

{% for project in site.research %}
  <h3>
    <a href="{{ project.url | relative_url }}">
    {{ project.title | escape }}
    </a>
  </h3>
  {{ project.excerpt }}
{% endfor %}
