---
title: London and the Thames
layout: default
permalink: /london-and-the-thames/
dates: '1859-1879'
tag: london
preview: https://data.fitzmuseum.cam.ac.uk/imagestore/pdp/pdp33/preview_P_79_1959.jpg
order: 3
---
After returning to London from Paris in May 1859, Whistler took lodgings in Wapping and explored the area of warehouses and wharves along the Thames east of the City. Much of the architecture and character of the sites quickly changed with the demolition and rebuilding that took place in connection with the construction of the embankments.

When a selection of the prints was published as A Series of Sixteen Etchings of Scenes on the Thames and Other Subjects (known as 'The Thames Set') in 1871, the prints were recognised as a valuable record of an already vanishing London.

In Whistler's later Thames etchings linear description of detail gave way to evocation of the atmosphere resulting from increasing pollution and smog, leading him to experiment with different ways of printing half-tones.

<div class="container mb-3">
  <div class="row">
  {% assign rows =  site.posts.size | divided_by: 2.0 | ceil %}
  {% for i in (1..rows) %}
  {% assign offset = forloop.index0 | times: 2 %}
  {% assign sorted =  site.posts  | sort: "title"  %}

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
