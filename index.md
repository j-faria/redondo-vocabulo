---
title: Um Redondo Vocábulo
layout: default
pagination:
  enabled: true
description:
---


<div class="container">
    <div class="row remove-site-content-margin">
    <div class="col-md-12">
        <div class="card border-0 mb-4 box-shadow">   
            <div class="topfirstimage" 
            style="background-image: url(/assets/images/blog.jpg); height: 250px; background-size: cover; background-repeat:no-repeat;">
            </div>     
        <div class="card-body px-0 pb-0 d-flex flex-column align-items-start">
            <h2 class="h4 font-weight-bold">Seja bem vindo quem vier por bem</h2>
            <p>
                Tentativa de voltar às origens para contrariar o frenesim da
                escrita a correr, sobre tudo e sobre nada. 
                <!--  -->
                Recolha de textos antigos, deixados por aí.
                Opiniões. Viagens. 
                <!--  -->
                Este sitio é, sobretudo, uma sequência de "Momentos".
                <!--  -->
                Um sitio de Esquerda. Feito da margem Esquerda da
                vida e da politica. Com hesitações e com dúvidas, seguramente. 
                Mas sem concessões.
            </p>
            <p>Bem vindos... quem vier por bem!</p>
        </div>
    </div>
    </div>
    </div>
    <!--  -->
    <div class="row mt-3">
        <div class="col-md-8 main-loop">
            <h4 class="font-weight-bold spanborder"><span>Todas as Histórias</span></h4>
            <!--  -->
            <!-- List of posts -->
            {% for post in paginator.posts %}
                {% if post.categories contains "Lendo" %}
                    {% linkpreview {{post.link}} %}
                    <br>
                {% else %}
                    {% include main-loop-card.html %}
                {% endif %}
            {% endfor %}
            <!--  -->
            <!-- Pagination links -->
            <div class="mt-5">
                {% if paginator.total_pages > 1 %}
                <ul class="pagination"> 
                    {% if paginator.previous_page %}
                        {% assign href = paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' %}
                        <li class="page-item"><a class="page-link" href="{{ href }}">&laquo; Prev</a></li>
                    {% else %}
                        <!-- <li class="page-item disabled"><span class="prev page-link">&laquo;</span></li> -->
                    {% endif %}
                    <!--  -->
                    {% for page in (1..paginator.total_pages) %}
                        {% if page == paginator.page %}
                            <li class="page-item disabled"><span class="webjeda page-link">{{ page }}</span></li>
                        {% elsif page == 1 %}
                            <li class="page-item"><a class="page-link" href="{{site.baseurl}}/">{{ page }}</a></li>
                        {% else %}
                            {% assign href = site.paginate_path | prepend: site.baseurl | replace: '//', '/' | replace: ':num', page %}
                            <li class="page-item"><a class="page-link" href="{{ href }}">{{ page }}</a></li>
                        {% endif %}
                    {% endfor %}
                    <!--  -->
                    {% if paginator.next_page %}
                        {% assign href = paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' %}
                        <li class="page-item"><a class="page-link" href="{{ href }}">Next &raquo;</a></li>
                    {% else %}
                        <!-- <li class="page-item disabled"><span class="next page-link">&raquo;</span></li> -->
                    {% endif %}
                </ul>
                {% endif %}      
            </div>
        </div>
        <!--  -->
        <!-- Temas -->
        <div class="col-md-4">
            {% include sidebar-destaque.html %}    
        </div>
    </div>


</div>