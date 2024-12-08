---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<h1> See my most recent Show <h1>

<ul class="post-list">
  {% for post in site.categories.show limit:1 %}
    <li>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <span class="post-meta">{{ post.date | date: date_format }} --- {{ post.venue | escape}} --- {{ post.location | escape }}</span>
        <br />
    {%- if post.image -%}
        <img src="{{- post.image | relative_url -}}" alt="" class="post-image">
    {%- else -%}
        {%- assign postImage = "" -%}
    {%- endif -%}
    </li>
  {% endfor %}
</ul>