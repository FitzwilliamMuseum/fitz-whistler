---
title: The French Set
layout: default
permalink: /the-french-set/
dates: '1857-1861'
preview: https://data.fitzmuseum.cam.ac.uk/imagestore/pdp/pdp20/preview_P_273_1954.jpg
tag: french
---

Whistler took up etching seriously in London in the spring of 1858. After returning to Paris he made numerous prints in the city and on a journey to the river Rhine. In October 1858 a number of trial proofs were printed on the press of the leading Parisian printer Auguste Delâtre, from which Whistler selected twelve (plus title-page) to be published as Twelve etchings after Nature.

They include domestic and genre scenes, studies of friends or their children, and glimpses of shadowy figures in backstreets, alleyways and anonymous interiors. Whistler referred to the series as his 'French Set', although not all the subjects are French. Choice of subjects and treatment reflected Whistler's awareness of modern realist trends in French art.

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
