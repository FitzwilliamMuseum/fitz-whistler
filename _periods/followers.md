---
title: Prints by friends and followers

layout: default
permalink: /friends-and-followers/
dates: '1861 - 1889'
tag: 'followers'
---
Whistler attracted a number of pupils and followers, both amateur and professional, a number of whom became significant printmakers in their own right. Mortimer Menpes and Walter Sickert absorbed Whistler's methods while helping with the printing of the 'Second Venice Set'.

As in so many other cases, Whistler later fell out with both of them. Théodore Roussel seems to have been more subservient: out of respect he always removed his hat in Whistler's presence.

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
