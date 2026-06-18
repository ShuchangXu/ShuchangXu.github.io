---
layout: page
permalink: /projects/
title: Projects
class: projects
---

{:.hidden}
# Projects

{:.lead}
Beyond my research, I design indie games that engage players with real-world societal issues, alongside some real-time rendering experiments. Most of the code lives on [GitHub](https://github.com/{{ site.github_username }}).

<div class="grid">
  {% for project in site.data.projects %}
    {% include project.html project=project %}
  {% endfor %}
</div>
