---
title: "Cronicando"
layout: default
permalink: "/cronicando"
image: "/assets/images/screenshot.jpg"
comments: true
---

<div class="container">
    <div class="row justify-content-center">
        <!--  -->
        <div class="col-md-10" style="margin-top:50px">
        <h4 class="text-uppercase text-danger font-weight-bold">PASSEANDO</h4>
        </div>
        <div class="col-md-10">
        <p style="margin-bottom: 100px">
        Sem qualquer ordem cronol&oacute;gica. 
        Textos deixados por a&iacute; ao longo dos anos. 
        Como se fossem p&aacute;ginas&nbsp; do livro que n&atilde;o tenho tempo,
        nem paci&ecirc;ncia, nem temeridade para escrever.
        </p>
        <!--  -->
        <!--  -->
        {% for category in site.categories %}
        {% if category[0] == "cronicando" %}
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