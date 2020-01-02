{% from "common/admin.njk" import show_admin_page with context %}
{% from "admin/ip-tasks.mbdf" import show_ip_page  with context %}

{% set this_week_num = '8' %}

{% call show_admin_page("ip-w0" + this_week_num) %}
{{ show_ip_page(this_week_num) }}
{% endcall %}
