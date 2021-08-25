---
title: The Venice Sets
layout: default
permalink: /the-venice-sets/
dates: '1859-1879'
preview: https://data.fitzmuseum.cam.ac.uk/imagestore/pdp/pdp33/preview_P_2_2008.jpg
tag: venice
---
Following Whistler's bankruptcy in May 1879, the Fine Art Society commissioned him to go to Venice and return by December with a set of twelve prints. In the event his inspiration ran away with him and he did not return until November of 1880, bringing back many more plates.

Twelve were selected for publication as Venice, a Series of Twelve Etchings (known as 'The First Venice Set') and were exhibited at the Fine Art Society in December 1880. A larger exhibition was held in 1883, including the etchings later published in 1886 by Dowdeswells' as A Set of Twenty-Six Etchings (known as 'The Second Venice Set').

The printing of the edition of the Second Set was completed by July 1887, but the printing of the First Set was still not complete at the artist's death in 1903.


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
