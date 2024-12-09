---
layout: page
title: Sound
permalink: /Sound/
---

<ul class="post-list">
  {% for post in site.categories.sound %}
    <li>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        <!-- {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%} -->
        <span class="post-meta"><!-- {{ post.date | date: date_format }} --- -->{{ post.venue | escape}} --- {{ post.location | escape }}</span>
        <br />
    {%- if post.image -%}
        <a class="post-link" href="{{ post.url | relative_url }}"><img src="{{- post.image | relative_url -}}" alt="" class="post-image"></a>
    {%- else -%}
        {%- assign postImage = "" -%}
    {%- endif -%}
    </li>
  {% endfor %}
</ul>