---
layout: default
title: Forum 2012 - 2020
menu: bhq
---

## {{ page.title }}

{% assign items_grouped = site.data.forum81plus | group_by: 'Vol' %}
{%- for group in items_grouped -%}
{% assign vol = group.items[1].Vol | strip_newlines | normalize_whitespace %}
{% assign year = group.items[1].Year | strip_newlines | normalize_whitespace %}
{% assign month = group.items[1].Month | strip_newlines | normalize_whitespace %}
### Forum {{ vol }} &mdash; {% include month.md %} {{ year }} 
<ul>
{%- for item in group.items -%}
<li> <span class="title">{{ item.Title | normalize_whitespace | strip_newlines }}</span>
{% assign test1 = item.SubTitle | strip_newlines %}
{%- if test1 != "" -%}<span class="subTitle"> &mdash; {{- item.SubTitle | strip_newlines | normalize_whitespace -}}</span> {%- endif -%}
{%- assign test2 = item.Author | strip_newlines -%}{%- if test2 != "" -%}
<span class="author">&#x25CF; {{- item.Author | strip_newlines | normalize_whitespace -}} </span>
{%- endif -%}
</li>
{%- endfor -%} 
</ul>
{%- endfor -%}



