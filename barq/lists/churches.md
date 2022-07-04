---
layout: lists
title: Baptist Union of Queensland - Churches
menu: barq
sortfields: "'church','commense','const','build'"
---

## {{ page.title }}

### Churches 1855+- with dates of commencement, constitution and first building (where available)

(As published in official directories and supplemented with additonal informaton - subject to correction - submissions welcomed)

<div id="entry-list">
<div class="row" style="margin-bottom:10px;">
		<input type="search" class="search form-control" placeholder="Search" />
</div>
<table class="churches">
<thead>
  <tr>
    <th><span class="sort" data-sort="church">Church</span></th>
    <th><span class="sort" data-sort="commense">Commencement</span></th>
    <th><span class="sort" data-sort="const">Constitution</span></th>
    <th><span class="sort" data-sort="build">Building</span></th>
  </tr>
</thead>
<tbody class="list">
{% assign churches = site.data.church-start %}
{% for item in churches %}
  <tr>
  <td class="church">{{ item.Church }}</td>
  <td class="commense">{{ item.Commensement }}</td>
  <td class="const">{{ item.Constitution }}</td>
  <td class="build">{{ item.Building }}</td>
  </tr>
{%- endfor -%}
</tbody>
</table>
</div>

