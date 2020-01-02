{% from "common/admin.njk" import show_admin_page with context %}
{% from "admin/ip-tasks.mbdf" import show_ip_page  with context %}

{% set this_week_num = '7' %}

{% macro show_main_text() %}
{{ show_ip_page(this_week_num) }}
{% endmacro %}

{{ show_admin_page("ip-w0" + this_week_num, show_main_text) }}

