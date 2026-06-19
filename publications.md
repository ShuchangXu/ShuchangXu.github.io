---
layout: page
permalink: /publications/
title: Publications
class: pubs
---

{:.hidden}
# Publications

{:.lead}
Selected publications are listed below. Please see my [Google Scholar]({{ site.google_scholar }}) for the full list.

{% assign recent_years = "2026,2025" | split: "," %}
{% for ys in recent_years %}
{% assign y = ys | plus: 0 %}
## {{ y }}
{:.year}
{% assign items = site.publications | where_exp:"p","p.year == y" | sort: "pub_order" %}
{% for pub in items %}
  {% include publication.html pub=pub %}
{% endfor %}
{% endfor %}

## 2020–2024
{:.year}
{% assign mid = site.publications | where_exp:"p","p.year >= 2020 and p.year <= 2024" | sort: "pub_order" %}
{% for pub in mid %}
  {% include publication.html pub=pub %}
{% endfor %}

## Before 2020
{:.year}
{% assign older = site.publications | where_exp:"p","p.year < 2020" | sort: "year" | reverse %}
{% for pub in older %}
  {% include publication.html pub=pub %}
{% endfor %}
