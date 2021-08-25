---
title: Family and Friends
layout: default
permalink: /family-and-friends/
dates: '1857-1894'
preview: https://data.fitzmuseum.cam.ac.uk/imagestore/pdp/pdp20/preview_P_2071_R.jpg
tag: family
order: 1
---
Many of Whistler's figure subjects portrayed his immediate circle of family, friends and acquaintances, from his mistress Fumette in Paris in the 1850s, to his wife Beatrice and her sister 'Bunnie' in the 1890s.

One of the largest and earliest groups featured the family of his half-sister Deborah and her husband, the surgeon, etcher and collector Seymour Haden, who became an influential figure in the revival of etching in England. The relationship between Whistler and Haden quickly deteriorated. Whistler grew jealous of the public success of Haden's landscape prints, while Haden was outraged by Whistler's lifestyle (living openly with his new mistress).

Whistler's relationships with numerous other people suffered the same fate. When he turned his scathing wit on former friends his butterfly monogram acquired a barbed tail to match the sting of his wit.

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
