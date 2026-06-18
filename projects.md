---
layout: page
permalink: /projects/
title: Projects
class: projects
---

{:.hidden}
# Projects

{:.lead}
My research explores how AI technologies can enhance human cognition, particularly in three core areas: (1) Enhanced Perception, (2) Enhanced Memory and Reasoning, and (3) Enhanced Behavior. Beyond research, I also design indie games that raise awareness for real-world societal issues.

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

## Enhanced Memory and Reasoning
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
I design indie games that raise awareness for real-world societal issues. Most of the code lives on [GitHub](https://github.com/{{ site.github_username }}).

<div class="grid">
  {% for project in site.data.projects %}
    {% include project.html project=project %}
  {% endfor %}
</div>
