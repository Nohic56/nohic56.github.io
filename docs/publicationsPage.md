---
layout: "page"
title: "Publications"
permalink: "Publications"
order: 5
---

{% assign dateActu = 0 %}
{% assign sorted = site.publications | sort: 'year' | reverse %}
{% for publication in sorted %}
  
  {% if  publication.year != dateActu %}
    {% assign dateActu = publication.year %}
    {% capture publication %}{{ publication.year }}{% endcapture %}

## {{ year }}

  {% endif %}

  {% capture titre %}{{ publication.titre }}{% endcapture %}
  {% capture auteurs %}{{ publication.auteurs }}{% endcapture %}
  {% capture DOI %}{{ publication.DOI }}{% endcapture %}
  {% capture journal %}{{ publication.journal }}{% endcapture %}
  {% capture PDF %}{{ publication.PDF }}{% endcapture %}
  {% include publication.html titre=titre auteurs=auteurs DOI=DOI journal=journal %}

  {% capture text-capture %}
    {{ publication.content }}
  {% endcapture %}

  {% capture toggleId %}toggleId{{ forloop.index }}{% endcapture %}

  {% include toggle.html toggle-text=text-capture toggleId=toggleId PDF=PDF %}

{% endfor %}
