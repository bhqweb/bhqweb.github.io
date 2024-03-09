---
title: Photos held in the Archive
layout: lists
menu: barq
sortfields: "'col1','col2','col3','col4','col5','col6','col7','col8','col9','col10','col11','col12','col13','col14','col15','col16'"
---

## {{ page.title }}

Only the first 200 of the 1700+ are shown. Use Search to limit the records. Or click on a column to sort by that column.

<div id="entry-list">
<div class="row" style="margin-bottom:10px;">
		<input type="search" class="search form-control" placeholder="Search" />
</div>
<table class="photos">
<thead>
  <tr>
    <th><span class="sort" data-sort="col1">Reference</span></th>
    <th><span class="sort" data-sort="col2">Number</span></th>
    <th><span class="sort" data-sort="col3">Box</span></th>
    <th><span class="sort" data-sort="col4">ID</span></th>
    <th><span class="sort" data-sort="col5">Date1</span></th>
    <th><span class="sort" data-sort="col6">Source</span></th>
    <th><span class="sort" data-sort="col7">Date2</span></th>
    <th><span class="sort" data-sort="col8">Subject</span></th>
    <th><span class="sort" data-sort="col9">Notes</span></th>
    <th><span class="sort" data-sort="col10">Details</span></th>
    <th><span class="sort" data-sort="col11">Creator</span></th>
    <th><span class="sort" data-sort="col12">Location</span></th>
    <th><span class="sort" data-sort="col13">Dimensions</span></th>
    <th><span class="sort" data-sort="col14">Condition</span></th>
    <th><span class="sort" data-sort="col15">Format</span></th>
    <th><span class="sort" data-sort="col16">Copyright</span></th>
  </tr>
</thead>
<tbody class="list">
{% assign data = site.data.photos %}
{% for row in data %}
  <tr>
    <td class="col1">{{ row.Reference }}</td>
    <td class="col2">{{ row.Photo_No }}</td>
    <td class="col3">{{ row.ImgBox }}</td>
    <td class="col4">{{ row.DigitalID }}</td>
    <td class="col5">{{ row.Date_Added }}</td>
    <td class="col6">{{ row.Source }}</td>
    <td class="col7">{{ row.Date }}</td>
    <td class="col8">{{ row.Subject }}</td>
    <td class="col9">{{ row.Notes }}</td>
    <td class="col10">{{ row.Details }}</td>
    <td class="col11">{{ row.Creator }}</td>
    <td class="col12">{{ row.Location }}</td>
    <td class="col13">{{ row.Dimensions }}</td>
    <td class="col14">{{ row.Condition }}</td>
    <td class="col15">{{ row.Format }}</td>
    <td class="col16">{{ row.Copyright }}</td>
  </tr>
{%- endfor -%}
</tbody>
</table>
</div>
