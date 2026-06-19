---
layout: page
title: "Home"
class: home
---

# **Hi, I'm Shuchang**

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I'm a Ph.D. candidate in Computer Science at the [Hong Kong University of Science and Technology](https://hkust.edu.hk/), advised by Prof. [Huamin Qu](http://www.huamin.org/). I'm currently a visiting student at the [MIT Media Lab](https://www.media.mit.edu/groups/fluid-interfaces/overview/), where I work with Prof. [Pattie Maes](https://www.media.mit.edu/people/pattie/overview/). Before my Ph.D., I completed my undergraduate and master's studies at [Tsinghua University](https://www.tsinghua.edu.cn/en/), where I was advised by Prof. [Yuanchun Shi](https://pi.cs.tsinghua.edu.cn).

My research focuses on **AI-powered assistive systems that enhance human cognition**, with an emphasis on perception, memory, and behavior. My work has been published at CHI, UIST, and UbiComp, and has received Best Paper Honorable Mention Awards at CHI and UIST.
</div>


<div class="me" markdown="1">
<img src="{{ '/assets/img/me.png' | relative_url }}" alt="Shuchang Xu">

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
* Clear Water Bay, Hong Kong
</div>

</div>

## <a href="{{ "/research/" | relative_url }}">Research Overview</a>

My research focuses on AI-powered assistive systems that **enhance human cognition across three core areas: memory, perception, and behavior.**

<div class="projects overview">
<div class="grid">
  <div class="project">
    <span class="title">1. Perception Support</span>
    <p>I create <strong>multimodal AI systems</strong> and <strong>multisensory interfaces</strong> that help blind users engage with visual media.</p>
    <a href="{{ '/research/' | relative_url }}#perception-support---visual-accessibility" class="preview-image" style="background-image: url('{{ '/assets/img/Area_1.png' | relative_url }}')"></a>
    <div class="spacer"></div>
    <div class="links"><a href="{{ '/research/' | relative_url }}#perception-support---visual-accessibility"><i class="fas fa-arrow-right" aria-hidden="true"></i> Learn more</a></div>
  </div>
  <div class="project">
    <span class="title">2. Memory Support</span>
    <p>I develop <strong>personalized memory agents</strong> that help people reminisce about and share past memories.</p>
    <a href="{{ '/research/' | relative_url }}#memory-and-reasoning-support" class="preview-image" style="background-image: url('{{ '/assets/img/Area_2.png' | relative_url }}')"></a>
    <div class="spacer"></div>
    <div class="links"><a href="{{ '/research/' | relative_url }}#memory-and-reasoning-support"><i class="fas fa-arrow-right" aria-hidden="true"></i> Learn more</a></div>
  </div>
  <div class="project">
    <span class="title">3. Behavior Support</span>
    <p>I create <strong>personal behavior assistants</strong> that help people understand their behaviors and support positive behavior change.</p>
    <a href="{{ '/research/' | relative_url }}#behavior-and-learning-support" class="preview-image" style="background-image: url('{{ '/assets/img/Area_3.png' | relative_url }}')"></a>
    <div class="spacer"></div>
    <div class="links"><a href="{{ '/research/' | relative_url }}#behavior-and-learning-support"><i class="fas fa-arrow-right" aria-hidden="true"></i> Learn more</a></div>
  </div>
</div>
</div>

<a href="{{ "/research/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  More About My Research
</a>

## <a href="{{ "/publications/" | relative_url }}">Featured Publications</a>
Here are a few recent publications:

<div class="projects">
<div class="grid">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}{% if pub.highlight %}{% include research_card.html pub=pub %}{% endif %}{% endfor %}
</div>
</div>

<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  All Publications
</a>

## <a href="{{ "/interests/" | relative_url }}">Beyond Research</a>

Beyond research, I love to **create indie games that reflect on real-world social issues**.

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
  More Projects
</a>

## News

<div class="news">
<ul>
  {% for news in site.data.news %}
    {% include news.html news=news %}
  {% endfor %}
</ul>
</div>
