{% from "common/macros.njk" import  show_stars with context %}

{% macro show_main_text() %}
<div id="main">

{% for policy in policies %}
* [{{ policy.title }}](#{{ policy.id }}) {{show_stars(policy.priority) }}
{% endfor %}

{% for policy in policies %} 
<div id="{{ policy.id }}">

### {{ policy.title }} <small><small>{{show_stars(policy.priority) }}</small></small>

<div class="indented">
<include src="policies.fr#{{ policy.id }}" />
</div>

</div>
{% endfor %}

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page, policies with context %}
{{ show_admin_page("appendixB-policies", show_main_text) }}