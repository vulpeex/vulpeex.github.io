---
layout: page
title: Blog Archive
---
<link href="/css/archive.css" rel="stylesheet" type="text/css">

<div class="archive-container">
  {% for tag in site.tags %}
    <div class="archive-section">
      <h3 class="tag-title">{{ tag[0] | capitalize }}</h3>
      <ul class="archive-posts-list">
        {% for post in tag[1] %}
          <li class="archive-post-item">
            <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span><br>
            <a href="{{ post.url }}" class="post-title">{{ post.title }}</a>
          </li>
          <hr class="div-rule">
        {% endfor %}
      </ul>
    </div>
  {% endfor %}
</div>