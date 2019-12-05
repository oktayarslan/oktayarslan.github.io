---
title: "Blog"
layout: single
permalink: /blog/
author_profile: true
redirect_from:
  - /blog
excerpt:
share: false
---

<div class="home">
  
  <ul class="post">
    {% for post in site.posts %}
      <li>
        <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        <br>
        {{ post.excerpt }}
      </li>
    {% endfor %}
  </ul>

</div>
