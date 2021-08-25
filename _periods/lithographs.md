---
title: Lithographs
layout: default
permalink: /lithographs/
dates: '1890 - 1894'
tag: 'lithographs'
preview: https://data.fitzmuseum.cam.ac.uk/imagestore/pdp/pdp82/P_438_1949_dc2.jpg
order: 8
---
Whistler took up lithography in 1878 with the encouragement of the London printer Thomas Way, and prompted by revived interest in the medium among French painters like Corot, Degas and Fantin-Latour. At first he drew directly onto lithographic printing stones, but he soon followed the example of his French colleagues by working on transfer paper, from which the image was transferred onto the stone. This gave the same freedom as making a drawing.

After a gap of eight years Whistler resumed making lithographs in 1887. Using subtle techniques and choice materials he created prints with the delicacy of drawings, leaving large borders around the figures so that the images seem to float. The sense of refinement and suggestion appealed to the French Symbolist poet Stéphane Mallarmé, who became friends with Whistler at this time.

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
