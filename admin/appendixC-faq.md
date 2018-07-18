{% macro show_main_text() %}
<div id="main">

# Appendix C: Frequently Asked Questions

{% for faq in FAQs %} 
* [{{ faq.title }}](#{{ faq.id }})
{% endfor %}

{% for faq in FAQs %} 
<div id="{{ faq.id }}">

### {{ faq.title }} 

<include src="faq.md#{{ faq.id }}" />

</div>
{% endfor %}

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page, FAQs with context %}
{{ show_admin_page("appendixC-faq", show_main_text) }}