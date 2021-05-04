---
layout: page
title: Docentes
---

{%- for image in site.static_files -%}
    {%- if image.path contains '/assets/docentes/' -%}
    <h1>Profe!</h1>
    <img src="{{image.path | relative_url }}" alt="image" width="60" height="60"/>
    {%- endif -%}
{%- endfor -%}


