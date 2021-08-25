---
title: The Honeymoon Tour
layout: default
permalink: /the-honeymoon-tour/
dates: '1888'
tag: 'honeymoon'
---
After marrying Beatrice Godwin on 11 August 1888, Whistler set off on his honeymoon to the chateaux of the Loire and the towns of Touraine, taking with him 34 prepared plates. In most of the etchings that he made during the trip, he avoided the obvious tourist sites, and concentrated on picturesque settings rather than figures, much as he had done in Venice, London and Brussels.

He generally referred to the etchings of this tour as his 'Renaissance lot' because of the details of French Renaissance architecture that caught his eye, but the etchings were never published as a set. Relatively few impressions were printed, the first of them sent to the Fine Art Society on 27 March 1889.

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
