---
layout: page
title:  　
tagline: Supporting tagline
---
{% include JB/setup %}


<div class="posts">
  <div class="post">
    <h1 class="post-title">
      <a href="{{ site.posts.first.url }}">
        {{ site.posts.first.title }}
      </a>
    </h1>

    <span class="post-date">{{ site.posts.first.date | date_to_string }}</span>

    {{ site.posts.first.content }}
  </div>
</div>


##Posts

<ul class="posts">
  {% for post in site.posts limit: 4 %}
    {% if site.posts.first != post %}
    <li><span>
      <h4>
        <a href="{{ post.url }}">{{ post.date | date_to_string }} &raquo; {{ post.title }}</a>
      </h4>
    </li>
    {% endif %}
  {% endfor %}

  <a href="/archive.html">more...</a>
</ul>
