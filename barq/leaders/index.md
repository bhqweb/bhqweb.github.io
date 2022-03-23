---
layout: lists
title: Baptist Church Organisation Leaders in Queensland, Australia 1907-1969
menu: barq
---

## {{ page.title }}

Compiled by Rosemary Kopitke

Names of the church secretaries and treasurers, Sunday school superintendant and secretary, leaders of various groups: ladies, mens, youth, Christian Endeavour, Girls Brigade, Boys Brigade, Junior and Senior Girls Missionary Union.

Type to search for Name, Church, Year or Position. Click on row headers to sort. Click again to get reverse order. 

Note: Only up to 500 rows are shown at one time. There are over 19,000 records altogether. Put in the search a year or church of orgaisation first then sort that field. 
<div id="entry-list">
<div class="row" style="margin-bottom:10px;">
		<input type="search" class="search form-control" placeholder="Search" />
</div>
<table>
<thead>
<tr>
<th><span class="sort" data-sort="name">Name</span></th>
<th>Title</th>
<th><span class="sort" data-sort="church">Church</span></th>
<th><span class="sort" data-sort="year">Year</span></th>
<th><span class="sort" data-sort="position">Position</span></th>
</tr>
</thead>
<tbody class="list">
{% for leader in site.data.leaders %}
	<tr>
		<td class="name">{{ leader.Name }}</td>
		<td class="npre">{{ leader.Title }}</td>
		<td class="church">{{ leader.Church }}</td>
		<td class="year">{{ leader.Year | slice: 0, 4}}</td>
		<td class="position">{{ leader.Position }}</td>
	</tr>
{% endfor %}
</tbody>
</table>
</div>
