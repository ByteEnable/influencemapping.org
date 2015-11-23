---
layout: none
---

# {{ page['Friendly Term'] }} 

{% assign practices = site.data.practices | where:"Friendly Term",page['Friendly Term'] %}
{% for practice in practices  %}
  * [{{ practice["Sub-Practice"]}}]({{ practice["Sub-Practice"] | slugify}}.html)
    <p> {{ practice['Category'] }} {{ practice['Tagline'] }} </p>
    <p> {{ practice.Description }} </p>
{% endfor %}