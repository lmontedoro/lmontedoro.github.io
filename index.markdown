---
layout: page
title: My Blog
header: Blog Post
---

<div class="home">
  {% assign posts = site.posts %}
  {%- if posts.size > 0 -%}

  <ul class="post-list">
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}

    {%- for post in posts -%}
    <li>
      <h2>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h2>
      <span class="post-meta">{{ post.date | date: date_format }}</span>
      
      {%- if site.show_excerpts -%}
        {{ post.excerpt }}
      {%- endif -%}
    </li>
    {%- endfor -%}

  </ul>
{%- endif -%}

</div>