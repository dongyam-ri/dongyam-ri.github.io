---
layout: archive
permalink: /
title: "Category"
---

<header class="site-category">
  <ul>

    {% assign pages_list = site.pages %}
    {% for node in pages_list %}
      {% if node.title != null %}
        {% if node.layout == "category" %}
          <H3>
          <li style="padding: 5px 0px 5px 5px;
                     margin-bottom: 5px;
                     font-size: 30px;">
            <a class="category-link {% if page.url == node.url %} active{% endif %}"
            href="{{ site.baseurl }}{{ node.url }}">{{ node.title }}</a></li>
          </H3>
        {% endif %}
      {% endif %}
    {% endfor %}

</ul>
</header>
