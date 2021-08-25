---
title: Later London Street Scenes
layout: default
permalink: /later-london-street-scenes/
dates: 'circa 1887'
tag: 'london street'
---
Whistler's late etching style was first developed in the mid-1880s on the streets in Chelsea, where he lived at a series of addresses until leaving London for Paris in 1892. Many of the prints show shop fronts and facades, with figures silhouetted in doorways and arches, recalling the figure subjects among Whistler's Venice etchings.

Whistler also ventured further afield, especially to the used clothing district around Houndsditch in the East End of London. He occasionally referred to the group of prints he made in the East End at this time as his 'East London Set', although they were never formally published as such.

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
