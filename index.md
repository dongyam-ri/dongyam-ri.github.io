---
layout: archive
permalink: /
title: "Latest Posts"
---

 <div class="tiles">
   {% assign pages_list = site.pages %}
    {% for page in pages_list %}
    
    {% assign category = page.category | default: page.title %}
    {% for post in site.categories[category] %}
      {% include post-grid.html %}
    {% endfor %}
  
      {% endif %}
    {% endfor %}
    </div>
