---
layout: "page"
title: "Communications"
permalink: "Communications"
order: 6
---

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
  {% capture Type %}{{ com.Type }}{% endcapture %}
  {% capture Conf %}{{ com.Conf }}{% endcapture %}
  {% include com.html titre=titre auteurs=auteurs Type=Type Conf=Conf %}

  {% capture text-capture %}
    {{ com.content }}
  {% endcapture %}

  {% capture toggleId %}toggleId{{ forloop.index }}{% endcapture %}

  {% include toggle.html toggle-text=text-capture toggleId=toggleId PDF=PDF %}

{% endfor %}
