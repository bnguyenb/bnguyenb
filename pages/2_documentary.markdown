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

<p class="image-gallery-index">
  {%- for post in site.categories['documentary'] -%}
    <a href="{{ post.url }}" title="{{ post.title }}">
      <img src="//images.weserv.nl/?url={{ site.url | replace: 'http://','' | replace: 'https://','' }}/uploads/documentary/{{post.photos_folder}}/{{ post.feature_image }}&w=300&h=300&output=jpg&q=50&t=square" />
      <span>{{ post.title | escape }}</span>
    </a>
  {%- endfor -%}
</p> 