---
layout: page
permalink: /publications/
title: publications
description: publications by categories in reversed chronological order. generated by jekyll-scholar.
nav: false
# nav_order: 2

toc:
  sidebar: right
---

<div class="publications">

Total number of pubblication {% bibliography_count %}.

Total number of pubblication with tags {% bibliography_count --query @*[keywords] %}.

Total number of pubblication with pippo tags {% bibliography_count --query @*[keywords ~= pippo] %}.

## test

{% for keyword in site.data.bibkeywords.bibkeywords %}

  <h1>{{ keyword }}</h1>
    Total number of pubblication with {{ keyword | toc  }} tags {% bibliography_count --query @*[keywords ~= {{ keyword }} ] %}.
    {% bibliography --query @*[keywords ~= {{ keyword }} ] %}
{% endfor %}

<h1>The rest</h1>
{% bibliography %}

</div>
