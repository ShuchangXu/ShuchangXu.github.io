---
layout: page
permalink: /research/
title: Research
class: projects
---

{:.hidden}
# Research

{:.lead}
My research explores how AI technologies can enhance human cognition across three core areas: perception, memory, and behavior.

## Enhanced Perception

My research enhances how blind users perceive and engage with visual information across digital media and physical environments.

### Digital Media Accessibility for Blind Users

I develop multimodal AI systems that transform visual content into structured, interactive narratives, enabling blind users to understand and engage with images and videos more effectively.

<div class="grid">
{% assign items = site.publications | where: "subgroup", "video" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>

### Physical World Accessibility for Blind Users

I design multisensory on-body interfaces that provide real-time navigation feedback, helping blind users identify and follow walkable paths safely and efficiently.

<div class="grid">
{% assign items = site.publications | where: "subgroup", "navigation" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>

## Enhanced Memory

My research supports how people revisit and reason over personal information, designing AI agents that make reminiscence and problem-solving more engaging and accessible.

<div class="grid">
{% assign items = site.publications | where: "theme", "Enhanced Memory and Reasoning" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>

## Enhanced Behavior

My research fosters healthier and more effective everyday behaviors, creating interactive experiences that support relaxation, skill-building, and well-being.

<div class="grid">
{% assign items = site.publications | where: "theme", "Enhanced Behavior" | sort: "order" %}
{% for pub in items %}{% include research_card.html pub=pub %}{% endfor %}
</div>
