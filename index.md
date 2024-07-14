---
title: "Einträge"
layout: archive
author_profile: true
---
{% for collection in site.collections %}
  {% capture label %}{{ collection.label }}{% endcapture %}
  {% if label != written_label %}
    {% capture written_label %}{{ label }}{% endcapture %}
   {% endif %}
  {% for post in collection.docs %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}