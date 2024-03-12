---
layout: page
title: Poems, Creative Writing and Such.
menu_title: Poetry
permalink: /poetry/
description: 'Poems inspired and born from the heart, spirit and soul of Portland artist, Uri Frazier.'
---

{%- if site.posts.size > 0 -%}

<ul class="post-list"  markdown=1>
    {%- for post in site.categories.poem -%}
    <li class="post-preview">
    {%- if post.thumbnail -%}
        <span class="thumbnail_url hidden">{{site.url}}/{{site.images_path}}{{post.thumbnail}}</span>
        <span class="thumbnail_alt hidden">{{post.thumbnail_alt}}</span>
    {%- endif -%}     
        <div class="post-preview-text">
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <span class="post-meta">{{ post.date | date: date_format }}</span>
        <h3>
            <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
            </a>
        </h3>
        {%- if site.show_excerpts -%}
            <p>{{ post.excerpt | strip_html | truncate: 156 }}</p>
        {%- endif -%}
        </div>
    </li>
    {%- endfor -%}
</ul>

<!-- <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p> -->
{%- endif -%}