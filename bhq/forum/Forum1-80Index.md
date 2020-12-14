---
layout: default
title: Forum Index Vols 1-80
menu: bhq
---

{{ page.title }}

{% assign list = site.data.Forum1-80Index %}
<table class="forum1-80">
  <tr>
    <th>Year</th>
    <th>Month</th>
    <th>Forum No.</th>
    <th>Article</th>
    <th>Topic Area</th>
    <th>Author</th>
  </tr>
{% for item in list %}
{% assign month = item.Month | strip_newlines | normalize_whitespace %}
  <tr>
  <td>{{ item.Year }}</td>
  <td>{% include mth.md %}</td>
  <td>{{ item.No }}</td>
  <td>{{ item.Article }}</td>
  <td>{{ item.PostAuthor }}</td>
  <td>{{ item.Author }}</td>
  </tr>
{%- endfor -%}
</table>