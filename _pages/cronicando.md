---
title: "Cronicando"
layout: default
permalink: "/cronicando"
pagination: 
  enabled: true
  category: Cronicando
---

<div class="container">
    <div class="row justify-content-center">
        <!--  -->
        <div class="col-md-10" style="margin-top:50px">
        <h4 class="text-uppercase text-danger font-weight-bold">CRONICANDO</h4>
        </div>
        <div class="col-md-10">
        <p style="margin-bottom: 100px">
        Sem qualquer ordem cronol&oacute;gica. 
        Textos deixados por a&iacute; ao longo dos anos. 
        Como se fossem p&aacute;ginas&nbsp; do livro que n&atilde;o tenho tempo,
        nem paci&ecirc;ncia, nem temeridade para escrever.
        </p>
        <!--  -->
        {% for post in paginator.posts %}
            {% include main-loop-card.html %}
        {% endfor %}
        </div>
    </div>
</div>