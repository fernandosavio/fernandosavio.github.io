---
layout: tags
title: Tag Archive
description: "Artigos categorizados por suas tags."
permalink: /tags.html
---

{% capture site_tags %}{% for tag in site.tags %}{{ tag | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
{% assign tags_list = site_tags | split:',' | sort %}

<div>
  <strong>Tags</strong>:
  {% for item in (0..site.tags.size) %}
    {% unless forloop.last %}
      {% capture this_word %}{{ tags_list[item] | strip_newlines }}{% endcapture %}
        <a href="#{{ this_word }}" style="margin: 5px;">#{{ this_word }} [{{ site.tags[this_word].size }}]</a>
    {% endunless %}
  {% endfor %}
</div>

{% for item in (0..site.tags.size) %}
  {% unless forloop.last %}
    {% capture this_word %}{{ tags_list[item] | strip_newlines }}{% endcapture %}
<h2 id="{{ this_word }}" class="tag-heading">#{{ this_word }}</h2>
<ul class="post-list">
  {% for post in site.tags[this_word] %}
    {% if post.title != null %}
      <li>
        <article>
          <time class="post-date" datetime="{{ post.date }}">{{ post.date | date: '%d/%m/%Y' }}</time>
          <h2>
            <a href="{{ site.url }}{{ post.url }}" class="post-title">{{ post.title | markdownify | remove: "<p>" | remove: "</p>" }}</a>
          </h2>
          <p class="post-excerpt">{{ post.excerpt | strip_html }}</p>
          <div>
            {% for tag in post.tags %}
                <a href="#">#{{ tag }}</a>
            {% endfor %}
          </div>
        </article>
      </li>
    {% endif %}
  {% endfor %}
</ul>
  {% endunless %}
{% endfor %}
