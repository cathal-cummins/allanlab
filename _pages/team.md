---
title: "Active Touch Lab - Team"
layout: gridlay
excerpt: "Active Touch Lab: Team members"
sitemap: false
permalink: /team/
---

# Group Members

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/team/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.status }}</i><br>
  Email:<i> <{{ member.email }}></i><br>

  {%- if member.uni-website -%}
  <a href="{{ member.uni-website }}" title="University Website">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1em">
      <i class="fas fa-circle fa-stack-2x"></i>
      <i class="fa fa-university fa-stack-1x fa-inverse"></i>
    </span>
    <span class="sr-only">University Website</span>
  </a>
  {%- endif -%}

  {%- if member.twitter -%}
  <a href="https://twitter.com/{{ member.twitter }}" title="Twitter">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1em">
      <i class="fas fa-circle fa-stack-2x"></i>
      <i class="fab fa-twitter fa-stack-1x fa-inverse"></i>
    </span>
    <span class="sr-only">Twitter</span>
  </a>
  {%- endif -%}

  {%- if member.github -%}
  <a href="https://github.com/{{ member.github }}" title="Github">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1em">
      <i class="fas fa-circle fa-stack-2x"></i>
      <i class="fab fa-github fa-stack-1x fa-inverse"></i>
    </span>
    <span class="sr-only">Github</span>
  </a>
  {%- endif -%}

  {%- if member.gscholar -%}
  <a href="https://scholar.google.com/citations?user={{ member.gscholar }}" title="GScholar">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1em">
      <i class="fas fa-circle fa-stack-2x"></i>
      <i class="fa fa-graduation-cap fa-stack-1x fa-inverse"></i>
    </span>
    <span class="sr-only">GScholar</span>
  </a>
  {%- endif -%}

  {%- if member.orcid -%}
  <a href="https://orcid.org/{{ member.orcid }}" title="Orcid">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1em">
      <i class="fas fa-circle fa-stack-2x"></i>
      <i class="fab fa-orcid fa-stack-1x fa-inverse"></i>
    </span>
    <span class="sr-only">Orcid</span>
  </a>
  {%- endif -%}
  <br>
  <p>{{ member.description }}</p>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


## Associate members

{% assign number_printed = 0 %}
{% for member in site.data.associate_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/team/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.status }}</i><br>
  Email:<i> <{{ member.email }}></i><br>

  {%- if member.uni-website -%}
  <a href="{{ member.uni-website }}" title="University Website">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1em">
      <i class="fas fa-circle fa-stack-2x"></i>
      <i class="fa fa-university fa-stack-1x fa-inverse"></i>
    </span>
    <span class="sr-only">University Website</span>
  </a>
  {%- endif -%}

  {%- if member.twitter -%}
  <a href="https://twitter.com/{{ member.twitter }}" title="Twitter">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1em">
      <i class="fas fa-circle fa-stack-2x"></i>
      <i class="fab fa-twitter fa-stack-1x fa-inverse"></i>
    </span>
    <span class="sr-only">Twitter</span>
  </a>
  {%- endif -%}

  {%- if member.github -%}
  <a href="https://github.com/{{ member.github }}" title="Github">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1em">
      <i class="fas fa-circle fa-stack-2x"></i>
      <i class="fab fa-github fa-stack-1x fa-inverse"></i>
    </span>
    <span class="sr-only">Github</span>
  </a>
  {%- endif -%}

  {%- if member.gscholar -%}
  <a href="https://scholar.google.com/citations?user={{ member.gscholar }}" title="GScholar">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1em">
      <i class="fas fa-circle fa-stack-2x"></i>
      <i class="fa fa-graduation-cap fa-stack-1x fa-inverse"></i>
    </span>
    <span class="sr-only">GScholar</span>
  </a>
  {%- endif -%}

  {%- if member.orcid -%}
  <a href="https://orcid.org/{{ member.orcid }}" title="Orcid">
    <span class="fa-stack fa-lg" aria-hidden="true" style="font-size: 1em">
      <i class="fas fa-circle fa-stack-2x"></i>
      <i class="fab fa-orcid fa-stack-1x fa-inverse"></i>
    </span>
    <span class="sr-only">Orcid</span>
  </a>
  {%- endif -%}
  <br>
  <p>{{ member.description }}</p>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Alumni

{% for member in site.data.alumni_members %} {{ member.name }} <br /> {% endfor %}
