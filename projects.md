---
layout: page
permalink: /projects/
title: Projects
class: projects
---

{:.hidden}
# Projects

{:.lead}
My research explores how AI technologies can augment human cognition across three core domains: enhanced perception, enhanced memory, and enhanced behavior.

## Enhanced Perception

### Multi-Modal AI Systems for Video Accessibility
<div class="grid">
{% assign items = site.publications | where: "subgroup", "video" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>

### Wearable Interfaces for Accessible Navigation
<div class="grid">
{% assign items = site.publications | where: "subgroup", "navigation" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>

## Enhanced Memory
<div class="grid">
{% assign items = site.publications | where: "theme", "Enhanced Memory and Reasoning" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>

## Enhanced Behavior
<div class="grid">
{% assign items = site.publications | where: "theme", "Enhanced Behavior" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>

## Indie Game Projects

{:.lead}
Beyond my research, I create indie games that raise awareness of real-world social issues. Most of the code lives on [GitHub](https://github.com/{{ site.github_username }}).

<div class="grid">
  {% for project in site.data.projects %}
    {% include project.html project=project %}
  {% endfor %}
</div>
