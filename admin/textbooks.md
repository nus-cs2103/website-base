{% macro show_main_text() %}
<div id="main">

This module is supported by a customized online textbook [**_Software Engineering for Self-Directed Learners_** ({{ module }} edition)]({{ baseUrl }}/se-book-adapted/index.html), integrated into this module website. While it is in a dynamic Web page format, there is a way to save the main text as pdf files. Printer-friendly versions have been provided too.

{{ embed_topic("../book/about/usage.md#saving", "Admin " + icon_embedding + " Using this Website → Saving as PDF files", "textbooks-savingAsPdf", "3") }}

</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("textbooks", show_main_text) }}