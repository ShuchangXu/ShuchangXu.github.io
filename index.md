---
layout: page
title: "Home"
class: home
---

# Hi, I'm Shuchang Xu

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I'm a Ph.D. candidate in Computer Science at the [Hong Kong University of Science and Technology](https://hkust.edu.hk/), advised by Prof. [Huamin Qu](http://www.huamin.org/). I'm currently a visiting student at the [MIT Media Lab](https://www.media.mit.edu/groups/fluid-interfaces/overview/), working with Prof. [Pattie Maes](https://www.media.mit.edu/people/pattie-maes/) in the Fluid Interfaces Group. 
Before my PhD, I earned my degrees from [Tsinghua University](https://www.tsinghua.edu.cn/en/): an M.S. in [Computer Science](https://www.cs.tsinghua.edu.cn/csen/) (advised by Prof. [Yuanchun Shi](https://pi.cs.tsinghua.edu.cn)), a B.E. in [Electrical Engineering](https://www.eea.tsinghua.edu.cn/en/).

My research focuses on **AI-powered assistive systems for enhancing human cognition**.  I explore how emerging technologies can support people’s cognitive needs in critical contexts, including visual media accessibility for blind users and memory support for older adults. My work has been published at CHI, UIST, and UbiComp, and has received Best Paper Honorable Mention Awards at CHI and UIST.
</div>


<div class="me" markdown="1">
<img src="{{ '/assets/img/me.png' | relative_url }}" alt="Shuchang Xu">

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
* Clear Water Bay, Hong Kong
</div>

</div>

## Research Overview

My research focuses on developing AI-powered assistive systems that augment **human cognition** for blind and aging populations, across three core areas:

**1. Personalized Memory Agents for Reminiscence.** I develop personal memory agents that help users relive meaningful memories — through independent reminiscence with proactive chatbots ([UIST 2024](https://dl.acm.org/doi/10.1145/3654777.3676336)), collaborative reminiscence with therapist-in-the-loop support, and everyday reminiscence integrated into daily routines.

**2. Multi-Modal AI Systems for Video Accessibility.** I build machine-learning pipelines that enable blind and low-vision users to understand and engage with video: making online comments accessible ([CHI 2025](https://dl.acm.org/doi/10.1145/3706598.3713496)), enabling interactive exploration of 360° videos ([UIST 2025](https://arxiv.org/abs/2507.09959)), and enhancing spatial awareness in film and television ([Sonic Stage](https://shuchangxu.github.io/Sonic_Stage_Demo/)).

**3. Multi-Sensory Interfaces for Outdoor Navigation.** I develop wearable systems that support navigation through multi-sensory feedback: on-body haptics ([IMWUT 2020](https://dl.acm.org/doi/abs/10.1145/3411814)), handheld vibrations ([CHI 2021](https://dl.acm.org/doi/10.1145/3411764.3445644)), and head-mounted light cues ([IMWUT 2021](https://dl.acm.org/doi/10.1145/3463524)).

## <a href="{{ "/publications/" | relative_url }}">Featured Publications</a>

<div class="featured-publications">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    {% if pub.highlight %}
      <a href="{% if pub.pdf %}{{ pub.pdf }}{% elsif pub.arxiv %}https://arxiv.org/abs/{{ pub.arxiv }}{% elsif pub.doi %}https://doi.org/{{ pub.doi }}{% endif %}" class="publication">
        <strong>{{ pub.title }}</strong>
        <span class="authors">{% for author in pub.authors %}{% if author == "Shuchang Xu" %}<b>{{ author }}</b>{% else %}{{ author }}{% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>.
        <i>{% if pub.venue %}{{ pub.venue }}, {% endif %}{{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-trophy" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
    {% endif %}
  {% endfor %}
</div>

<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a>

## <a href="{{ "/interests/" | relative_url }}">Interests</a>

Beyond research, I create indie games that engage players with real-world social issues.

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>

<a href="{{ "/interests/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show More Interests
</a>

## News

<div class="news">
<ul>
  {% for news in site.data.news %}
    {% include news.html news=news %}
  {% endfor %}
</ul>
</div>
