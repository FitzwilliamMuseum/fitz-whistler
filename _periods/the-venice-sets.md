---
title: The Venice Sets
layout: default
permalink: /the-venice-sets/
dates: '1859-1879'
preview: https://data.fitzmuseum.cam.ac.uk/imagestore/pdp/pdp33/preview_P_2_2008.jpg
tag: venice
order: 4
---
Following Whistler's bankruptcy in May 1879, the Fine Art Society commissioned him to go to Venice and return by December with a set of twelve prints. In the event his inspiration ran away with him and he did not return until November of 1880, bringing back many more plates.

Twelve were selected for publication as Venice, a Series of Twelve Etchings (known as 'The First Venice Set') and were exhibited at the Fine Art Society in December 1880. A larger exhibition was held in 1883, including the etchings later published in 1886 by Dowdeswells' as A Set of Twenty-Six Etchings (known as 'The Second Venice Set').

The printing of the edition of the Second Set was completed by July 1887, but the printing of the First Set was still not complete at the artist's death in 1903.


### Etchings & Dry Points.

**Venice Second Series, London 1883, 1st & 2nd editions**

Whistler called his second exhibition of Venetian prints at the Fine Art Society in 1883, an 'Arrangement in White and Yellow'. It was 'Sparkling and dainty-and all so sharp-White walls of different whites, with painted mouldings-not gilded!-yellow velvet curtains-pale yellow matting-yellow sofas and little chairs-lovely little table yellow-own design-with yellow pot and Tiger Lily!... etchings in their exquisite white frames-with their little butterflies-large white butterfly on yellow curtains and yellow butterfly on white wall-and [a] servant in yellow livery' to hand out this catalogue. He gave his allies yellow butterflies 'to wear defiantly with the brave and beautiful on the great day'. For the catalogue, he culled quotes from previous criticism of his work, adding his own marginal glosses to hold his critics up to ridicule.

The three Venetian prints included in this exhibition were accompanied by the following quotes:

**The Beggars**

> "In the character of humanity he has not time to be interested." - Standard
"General absence of tone" - P. G. Hamerton

**The Doorway**

>"'There is seldom in his Etchings any large arrangement of light and shade." - P. G. Hamerton
"Short, scratchy lines." - St. James's Gazette
"The architectural ornaments and the interlacing bars of the gratings are suggested rather than drawn." - St. James's Gazette
"Amateur prodige" - Saturday Review

**Long Lagoon**

>"We think that London fogs and the muddy old Thames supply Mr Whistler's needle with subjects more congenial than do the Venetian palaces and lagoons" - Daily News


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
