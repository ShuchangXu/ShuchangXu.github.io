---
layout: page
permalink: /publications/
title: Publications
class: pubs
---

{:.hidden}
# Publications

{:.lead}
A full list of my publications. <b>Bold</b> name marks my contributions. See also my [Google Scholar]({{ site.google_scholar }}).

{% assign recent_years = "2026,2025" | split: "," %}
{% for ys in recent_years %}
{% assign y = ys | plus: 0 %}
## {{ y }}
{:.year}
{% assign items = site.publications | where_exp:"p","p.year == y" | sort: "order" %}
{% for pub in items %}
  {% include publication.html pub=pub %}
{% endfor %}
{% endfor %}

## 2024 & Earlier
{:.year}
{% assign older = site.publications | where_exp:"p","p.year <= 2024" | sort: "year" | reverse %}
{% for pub in older %}
  {% include publication.html pub=pub %}
{% endfor %}
