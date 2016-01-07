---
layout: page
title: thoughts
permalink: /thoughts/
---

these are some ideas that I felt like sharing but weren't really cohesive enough to make concise points. if i do ever come to writing a full piece, they'll have found their foundatons here and posted on [medium](https://www.medium.com/@aranibatta). i'll write about anything tech, connecting dots about pretty much anything, and random stastics. all the statistics.
<td>
            <h2>Posts</h2>
            <div id="tags">
                Tags:
                {% comment %} Based on code from Christian Specht at http://stackoverflow.com/a/24744306/2712951 {% endcomment %}
                {% capture tags %}{% for tag in site.tags %}{{ tag[1].size | plus: 10000 }}{{ tag[1].first.date | date: "%Y%m%d" }}#{{ tag[0] }}#{{ tag[1].size }}{% unless forloop.last %}|{% endunless %}{% endfor %}{% endcapture %}
                {% assign sorted = tags | split: "|" | sort | reverse %}
                {% for tag in sorted %}
                    {% assign items = tag | split: "#" %}
                    <span data-tag="{{ items[1] }}" class="tag">{{ items[1] | replace: " ", "&nbsp;" }}&nbsp;<span class="subtitle">({{ items[2] }})</span></span>
                {% endfor %}
            </div>
            <ul id="post-list" class="work-list">
                {% for post in site.posts %}
                    <li data-tags="{{ post.tags | join: "|" }}">{{ post.date | date: "%b %-d, %Y" }}: <a class="underlined" href="{{ post.url }}">{{ post.title }}</a><br /><span class="subtitle">{{ post.description }}<br />{{ post.tags | join: ", " }} &middot; {% if post.draft %}<span class="draft">Draft</span>{% else %}<a href="{{ post.url }}#disqus_thread" data-disqus-identifier="{{ post.id }}"></a>{% endif %}</span></li>
                {% endfor %}
                <li id="null-post" data-tags="" style="display: none;"><i>No posts with these tags</i></li>
            </ul>
        </td>


<script id="dsq-count-scr" src="//arani.disqus.com/count.js" async></script>