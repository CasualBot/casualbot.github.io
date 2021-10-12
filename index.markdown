---
layout: page
---
<div>
    <h1>Hi! I'm <span style="color:#a00000;">Shawn.</span></h1>
    <h4>I make things on the internet from time to time!</h4> 
    <p>My background is in web development, primarily eCommerce, but thanks to my ADD I have learned many different things.</p>
    <p>I'm making this simply as a way to showcase some of the things I've used my technical knowledge and skills to do, learn, and grow with.</p>
    <p>I even made this site you're seeing now!</p>
    <br/>
    <img src="/assets/img/headshot.png" alt="me" width="600" style="margin-left: 20px; padding: 20px; border: 1px solid #a00000; border-radius: 0;"/>
</div>
<hr/>
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
        <hr style="color:#800;"/>
    {% endfor %}
</div>
<style>
    .post-title { display: none; }
    .footer-col-1 { display: none; }
</style>
