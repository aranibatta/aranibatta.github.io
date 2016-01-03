---
layout: page
title: thoughts
permalink: /thoughts/
---

these are some ideas that I felt like sharing but weren't really cohesive enough to make concise points. if i do ever come to writing a full piece, they'll have found their foundatons here and posted on [medium.](https://www.medium.com/@aranibatta)
<div class="home">

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>

</div>
