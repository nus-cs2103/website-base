{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("textbooks") %}
<div id="main">

This module is supported by a customized online textbook [**_Software Engineering for Self-Directed Learners_** ({{ module }} edition)]({{ baseUrl }}/se-book-adapted/index.html), integrated into this module website. While it is in a dynamic Web page format, there is a way to save the main text as pdf files. {% if not (tic4001 or tic4002) %}Printer-friendly versions have been provided too. In addition, ==a PDF version of the full textbook will be provided== by Week 4 of the semester, via LumiNUS.{% endif %}

{{ embed_topic("../book/about/usage.md#saving", "Admin " + icon_embedding + " Using this Website → Saving as PDF files", "3") }}

</div>

{% endcall %}
