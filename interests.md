---
layout: page
permalink: /interests/
title: Interests
class: interests
---

{:.hidden}
# Interests

{:.lead}
Beyond research, I love to create indie games that **reflect on real-world social issues**.

## My Games
<div class="grid">
  {% for project in site.data.projects %}
    {% include project.html project=project %}
  {% endfor %}
</div>
