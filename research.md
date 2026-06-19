---
layout: page
permalink: /research/
title: Research
class: projects
---

{:.hidden}
# Research

{:.lead}
My research develops AI-powered assistive systems that **enhance human cognition across three core areas: perception, memory, and behavior**.

<!-- ## Enhanced Perception

My research improves visual access for blind users across digital media and the physical world. -->

<!-- ## Perception Support - Video Accessibility

<div class="grid">
{% assign items = site.publications | where: "subgroup", "video" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>

## Perception Support - Multi-Sensory Navigation

<div class="grid">
{% assign items = site.publications | where: "subgroup", "navigation" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div> -->

## 1. Perception Support

<div class="grid">
{% assign items = site.publications | where: "subgroup", "video" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}

{% assign items = site.publications | where: "subgroup", "navigation" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>

## 2. Memory and Reasoning

<div class="grid">
{% assign items = site.publications | where: "theme", "Enhanced Memory and Reasoning" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>

## 3. Behavior and Learning

<div class="grid">
{% assign items = site.publications | where: "theme", "Enhanced Behavior" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>
