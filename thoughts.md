---
layout: page
title: thoughts
permalink: /thoughts/
---

these are some ideas that I felt like sharing but weren't really cohesive enough to make concise points. if i do ever come to writing a full piece, they'll have found their foundatons here and posted on [medium](https://www.medium.com/@aranibatta). i'll write about anything tech, connecting dots about pretty much anything, and random stastics. all the statistics.
<div class="home">

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
		  <font size=".01"><a class="post-link" href="{{ post.url }}#disqus_thread" data-disqus-identifier="{{ post.id }}"></a></font>
        </h2>
      </li>
    {% endfor %}
  </ul>

</div>


<script id="dsq-count-scr" src="//arani.disqus.com/count.js" async></script>