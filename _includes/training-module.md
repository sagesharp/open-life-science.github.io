<!--
Make sure that each training module has a unique title,
otherwise the links to each module section for the two duplicate titles won't work.
That's because each anchor id needs to be unique,
and we're using the module title to create part of the HTML link (slug).
-->
<!--
The module description should be one paragraph only.
Otherwise the list of training modules in the training catalog page may look weird.
-->
{% assign topic = page.topic %}
{% assign motivation = page.motivation %}
{% assign customization = page.customization %}
{% assign modules = page.modules %}
{% assign topic-image = page.topic-image %}
{% assign topic-image-alt = page.topic-image-alt %}


{% if topic-image and topic-image-alt %}
<div class="media" style="margin-bottom: 10px;">
    <div><p>{{ motivation}}</p></div>
    <div class="media-right">
        <figure class="image is-64x64">
          <img
            src="{{ topic-image }}"
            alt="{{ topic-image-alt }}"
          />
        </figure>
    </div>
</div>
{% else %}
{{ motivation }}
{% endif %}

{% if customization %}{{ customization }}{% else %}Open Life Science can [customize our Open Data training modules to fit your needs](/training/training-services).{% endif %}

<div style="margin-top: 30px; margin-bottom: 30px;"><a class="training-navigation" href="/training/training-services">
    Training Services
</a></div>

<h2 id="topics"><a class="anchor" href="#topics" aria-hidden="true"><span class="octicon octicon-link"></span></a>{{ topic }} Topics</h2>

{% for module in modules %}
<p><a href="#module-{{ module.title | slugify }}">{{ module.title }}</a></p>
{% endfor %}

<div  style="margin-top: 30px; margin-bottom: 30px;"><p><a class="catalogue-navigation" href="/training/training-catalogue">
    ❮ Back to Catalogue
</a></p></div>

{% for module in modules %}
<hr>
<h2 id="module-{{ module.title | slugify }}"><a class="anchor" href="#module-{{ module.title | slugify }}" aria-hidden="true"><span class="octicon octicon-link"></span></a>{{ module.title }}</h2>

{{ module.description }}

{% if module.learning-goals %}<h3>Learning goals</h3>

{{ module.learning-goals }}
{% endif %}
{% if module.prework %}<h3>Prework</h3>

{{ module.prework }}
{% endif %}

<div  style="margin-top: 30px; margin-bottom: 30px;"><a class="catalogue-navigation" href="#topics">
    ↑ Other Topics
</a></div>

{% endfor %}