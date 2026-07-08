---
layout: page
title: "Home"
class: home
---

<div class="columns" markdown="1">

<div class="intro" markdown="1">
Hi, I'm Shuchang Xu, a Ph.D. candidate in Computer Science at the [Hong Kong University of Science and Technology](https://hkust.edu.hk/), advised by Prof. [Huamin Qu](http://www.huamin.org/). I'm currently visiting the [MIT Media Lab](https://www.media.mit.edu/groups/fluid-interfaces/overview/), where I work with Prof. [Pattie Maes](https://www.media.mit.edu/people/pattie/overview/). Previously, I earned my bachelor’s and master’s degrees from [Tsinghua University](https://www.tsinghua.edu.cn/en/) under the guidance of Prof. [Yuanchun Shi](https://pi.cs.tsinghua.edu.cn).

My research develops **AI-powered assistive systems that enhance human cognition** across perception, memory, and behavior. I design, build, and study interactive systems that enable blind users to access visual media, support older adults in revisiting meaningful life memories, and help young adults make positive behavioral changes. My work has been published at premier venues including CHI, UIST, and UbiComp, and has received Best Paper Honorable Mention Awards at CHI and UIST.
</div>


<div class="me" markdown="1">
<img src="{{ '/assets/img/me.png' | relative_url }}" alt="Shuchang Xu">

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
* Clear Water Bay, Hong Kong
</div>

</div>

## <a href="{{ "/research/" | relative_url }}">Research Overview</a>

My research focuses on AI-powered assistive systems that **enhance human cognition across three core cognitive stages: perception, memory, and behavior.**

<div class="projects overview">
<div class="grid">
  <div class="project">
    <span class="title">1. Perception Support</span>
    <p>I create <strong>multimodal AI systems</strong> and <strong>multisensory interfaces</strong> that help blind users engage with visual media.</p>
    <a href="{{ '/research/' | relative_url }}#1-perception-support" class="preview-image" style="background-image: url('{{ '/assets/img/13_SonicStage.png' | relative_url }}')"></a>
    <div class="spacer"></div>
    <div class="links"><a href="{{ '/research/' | relative_url }}#1-perception-support"><i class="fas fa-arrow-right" aria-hidden="true"></i> Learn more</a></div>
  </div>
  <div class="project">
    <span class="title">2. Memory Support</span>
    <p>I develop <strong>personalized memory agents</strong> that help people reminisce about and share past memories.</p>
    <a href="{{ '/research/' | relative_url }}#2-memory-and-reasoning" class="preview-image" style="background-image: url('{{ '/assets/img/14_RemiAssist.png' | relative_url }}')"></a>
    <div class="spacer"></div>
    <div class="links"><a href="{{ '/research/' | relative_url }}#2-memory-and-reasoning"><i class="fas fa-arrow-right" aria-hidden="true"></i> Learn more</a></div>
  </div>
  <div class="project">
    <span class="title">3. Behavior Support</span>
    <p>I create <strong>personal behavior assistants</strong> that help people understand their behaviors and support positive behavior change.</p>
    <a href="{{ '/research/' | relative_url }}#3-behavior-and-learning" class="preview-image" style="background-image: url('{{ '/assets/img/12_InteractiveBreak.png' | relative_url }}')"></a>
    <div class="spacer"></div>
    <div class="links"><a href="{{ '/research/' | relative_url }}#3-behavior-and-learning"><i class="fas fa-arrow-right" aria-hidden="true"></i> Learn more</a></div>
  </div>
</div>
</div>

<a href="{{ "/research/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  More About My Research
</a>

## <a href="{{ "/publications/" | relative_url }}">Featured Publications</a>

<div class="projects">
<div class="grid">
  {% assign sorted_publications = site.publications | sort: 'highlight' %}
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
