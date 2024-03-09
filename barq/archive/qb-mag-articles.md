---
title: QB Magazine articles index 1881-1998
layout: lists
menu: barq
sortfields: "'col1','col2','col3','col4','col5','col6','col7'"
---

## {{ page.title }}

Only the first 200 of the 7890+ are shown. Use Search to limit the records. Or click on a column to sort by that column.

<div id="entry-list">
<div class="row" style="margin-bottom:10px;">
		<input type="search" class="search form-control" placeholder="Search" />
</div>
<table class="qbmagindex">
<thead>
  <tr>
    <th><span class="sort" data-sort="col1">Subject</span></th>
    <th><span class="sort" data-sort="col2">Month</span></th>
    <th><span class="sort" data-sort="col3">Year</span></th>
    <th><span class="sort" data-sort="col4">Page</span></th>
    <th><span class="sort" data-sort="col5">Location</span></th>
    <th><span class="sort" data-sort="col6">Type</span></th>
    <th><span class="sort" data-sort="col7">Note</span></th>

  </tr>
</thead>
<tbody class="list">
{% assign data = site.data.QB-index-1881-1998 %}
{% for row in data %}
  <tr>
    <td class="col1">{{ row.SUBJECT }}</td>
    <td class="col2">{{ row.MON }}</td>
    <td class="col3">{{ row.YEAR }}</td>
    <td class="col4">{{ row.PAGE }}</td>
    <td class="col5">{{ row.LOCATION }}</td>
    <td class="col6">{{ row.TYPE }}</td>
    <td class="col7">{{ row.MEMO }}</td>
  </tr>
{%- endfor -%}
</tbody>
</table>
</div>
