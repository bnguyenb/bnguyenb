---
layout: page
menu: shouldbuy
title: Should Buy
permalink: /should-buy/
---

<ul class="post-list">
  {%- for post in site.categories['things'] -%}
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

<!-- Posts List with Sidebar (except featured)
================================================== -->
<section class="row">
  <div class="col-sm-9">
    <div class="row" id="items_container">
    123123
    </div>
    <!-- Pagination -->
    <div class="bottompagination">
      <span class="navigation" role="navigation">
        <nav class="pagination" role="pagination">
          <span class="page-number d-none"> &nbsp; &nbsp; Page 1 of 1 &nbsp; &nbsp; </span>
        </nav>
      </span>
    </div>
  </div>
  <div class="col-sm-3">
    
  </div>
</section>