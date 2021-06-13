---
title: "Passeando"
layout: default
permalink: "/passeando"
comments: true
---

<div class="container">
    <div class="row justify-content-center">
        <div class="col-md-10">
            <h4 class="font-weight-bold spanborder text-capitalize" id="passeando">
            <span>Passeando</span>
            </h4>
        <!--  -->
        <p>
        Viajar em Portugal. Comidas e dormidas com a cadeira de rodas do meu companheiro como guia..
        </p>
        <!--  -->
        <!-- <h1 class="font-weight-bold title h6 text-uppercase mb-4">Categories</h1> -->
        {% for category in site.categories %}
        {% if category[0] == "Passeando" %}
        <!--  -->
        {% assign pages_list = category[1] %}
        <!--  -->
        {% for post in pages_list %}
            {% if post.title != null %}
                {% if group == null or group == post.group %}
                    {% include main-loop-card.html %}
                {% endif %}
            {% endif %}
        {% endfor %}
        {% assign pages_list = nil %}
        {% assign group = nil %}
        {% endif %}
        {% endfor %}

        </div>
        
        
    </div>
</div>