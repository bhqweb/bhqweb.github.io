---
layout: default
title: Forum Journal Articles and Extracts
menu: bhq
---

## {{ page.title }}

### Extracts

- [Forum 84 extracts](forum84-ex/)
- [Forum 83 extracts](forum83-ex/)
- [Forum 82 extracts](forum82-ex/)
- [Forum 81 extracts](forum81-ex/)

### Full Articles

{% assign items_grouped = site.data.forum | group_by: 'Vol' | sort: 'vol' %}
{%- for group in items_grouped -%}
{% assign vol = group.items[0].Vol | strip_newlines | normalize_whitespace %}
{% assign year = group.items[0].Year | strip_newlines | normalize_whitespace %}
{% assign month = group.items[0].Month | strip_newlines | normalize_whitespace %}
{% assign file = group.items[0].file | strip_newlines | normalize_whitespace %}
{% assign ext = group.items[0].file | slice: -3,3 %}
{% if ext == "pdf" %}<li>Forum {{ vol }} &mdash; {% include month.md %} {{ year }} <a href="/pdf/{{- file -}}">view PDF</a></li>{% endif %}
{% if ext == ".md" %}<li>Forum {{ vol }} &mdash; {% include month.md %} {{ year }} <a href="/bhq/forum/volumes/{{- file | replace: '.md', '/' -}}">read.</a></li>{% endif %}
{%- endfor -%}
