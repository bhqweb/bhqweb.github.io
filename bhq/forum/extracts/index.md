---
layout: default
title: Forum Journal Articals and Extracts
menu: bhq
---

## {{ page.title }}

- [Forum 1 articles](../volumes/QB-Forum001.html)
- [Forum 81 extracts](forum81-ex.html)
- [Forum 82 extracts](forum82-ex.html)
- [Forum 83 extracts](forum83-ex.html)
- [Forum 84 extracts](forum84-ex.html)


{% assign items_grouped = site.data.forum | group_by: 'Vol' | sort: 'vol' %}
{%- for group in items_grouped -%}
{% assign vol = group.items[0].Vol | strip_newlines | normalize_whitespace %}
{% assign year = group.items[0].Year | strip_newlines | normalize_whitespace %}
{% assign month = group.items[0].Month | strip_newlines | normalize_whitespace %}
{% assign file = group.items[0].file | strip_newlines | normalize_whitespace %}
{% assign ext = group.items[0].file | slice: -3,3 %}
{% if ext == "pdf" %}<li>Forum {{ vol }} &mdash; {% include month.md %} {{ year }} <a href="/pdf/{{- file -}}">view PDF</a></li>{% endif %}
{%- endfor -%}
