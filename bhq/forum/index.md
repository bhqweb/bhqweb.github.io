---
layout: default
title: Forum 1984&#x2013;
menu: bhq
dlpath: /dl/
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
<!-- The following line was changed 2024-03-08 so the download goes via a redirect html page to record downloads. -->
{% if ext == "pdf" %}
<li>
<a href="{{ page.dlpath }}{{- file | replace: ".pdf","/" -}}">view PDF</a>
</li>
{% endif %}
{% if ext == ".md" %}<li><a href="/bhq/forum/volumes/{{- file | replace: ".md","/" -}}">view file</a></li>{% endif %}

{%- for item in group.items -%}
{% if item.Order != "0" %}
<li> <span class="title">{{ item.Title | normalize_whitespace | strip_newlines }}</span>
{% assign test1 = item.SubTitle | strip_newlines %}
{%- if test1 != "" -%}<span class="subTitle"> &mdash; {{ item.SubTitle | strip_newlines | normalize_whitespace }}</span> {%- endif -%}
{%- assign test2 = item.Author | strip_newlines -%}
{%- if test2 != "" -%}<span class="author"> &#x25CF; {{ item.Author | strip_newlines | normalize_whitespace }} </span>
{%- endif -%}
{% assign linktest = item.link | strip_newlines %}
{%- if linktest != "" -%} <a href="{{ item.link | strip_newlines | normalize_whitespace }}">{{ item.linklabel | strip_newlines | normalize_whitespace }}</a> {%- endif -%}
</li>
{%- endif -%}
{%- endfor -%} 
</ul>
{%- endfor -%}



