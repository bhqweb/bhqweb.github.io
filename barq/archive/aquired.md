---
title: Items aquired for the Archive
layout: lists
menu: barq
sortfields: "'col1','col2','col3','col4','col5','col6','col7','col8'"
---

## {{ page.title }}

Only the first 500 of the 3600+ are shown. Use Search to limit the records. Or click on a column to sort by that column.

<div id="entry-list">
<div class="row" style="margin-bottom:10px;">
		<input type="search" class="search form-control" placeholder="Search" />
</div>
<table class="aquired">
<thead>
  <tr>
    <th><span class="sort" data-sort="col1">Sequence</span></th>
    <th><span class="sort" data-sort="col2">Indexed</span></th>
    <th><span class="sort" data-sort="col3">Name</span></th>
    <th><span class="sort" data-sort="col4">Notes</span></th>
    <th><span class="sort" data-sort="col5">Box</span></th>
    <th><span class="sort" data-sort="col6">Type</span></th>
    <th><span class="sort" data-sort="col7">Accessioned</span></th>
    <th><span class="sort" data-sort="col8">Note2</span></th>

  </tr>
</thead>
<tbody class="list">
{% assign data = site.data.acquisitions %}
{% for row in data %}
  <tr>
    <td class="col1">{{ row.Seq }}</td>
    <td class="col2">{{ row.Indexed }}</td>
    <td class="col3">{{ row.NAME }}</td>
    <td class="col4">{{ row.NOTES }}</td>
    <td class="col5">{{ row.BOX }}</td>
    <td class="col6">{{ row.TYPE }}</td>
    <td class="col7">{{ row.Accessioned }}</td>
    <td class="col8">{{ row.Note }}</td>
  </tr>
{%- endfor -%}
</tbody>
</table>
</div>
