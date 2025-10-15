---
layout: default
title: Blog
---

<div class="container">
    <h1>Blog</h1>
    
    <div class="post-list">
        {% for post in site.posts %}
        <article class="post-preview">
            <h2>
                <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            </h2>
            <time datetime="{{ post.date | date_to_xmlschema }}">
                {{ post.date | date: "%B %d, %Y" }}
            </time>
            <p>{{ post.excerpt }}</p>
            <a href="{{ post.url | relative_url }}" class="read-more">Read more →</a>
        </article>
        {% endfor %}
    </div>
</div>
