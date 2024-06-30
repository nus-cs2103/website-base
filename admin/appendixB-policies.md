{% from "common/macros.njk" import  show_stars with context %}

{% from "common/admin.njk" import show_admin_page, policies with context %}

{% call show_admin_page("appendixB-policies") %}
<div id="main">

{% for policy in policies %}
* [{{ policy.title }}](#{{ policy.id }}) {{show_stars(policy.priority) }}
{% endfor %}

{% for policy in policies %}
<div id="{{ policy.id }}">

### {{ policy.title }} <small><small>{{show_stars(policy.priority) }}</small></small>

<div class="indented">
<include src="policies-fragment.md#{{ policy.id }}" />
</div>

</div>
{% endfor %}

</div>

{% endcall %}
