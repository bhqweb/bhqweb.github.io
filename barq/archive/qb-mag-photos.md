---
title: QB Magazine Photos
layout: lists
menu: barq
sortfields: "'col1','col2','col3'"
---

## {{ page.title }}

Only the first 200 of the 340+ are shown. Use Search to limit the records. Or click on a column to sort by that column.

<div id="entry-list">
<div class="row" style="margin-bottom:10px;">
		<input type="search" class="search form-control" placeholder="Search" />
</div>
<table class="churches">
<thead>
  <tr>
    <th><span class="sort" data-sort="col1">Reference</span></th>
    <th><span class="sort" data-sort="col2">Date</span></th>
    <th><span class="sort" data-sort="col3">Details</span></th>

  </tr>
</thead>
<tbody class="list qbphotos">
{% assign data = site.data.QB-Mag-photos %}
{% for row in data %}
  <tr>
    <td class="col1">{{ row.NO }}</td>
    <td class="col2">{{ row.DATE }}</td>
    <td class="col3">{{ row.DETAILS }}</td>
  </tr>
{%- endfor -%}
</tbody>
</table>
</div>
