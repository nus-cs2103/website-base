{% macro show_main_text() %}
<div id="main">

This module is supported by a customized online text book [**_Software Engineering for Self-Directed Learners_** ({{ module }} edition)]({{ baseUrl }}/se-book-adapted/index.html), integrated into this module website. While it is in a dynamic Web page format, [there is a way to save the main text as pdf files]({{baseUrl}}/admin/usingThisWebsite.html#saving-as-pdf-files). Printer-friendly versions have been provided too.


</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("textbooks", show_main_text) }}