---
layout: page
title: Posts
permalink: /posts/
---
<div class="post">
    {% for post in site.posts %}
        <div class="container">
            <h3>{{post.title}}</h3>
            <h5>
                {% for category in post.categories %}
                    {{category}}
                {% endfor %}
            </h5>
            {{ post.description | html_safe | markdownify }}
            <br/>
            <a href="{{post.url}}">Continue reading...</a>
        </div>
        <br/>
        <hr/>
    {% endfor %}
</div>

<style>
    .post-header {
        display: none;
    }
</style>