---
layout: default
title: Publications by Authors
menu: bhq
---

## {{ page.title }}

<ul>
{% assign items_grouped = site.data.Authors | sort: 'AuthorLast' | group_by: 'AuthorLast' | sort: 'Title' %}
{%- for group in items_grouped -%}
{% assign type = group.items[0].Author | normalize_whitespace %}
<h3>{{ type }}</h3> 
<ul class="pubs">
{%- for item in group.items -%}
<li>
{% include pub-typeset.md %} 
</li>
{%- endfor -%}
</ul>
{%- endfor -%}