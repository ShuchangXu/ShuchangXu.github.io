---
layout: page
permalink: /research/
title: Research
class: projects
---

{:.hidden}
# Research

{:.lead}
My research explores how AI technologies can augment human cognition across three core areas: (1) enhanced perception, (2) enhanced memory, and (3) enhanced behavior.

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
