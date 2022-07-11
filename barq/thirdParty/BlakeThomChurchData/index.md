---
layout: lists
title: Baptist Church information by Thom Blake
menu: barq
sortfields: "'Location','Name','Date'"
---

## {{ page.title }}

Compiled by Thom Blake

Thom Blake is an historian. This page provides links to his [website](https://thomblake.com.au/) with information and images about churches. BHSQ has not validaded the information.

Searching will filter the table. You can also sort on the Location, Church or Year fields, by clicking on those words in the table header.

<div id="entry-list">
<div class="row" style="margin-bottom:10px;">
		<input type="search" class="search form-control" placeholder="Search" />
</div>
<table>
<thead>
<tr>
<th>Link</th>
<th><span class="sort" data-sort="Location">Location</span></th>
<th><span class="sort" data-sort="Name">Church</span></th>
<th><span class="sort" data-sort="Date">Year</span></th>
</tr>
</thead>
<tbody class="list">
{% for church in site.data.thomblake-data %}
	<tr>
		<td class="link"><a href="https://www.thomblake.com.au/qc_new/view_p.php?id={{ church.View }}" target="_blank">View</a></td>
		<td class="Location">{{ church.Location }}</td>
		<td class="Name">{{ church.Name }}</td>
		<td class="Date">{{ church.Date }}</td>
	</tr>
{% endfor %}
</tbody>
</table>
</div>
