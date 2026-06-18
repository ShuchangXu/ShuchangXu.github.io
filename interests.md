---
layout: page
permalink: /interests/
title: Interests
class: projects
---

{:.hidden}
# Interests

{:.lead}
Beyond my research, I enjoy creating indie games that raise awareness of real-world social issues, such as gender equity and online credibility.

<div class="grid">
  {% for project in site.data.projects %}
    {% include project.html project=project %}
  {% endfor %}
</div>
