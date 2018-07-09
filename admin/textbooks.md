{% macro show_main_text() %}
<div id="main">

# Text Books

The main text book is [here]({{baseUrl}}/se-book-adapted/index.html). While it is in a dynamic Web page format, [there is a way to save the main text as pdf files]({{baseUrl}}/book/about/usage.html#saving).


</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("textbooks", show_main_text) }}