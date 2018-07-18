{% from "common/macros.njk" import  show_stars with context %}

{% macro show_main_text() %}
<div id="main">

# Appendix C: Frequently Asked Questions

{% for faq in FAQs %} 
* [{{ faq.title }}](#{{ faq.id }}) {{show_stars(faq.priority) }}
{% endfor %}

{% for faq in FAQs %} 
<div id="{{ faq.id }}">

### {{ faq.title }} <small><small>{{show_stars(faq.priority) }}</small></small>

<div class="indented">
<include src="faq.md#{{ faq.id }}" />
</div>

</div>
{% endfor %}

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page, FAQs with context %}
{{ show_admin_page("appendixC-faq", show_main_text) }}