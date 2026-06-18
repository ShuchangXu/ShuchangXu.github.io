---
layout: page
permalink: /publications/
title: Publications
class: pubs
---

{:.hidden}
# Publications

{:.lead}
My research builds AI-powered assistive systems that augment human perception and cognition. <b>Bold</b> name marks my contributions. See also my [Google Scholar]({{ site.google_scholar }}).

{% assign themes = "Enhanced Perception|Enhanced Memory and Reasoning|Enhanced Behavior|Sensing and Machine Learning" | split: "|" %}
{% for theme in themes %}
## {{ theme }}
{:.theme}
{% assign items = site.publications | where: "theme", theme | sort: "order" %}
{% for pub in items %}
  {% include publication.html pub=pub %}
{% endfor %}
{% endfor %}
