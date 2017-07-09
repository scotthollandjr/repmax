---
layout: page
title: Blog
permalink: /blog/
---

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <div class="post-image">
        <img src="{{ post.image }}">
      </div>
      <div class="post-content">
        <div class="col-one">
          <h1 class="post-title">
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
          </h1>
          {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
          <span class="post-date">{{ post.date | date: date_format }}</span>
        </div>
        <div class="col-two">
          <p>{{ post.preview }}</p>
        </div>
      </div>
    </li>
  {% endfor %}
</ul>

<!-- <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p> -->
