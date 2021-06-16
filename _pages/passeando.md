---
title: "Passeando"
layout: default
permalink: "/passeando"
---

<div class="container">
    <div class="row justify-content-center">
        <!--  -->
        <div class="col-md-10" style="margin-top:50px">
        <h4 class="text-uppercase text-danger font-weight-bold">PASSEANDO</h4>
        </div>
        <div class="col-md-10">
        <p style="margin-bottom: 100px">
        Viajar em Portugal. Comidas e dormidas com a cadeira de rodas do meu companheiro como guia..
        </p>
        <!--  -->
        <!--  -->
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