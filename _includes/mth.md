{%- case month -%}
{%- when "1" -%}Jan
{%- when "2" -%}Feb
{%- when "3" -%}Mar
{%- when "4" -%}Apr
{%- when "5" -%}May
{%- when "6" -%}Jun
{%- when "7" -%}Jul
{%- when "8" -%}Aug
{%- when "9" -%}Sep
{%- when "10" -%}Oct
{%- when "11" -%}Nov
{%- when "12" -%}Dec
{%- when "5-8" -%}May-Aug
{%- else -%}{{ month }}{%- endcase -%}