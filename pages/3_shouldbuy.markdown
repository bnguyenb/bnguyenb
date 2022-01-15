---
# layout: page
# menu: shopping with me
# title: Sharing my shopping experiences
# permalink: /should-buy/
---

<section class="row">
  <div class="col-sm-9">
    <div class="row" id="items_container">
      {%- for post in site.categories['things'] -%}
        <div class="col-md-6 mb-5 item" data-parameterize="{{ post.parameterize }}" data-tags="">
          <!-- begin post -->
          <div class="card">
            <a target="_blank" href="<%= af.af_url%>">
              <img class="rounded mb-4" border="0" src="<%= af.item.image_url %>" />
            </a>
            <strong>{{ post.price }}</strong>
            <div class="card-block">
              <h2 class="card-title h4 serif-font">
              <a href="<%= af.item.item_details_url %>">{{ post.name }}</a>
              </h2>
              <p class="card-text text-muted">{{ post.description }}</p>
              <div class="metafooter">
                <div class="wrapfooter small d-flex align-items-center">
                  <span class="author-meta">
                    <a target="_blank" href="{{ post.af_url }}" class="btn btn-warning">Buy</a>
                  </span>
                  <div class="clearfix">
                    <a href="https://www.facebook.com/sharer/sharer.php?u={{ post.af_url }}" target="_blank">
                      <i class="fab fa-facebook fa-lg"></i>
                    </a>
                    <i class="fab fa-instagram fa-lg"></i>
                    <i class="fab fa-pinterest fa-lg"></i>
                    <i class="fas fa-at fa-lg"></i>
                  </div>
                </div>
              </div>
              <span class="card-text text-muted">
                <% af.item.tags.each do |t| %>
                  <%= link_to "##{t.name}", filter_by_tag_path(t.id, t.name) %>
                  <a href=""></a>
                <% end %>
                <% af.item.tags.map(&:name) %>
              </span>
            </div>
          </div>
          <!-- end post -->
        </div>
      {%- endfor -%}
    



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
</section>
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