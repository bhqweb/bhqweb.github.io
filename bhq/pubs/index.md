---
layout: default
title: Publications
menu: bhq
epuburl: https://www.lulu.com
---

## {{ page.title }}


{% include book-order-info.md %} 

<ul>
{% assign items_grouped = site.data.Books | group_by: 'Type' %}
{%- for group in items_grouped -%}
{% assign type = group.items[1].Type | strip_newlines | normalize_whitespace %}
<h3>{{ type }}</h3> 
<ul class="pubs">
{%- for item in group.items -%}
<li>
{% include pub-typeset.md %} 
</li>
{%- endfor -%}
</ul>
{%- endfor -%}