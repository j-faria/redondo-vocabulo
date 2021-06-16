---
title: "Opinando"
layout: default
permalink: "/opinando"
---

<div class="container">
    <div class="row justify-content-center">
        <!--  -->
        <div class="col-md-10" style="margin-top:50px">
        <h4 class="text-uppercase text-danger font-weight-bold">OPINANDO</h4>
        </div>
        <div class="col-md-10">
        <p style="margin-bottom: 100px;">
        Opini&otilde;es sobre o dia a dia do Pa&iacute;s e do Mundo. 
        Escritas de resist&ecirc;ncia e de luta. 
        Ou, apenas, de reflex&atilde;o. Actualizado ao sabor da vontade e da disponibilidade.
        </p>
        <!--  -->
        <!--  -->
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