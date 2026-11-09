---
title: "Sitemap"
permalink: /sitemap/
---

Every page on this site. For robots there is an [XML version](/sitemap.xml).

{% assign pages = site.pages | where_exp: "p", "p.title" | where_exp: "p", "p.sitemap != false" | sort: "url" -%}
{% for p in pages %}
  - [{{ p.title }}]({{ p.url | relative_url }})
{%- endfor %}
