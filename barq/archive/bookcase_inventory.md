---
layout: lists
title: Bookcase Inventory
menu: barq
sortfields: "'col1','col2','col3','col4','col5'"
---

## {{ page.title }}

This is a listing of the Books held in the Archive book case, located in the archive.

You can Search to filter records and or sort by column. Refresh to start over.

<div id="entry-list">
   <div class="row" style="margin-bottom:10px;">
      <input type="search" class="search form-control" placeholder="Search"/>
   </div>
   <table class="bookcase_inv">
      <thead>
         <tr>
            <th>
               <span class="sort" data-sort="col1">Author</span>
            </th>
            <th>
               <span class="sort" data-sort="col2">Title</span>
            </th>
            <th>
               <span class="sort" data-sort="col3">Publisher</span>
            </th>
            <th>
               <span class="sort" data-sort="col4">Year</span>
            </th>
            <th>
               <span class="sort" data-sort="col5">Notes</span>
            </th>
         </tr>
      </thead>
      <tbody class="list">
{% assign data = site.data.bookcase-inv %}
{% for row in data %}
<tr>
            <td class="col1">{{ row.Author }}</td>
            <td class="col2">{{ row.Title }}</td>
            <td class="col3">{{ row.Publisher }}</td>
            <td class="col4">{{ row.Date_of_Pub }}</td>
            <td class="col5">{{ row.Notes }}</td>
         </tr>
{%- endfor -%}
</tbody>
   </table>
</div>
