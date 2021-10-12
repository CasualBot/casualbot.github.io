---
layout: page
title: Projects
permalink: /projects/
---
{% for project in site.projects %}
<div class="card" style="background-color:#{{project.card-color}}">
    {% if project.image_url %}
        <img class="card-img" src="{{ project.image_url }}" alt="Project Image"  />
    {% endif %}
    <div class="container">
        {% if project.hyperlink %}
            <h3 class="title"><a href="{{project.hyperlink}}" target="_blank">{{ project.title }}</a></h3>
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
<style>
.card {
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    transition: 0.3s;
    width: 250px;
    display: flex;
    flex-direction: column;
    justify-content: left;
}

.container {
    background-color: #fdfdfd;
}
.card:hover {
    box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}
.container {
    padding: 2px 16px;
    height: 25%;
    border-top: 1px solid #414a4c;

}
.card-img {
    max-height: 80%;
    height: 80%;
    margin-bottom: 10px;
    margin-top: 10px;
    justify-content: center;
    vertical-align: middle;
}
.fill {
    width:100% !important
}
</style>