---
layout: "page"
title: "Communications"
permalink: "Communications"
order: 6
---
{% if site.coms %}
{% assign dateActu = 0 %}
{% assign sorted = site.coms | sort: 'annee' | reverse %}
{% for com in sorted %}
  
  {% if  com.annee != dateActu %}
    {% assign dateActu = com.annee %}
    {% capture annee %}{{ com.annee }}{% endcapture %}

## {{ annee }}

  {% endif %}

  {% capture titre %}{{ com.titre }}{% endcapture %}
  {% capture auteurs %}{{ com.auteurs }}{% endcapture %}
  {% capture type %}{{ com.type }}{% endcapture %}
  {% capture conf %}{{ com.conf }}{% endcapture %}
  {% include com.html titre=titre auteurs=auteurs type=type conf=conf %}

  {% capture text-capture %}
    {{ com.content }}
  {% endcapture %}

  {% capture toggleId %}toggleId{{ forloop.index }}{% endcapture %}

  {% include toggle.html toggle-text=text-capture toggleId=toggleId PDF=PDF %}

{% endfor %}
{% else %}
  <!-- Handle case where site.coms is null or empty -->
{% endif %}
