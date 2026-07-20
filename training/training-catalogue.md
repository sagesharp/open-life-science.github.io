---
layout: default
title: Open Science Training Catalogue
description: Catalogue of training modules offered by Open Life Science.
---

{% assign topics = site.pages | where: 'dir', '/training/catalogue/' %}
{% assign number-modules = 0 %}
{% for topic-page in topics %}
<!-- Need to find a way to skip the cohort project presentation pages, if those get included.
Might need to skip counting modules if the page.name starts with a specific string.
-->
    {% for module in topic-page.modules %}
        {% assign number-modules = number-modules | plus:1 %}
    {% endfor %}
{% endfor %}

Open Life Science (OLS) has {{ number-modules }} training modules
that can be customized to fit your needs.

<div style="margin-top: 30px; margin-bottom: 30px;"><a class="training-navigation" href="/training/training-services">
    Training Services
</a></div>

<h2>Training Topics</h2>
{% for topic-page in topics %}
<a href="#topic-{{ topic-page.topic | slugify }}">{{ topic-page.topic }}</a>
{% endfor %}

{% for topic-page in topics %}
<h3 id="topic-{{ topic-page.topic | slugify }}"><a class="anchor" href="#topic-{{ topic-page.topic | slugify }}" aria-hidden="true"><span class="octicon octicon-link"></span></a>{{ topic-page.topic }}</h3>

{% if topic-page.topic-image and topic-page.topic-image-alt %}
<div class="media" style="margin-bottom: 10px;">
    <div><p>{{ topic-page.motivation}}</p></div>
    <div class="media-right">
        <figure class="image is-64x64">
          <img
            src="{{ topic-page.topic-image }}"
            alt="{{ topic-page.topic-image-alt }}"
          />
        </figure>
    </div>
</div>
{% else %}
{{ topic-page.motivation}}
{% endif %}

Modules:
{% for module in topic-page.modules %}
 - <a href="{{ topic-page.url }}#{{ module.title | slugify }}">{{ module.title }}</a> - {{ module.description }}
{% endfor %}
<div  style="margin-top: 30px; margin-bottom: 30px;"><a class="catalogue-navigation" href="{{ topic-page.url }}">
    View Content →
</a></div>
{% endfor %}