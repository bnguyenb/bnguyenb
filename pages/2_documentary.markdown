---
layout: page
menu: documentary
title: Documentary
permalink: /documentary/
---
<p>
  Beside of my work, i'm playing with street and travel photography at free time. I'm using Fujifilm Camera to document all around me.
</p>

<style>
  .image-gallery-index {overflow: auto; margin-left: -1%!important;}
  .image-gallery-index a {float: left; display: block; margin: 0 0 1% 1%; width: 19%; text-decoration: none !important;}
  .image-gallery-index a img {width: 100%; display: block;}
  .image-gallery-index a span {display: block; text-align: center; padding: 3px 0;}
</style>

<ul class="post-list">
  {%- for post in site.categories['documentary'] -%}
  <li>
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
    <span class="post-meta">{{ post.date | date: date_format }}</span>
    <h3>
      <a class="post-link" href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>
    </h3>
    {%- if site.show_excerpts -%}
      {{ post.excerpt }}
    {%- endif -%}
  </li>
  {%- endfor -%}
</ul>

<p class="image-gallery-index">
  {%- for post in site.categories['documentary'] -%}
    <a href="{{ post.url }}" title="{{ post.title }}">
      <img src="//images.weserv.nl/?url={{ site.url | replace: 'http://','' | replace: 'https://','' }}/uploads/documentary/{{post.photos_folder}}/{{ post.feature_image }}&w=300&h=300&output=jpg&q=50&t=square" />
      <span>{{ post.title | escape }}</span>
    </a>
  {%- endfor -%}
</p> 