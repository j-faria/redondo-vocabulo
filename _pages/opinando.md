---
title: "Opinando"
layout: default
permalink: "/opinando"
---

<div class="container">
    <div class="row justify-content-center">
        <div class="col-md-10">
        <!-- <h1 class="font-weight-bold title h6 text-uppercase mb-4">Categories</h1> -->
        <h4 class="font-weight-bold spanborder text-capitalize" id="opinando">
            <span>Opinando</span>
        </h4>
        <p>
        Opini&otilde;es sobre o dia a dia do Pa&iacute;s e do Mundo. 
        Escritas de resist&ecirc;ncia e de luta. 
        Ou, apenas, de reflex&atilde;o. Actualizado ao sabor da vontade e da disponibilidade.
        </p>

        {% for category in site.categories %}
        {% if category[0] == "Opinando" %}

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