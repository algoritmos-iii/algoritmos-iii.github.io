---
layout: page
title: Docentes
---
<style>
.gallery {
  display: flex;
}

.card {
  border: 1px solid #dadada;
  box-shadow: 4px 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.2s;
  width: 50%;
  margin: 3px;
}

.card h1 {
  padding: 2px;
  margin: 8px 0;
}

.card:hover {
  box-shadow: 8px 8px 16px 0 rgba(0, 0, 0, 0.2);
}

.card .container {
  padding: 2px 14px;
}
</style>
<div class="gallery">
{%- for image in site.static_files -%}
  {%- if image.path contains '/assets/docentes/' -%}
    {%- assign filenameparts = image.path | split: "/" -%}
    {%- assign filename = filenameparts | last | replace: image.extname,"" -%}
    <div class="card">
      <img src="{{image.path | relative_url }}" alt="image" class="center" style="width:100%"/>
      <div class="container">
        <h1>{{ filename }}</h1>
        <a href="">
          <img align="left" alt="{{filename}}" width="22px" src="https://icongr.am/fontawesome/github.svg?size=128" />
        </a>
        <a href="">
          <img align="left" alt="{{filename}}" width="22px" src="https://icongr.am/clarity/email.svg?size=128&color=currentColor" />
        </a>
      </div>
    </div>
  {%- endif -%}
{%- endfor -%}
</div>