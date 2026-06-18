---
layout: page
permalink: /interests/
title: Interests
class: projects
---

{:.hidden}
# Interests

{:.lead}
Beyond my research, I create indie games that raise awareness of real-world social issues. Most of the code lives on [GitHub](https://github.com/{{ site.github_username }}).

<div class="grid">
  {% for project in site.data.projects %}
    {% include project.html project=project %}
  {% endfor %}
</div>
