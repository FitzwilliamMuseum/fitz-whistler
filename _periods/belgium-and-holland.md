---
title: Belgium and Holland
layout: default
permalink: /belgium-and-holland/
dates: '1887 - 1889'
tag: 'belgium and holland'
---
In August 1887 Whistler travelled to Belgium and Holland with his brother and sister-in-law. He took with him prepared plates and made nineteen etchings, thirteen of them in Brussels in September.

Whistler went back to Holland in 1889 and made a series of plates of Amsterdam. As ever, the view of a city viewed across water inspired him to new heights. He told the critic of the Pall Mall Gazette in 1890 that these etching combined the elaboration of his early Thames etchings with the Impressionism of his middle-period Venetian views.

<div class="container mb-3">
  <div class="row">
  {% assign rows =  site.posts.size | divided_by: 2.0 | ceil %}
  {% for i in (1..rows) %}
  {% assign offset = forloop.index0 | times: 2 %}
  {% assign sorted =  site.posts  %}

      {% for author in sorted limit:2 offset:offset %}

      {% if author.tags contains page.tag %}
      <div class="col-md-4 mb-3">
        <div class="card h-100" >
          <a href="{{site.baseurl}}{{ author.permalink }}" class="stretched-link">
            <img class="card-img-top square" src="{{author.preview}}" alt="Card image cap" width="300" height="300"/>
          </a>
          <div class="card-body">
            <h3 class="lead mt-2">
              <a href="{{site.baseurl}}{{ author.permalink }}" class="stretched-link">{{author.title}}</a>
            </h3>
            {% for tag in author.tags %}
            <span class="badge badge-dark badge-large p-2 mb-2 mr-2 ">
              <a href="" class="text-white"><i class="fas fa-tags"></i> {{ tag | capitalize }}</a>
            </span>
            {% endfor %}
          </div>
        </div>
      </div>
      {% endif %}
      {% endfor %}
    {% endfor %}


  </div>
</div>
