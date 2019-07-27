{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}

1. Write a brief user guide
1. Release the product
{% endcall %}
<div id="body">

#### {{ thumb(1) }} Write a brief user guide

<include src="dukeFragment.md" boilerplate var-header="**`A-UserGuide`: User Guide**" var-fragment="extensions.mbdf#A-UserGuide" />
<p/>

#### {{ thumb(2) }} Release the product

<include src="dukeFragment.md" boilerplate var-header="**`A-Release`: Release**" var-fragment="extensions.mbdf#A-Release" />

</div>
</div>
{% endmacro %}

{{ show_admin_page("ip-w06", show_main_text) }}