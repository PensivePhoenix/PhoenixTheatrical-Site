---
layout: page
title: Blog
permalink: /Blog/
---

<ul class="post-list">
  {% for post in site.categories.blog %}
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
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <span class="post-meta">{{ post.date | date: date_format }}</span>
    </li>
  {% endfor %}
</ul>