---
layout: default
---

{% assign categories = site.recipes | group_by: "category" | sort: "name" | uniq %}

{% for category in categories %}
<h3>{{ category.name }}</h3>
<ul class="recipe-list">
  {% assign recipes = category.items | sort: "name" %}
  {% for recipe in recipes %}
    <li>
      <a href="{{ recipe.url | relative_url }}">{{ recipe.name | escape }}</a>
    </li>
  {% endfor %}
</ul>
{% endfor %}
