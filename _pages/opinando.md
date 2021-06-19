---
title: "Opinando"
layout: default
permalink: "/opinando"
pagination: 
  enabled: true
  category: Opinando
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
        {% for post in paginator.posts %}
            {% include main-loop-card.html %}
        {% endfor %}
        </div>
    </div>
</div>