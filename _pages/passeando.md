---
title: "Passeando"
layout: default
permalink: "/passeando"
pagination: 
  enabled: true
  category: Passeando
---

<div class="container">
    <div class="row justify-content-center">
        <!--  -->
        <div class="col-md-10" style="margin-top:50px">
            <h4 class="text-uppercase text-danger font-weight-bold">PASSEANDO</h4>
        </div>
        <div class="col-md-10">
            <p style="margin-bottom: 100px">
            Viajar em Portugal. 
            Comidas e dormidas com a cadeira de rodas do meu companheiro como guia.
            </p>
            <!--  -->
            {% for post in paginator.posts %}
                {% include main-loop-card.html %}
            {% endfor %}
        </div>
    </div>
</div>