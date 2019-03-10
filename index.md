---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

{%- if site.recipes.size > 0 -%}
  <ul>
    {%- for recipe in site.recipes -%}
      <li>
        <a href="{{ recipe.url | relative_url }}">{{ recipe.name | escape }}</a>
      </li>
    {%- endfor -%}
  </ul>
{%- endif -%}
