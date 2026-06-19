---
layout: page
permalink: /interests/
title: Interests
class: interests
---

{:.hidden}
# Interests

{:.lead}
Beyond my research, I create indie games that engage players with real-world social issues.

<div class="grid">
  {% for project in site.data.projects %}
    {% include project.html project=project %}
  {% endfor %}
</div>
