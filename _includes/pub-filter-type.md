

<ul>
{% assign items_grouped = site.data.Books | group_by: 'Type'  %}
{%- for group in items_grouped -%}
{% assign type = group.items[1].Type | strip_newlines | normalize_whitespace %}
<ul class="pubs">
{%- for item in group.items  -%}
{% if page.filter == 'Type' %}
{% if item.Type == page.fvalue %}
<li>
{% include pub-typeset.md %} 
</li>
{% endif %}
{% elsif page.filter == 'POD' %}
{% if item.POD == page.fvalue %}
<li>
{% include pub-typeset.md %} 
</li>
{% endif %}
{% elsif page.filter == 'OOP' %}
{% if item.OOP == page.fvalue %}
<li>
{% include pub-typeset.md %} 
</li>
{% endif %}
{% endif %}
{%- endfor -%} 
</ul>
{%- endfor -%}