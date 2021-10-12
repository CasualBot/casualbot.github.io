---
layout: page
title: Projects
permalink: /projects/
---
<div class="card-container">
{% for project in site.projects %}
<div class="card" style="background-color:#{{project.card-color}}">
    {% if project.image_url %}
        <img class="card-img" src="{{ project.image_url }}" alt="Project Image"  />
    {% else %}
        <div class="card-img">    </div>
    {% endif %}
    <div class="container">
        {% if project.hyperlink %}
            <h3 class="title"><a href="{{project.url}}">{{ project.title }}</a></h3>
        {% else %}
            <h3 class="title">{{ project.title }}</h3>
        {% endif %} 
        {% if project.description %}
            <h5 class="description">{{ project.description }}</h5>
        {% endif %}
    </div>
  <!-- <p>{{ proj.content | markdownify }}</p> -->
</div>
{% endfor %}
</div>
<style>
.card-container {
    display: flex;
    width: 100%;
    flex-direction: row;
    flex-wrap: wrap;
}
.card {
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    transition: 0.3s;
    width: 30%;
    display: flex;
    flex-direction: column;
    justify-content: left;
    margin: 15px;
}
.card:hover {
    outline: 1px solid #800000;
}
.container {
    background-color: #fdfdfd;
}
.card:hover {
    box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}
.container {
    padding: 2px 16px;
    height: 20%;
    min-height: 20%;
    border-top: 1px solid #414a4c;
}
.card-img {
    max-height: 80%;
    height: 100%;
    justify-content: center;
    vertical-align: middle;
    object-fit: cover;
}
.fill {
    width:100% !important;
}
.page-content > .wrapper {
    max-width: calc(1200px - (30px * 2)) !important;   
}
</style>