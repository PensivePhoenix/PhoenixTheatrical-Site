---
layout: page
title: Lighting
permalink: /Lighting/
---
<ul class="post-list">
  {% for post in site.categories.lighting %}
    <li>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
    {%- if post.image -%}
        <img src="{{- post.image | relative_url -}}" alt="" class="post-image">
    {%- else -%}
        {%- assign postImage = "" -%}
    {%- endif -%}

    </li>
  {% endfor %}
</ul>