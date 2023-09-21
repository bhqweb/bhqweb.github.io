---
layout: default
title: Forum 1984 - 2022
menu: bhq
---

## {{ page.title }}

To search press Ctrl and F, then type your search word, then press enter.

{% assign items_grouped = site.data.forum | group_by: 'Vol' %}
{%- for group in items_grouped -%}
{% assign vol = group.items[0].Vol | strip_newlines | normalize_whitespace %}
{% assign year = group.items[0].Year | strip_newlines | normalize_whitespace %}
{% assign month = group.items[0].Month | strip_newlines | normalize_whitespace %}
{% assign file = group.items[0].file | strip_newlines | normalize_whitespace %}
{% assign ext = group.items[0].file | slice: -3,3 %}
{% assign title = group.items[0].Title | strip_newlines | normalize_whitespace %}
### Forum {{ vol }} &mdash; {% include month.md %} {{ year }}



<ul>

{% if ext == "pdf" %}<li><a href="/pdf/{{- file -}}">view PDF</a></li>{% endif %}
{% if ext == ".md" %}<li><a href="/bhq/forum/volumes/{{- file | replace: ".md",".html" -}}">view file</a></li>{% endif %}

{%- for item in group.items -%}
{% if item.Order != "0" %}
<li> <span class="title">{{ item.Title | normalize_whitespace | strip_newlines }}</span>
{% assign test1 = item.SubTitle | strip_newlines %}
{%- if test1 != "" -%}<span class="subTitle"> &mdash; {{ item.SubTitle | strip_newlines | normalize_whitespace }}</span> {%- endif -%}
{%- assign test2 = item.Author | strip_newlines -%}{%- if test2 != "" -%}
<span class="author"> &#x25CF; {{ item.Author | strip_newlines | normalize_whitespace }} </span>
{%- endif -%}
</li>
{%- endif -%}
{%- endfor -%} 
</ul>
{%- endfor -%}



