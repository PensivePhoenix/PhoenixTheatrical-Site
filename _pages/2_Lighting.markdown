---
layout: page
title: Lighting
permalink: /Lighting/
carousels:
  - images: 
    - image: /images/galleries/Cinderella_DSB/283685746_1000576367315018_4981594735398417190_n.jpg
    - image: /images/galleries/Cinderella_DSB/284032864_984778745566368_7034794374658458726_n.jpg
    - image: /images/galleries/Cinderella_DSB/284347624_370998338426845_1733981835855929904_n.jpg
    - image: /images/galleries/Cinderella_DSB/284439265_1137253380179528_4731624429043135746_n.jpg
---
Some examples of my work!
{% include carousel.html height="100" unit="%" duration="10" number="1" %}


<ul class="post-list">
  {% for post in site.categories.lighting %}
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