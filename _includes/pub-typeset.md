{%- assign ttitle = item.Title | normalize_whitespace | strip_newlines -%}
{%- assign ttitleid = item.Title | normalize_whitespace | strip_newlines| replace: ' ', '_' -%}
{%- assign tsubtitle = item.Subtitle | strip_newlines -%}
{%- assign tauthor = item.Author | strip_newlines | replace: ' ', '&nbsp;' -%}
{%- assign tyear = item.Author | strip_newlines -%}
{%- assign textent = item.Extent | strip_newlines -%}
{%- assign tisbn = item.ISBN | strip_newlines -%}
{%- assign tseries = item.Series | strip_newlines -%}
{%- assign tedition = item.Edition | strip_newlines -%}
{%- assign tvol = item.Volume | strip_newlines -%}
{%- assign tednote = item.EditionNote | strip_newlines -%}
{%- assign tfeatures = item.Features | strip_newlines -%}
{%- assign turl = item.URL | strip_newlines -%}
{%- assign surl = item.URL | strip_newlines | split: '/' -%}
{%- assign tcost = item.Cost | strip_newlines -%}
{%- assign tship = item.Shipping | strip_newlines -%}
{%- assign tpod = item.POD | strip_newlines -%}
{%- assign toop = item.OOP | strip_newlines -%}
{%- assign timage = item.Image | strip_newlines -%}

{%- if timage != "" -%}<div class="bk-thumb"><img src="/images/thumbs/{{- timage -}}" alt="{{- ttitle -}}"/></div>{%- endif -%}
<span class="title" id="{{- ttitleid -}}">{{- ttitle -}}</span>
{%- if tsubtitle != "" -%}<span class="subtitle"> &mdash; {{- tsubtitle -}}</span> {%- endif -%}
{%- if tauthor != "" -%}<span class="author">&ensp;&#x25CF;&ensp;{{- tauthor  -}} </span>{%- endif -%}
{%- if tyear != "" -%}<span class="year">&ensp;{{- item.Year -}} </span>{%- endif -%}
{%- if textent != "" -%}<span class="extent">&ensp;{{ item.Extent }}{{- item.Ext-type -}} </span>{%- endif -%}
{%- if tisbn != "" -%}<span class="isbn">&ensp;ISBN:&nbsp;{{ item.ISBN }} </span>{%- endif -%}
{%- if tseries != "" -%}<span class="series">&ensp;({{- item.Series -}}{%- if item.SeriesNo != "" -%}&nbsp;{{ item.SeriesNo }}){%- endif -%}</span>{%- endif -%}
{%- if tedition != "" -%}<span class="edition">&ensp; {{ item.Edition }} Edition </span>{%- endif -%}
{%- if tvol != "" -%}<span class="volumes">&ensp;Volumes {{ item.Volumes }} </span>{%- endif -%}
{%- if tednote != "" -%}<span class="editionnote">&ensp; {{ item.EditionNote }} </span>{%- endif -%}
{%- if tfeatures != "" -%}<span class="pubfeatures">&ensp; {{ item.Features }} </span>{%- endif -%}
{%- if turl != ""  -%}<span class="url"><a href="{{- turl -}}" alt="Lulu" style="display:inline">{{- surl[2] -}}</a> </span>{%- endif -%}
{%- if tcost != "" -%}<span class="price">&ensp; {{ tcost }} </span>{%- endif -%}
{% comment %}
{%- if tship != "" -%}<span class="shipping"> plus {{ tship  }} postage</span>{%- endif -%}
{% endcomment %}
{%- if tship!= "" -%}<span class="shipping"> plus postage</span>{%- endif -%}
{%- if toop != "" -%}<span class="out-print">&ensp; Out&nbsp;of&nbsp;print!</span>{%- endif -%}
