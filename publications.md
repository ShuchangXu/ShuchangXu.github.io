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

{% assign pubyears = site.publications | group_by:"year" %}
{% assign sorted_pubyears = pubyears | sort: "name" | reverse %}
{% for year in sorted_pubyears %}
## {{ year.name }}
{:.year}
{% for pub in year.items %}
  {% include publication.html pub=pub %}
{% endfor %}
{% endfor %}
