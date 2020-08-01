---
title: "Active Touch Lab - Research"
layout: textlay
excerpt: "Actice Touch Lab: Research"
sitemap: false
permalink: /research/
tweets: https://twitter.com/ShefTouch
---

# Research


{% for tweet in page.tweets %}
  {% twitter tweet align=right width=350 %}
{% endfor %}

{% twitter page.a_tweet %}
