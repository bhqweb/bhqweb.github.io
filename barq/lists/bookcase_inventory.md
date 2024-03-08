---
layout: lists
title: Bookcase Inventory
menu: barq
---

## {{ page.title }}

This is a listing of the Books held in the Archive book case, located in the archive.


<div id="entry-list">
   <!-- <div class="row" style="margin-bottom:10px;">
      <input type="search" class="search form-control" placeholder="Search"/>
   </div> -->
   <table class="bookcase_inv">
      <thead>
         <tr>
            <th>
               <span class="sort" data-sort="author">Author</span>
            </th>
            <th>
               <span class="sort" data-sort="title">Title</span>
            </th>
            <th>
               <span class="sort" data-sort="publisher">Publisher</span>
            </th>
            <th>
               <span class="sort" data-sort="date_of_pub">Date of Pub</span>
            </th>
            <th>
               <span class="sort" data-sort="notes">Notes</span>
            </th>
         </tr>
      </thead>
      <tbody class="list">
{% assign data = site.data.bookcase-inv %}
{% for row in data %}
<tr>
            <td class="Author">{{ row.Author }}</td>
            <td class="Title">{{ row.Title }}</td>
            <td class="Publisher">{{ row.Publisher }}</td>
            <td class="Date_of_Pub">{{ row.Date_of_Pub }}</td>
            <td class="Notes">{{ row.Notes }}</td>
         </tr>
{%- endfor -%}
</tbody>
   </table>
</div>
