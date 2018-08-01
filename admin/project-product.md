{% macro show_main_text() %} 
<div id="main">

In this semester, we are going to enhance [an AddressBook application](https://se-edu.github.io/addressbook-level4/).

<img src="{{module_org}}/addressbook-level4/raw/master/docs/images/Ui.png" width="600"/>
<p/>

This product is meant for users who can type fast, and prefer typing over mouse/voice commands. Therefore, ==Command Line Interface (CLI) is the primary mode of input.== 

<panel src="project-constraints.md#constraint-cli" header="Admin {{ icon_embedding }} Admin: Project Contstraints: More info about the 'CLI app' requirement" class="embedding" minimized />
<p/>

</div>
{% endmacro %} 


{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-product", show_main_text) }}
