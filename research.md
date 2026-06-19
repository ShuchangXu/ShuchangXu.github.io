---
layout: page
permalink: /research/
title: Research
class: projects
---

{:.hidden}
# Research

{:.lead}
My research focuses on developing AI-powered assistive systems to **enhance human cognition across three core areas: perception, memory, and behavior**.

<!-- ## Enhanced Perception

My research improves visual access for blind users across digital media and the physical world. -->

## Perception Support - Accessing Digital Media

<div class="grid">
{% assign items = site.publications | where: "subgroup", "video" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>

## Perception Support - Navigating Physical World

<div class="grid">
{% assign items = site.publications | where: "subgroup", "navigation" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>

## Memory and Reasoning Support

<div class="grid">
{% assign items = site.publications | where: "theme", "Enhanced Memory and Reasoning" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>

## Behavior Support

<div class="grid">
{% assign items = site.publications | where: "theme", "Enhanced Behavior" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>
