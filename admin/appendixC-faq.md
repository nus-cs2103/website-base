{% from "common/macros.njk" import  show_stars with context %}

{% macro show_main_text() %}
<div id="main">

{% for faq in faqs %}
* [{{ faq.title }}](#{{ faq.id }}) {{show_stars(faq.priority) }}
{% endfor %}

{% for faq in faqs %} 
<div id="{{ faq.id }}">

### {{ faq.title }} <small><small>{{show_stars(faq.priority) }}</small></small>

<div class="indented">
<include src="faq.md#{{ faq.id }}" />
</div>

</div>
{% endfor %}

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page, faqs with context %}
{{ show_admin_page("appendixC-faq", show_main_text) }}