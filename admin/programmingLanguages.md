{% macro show_main_text() %}
<div id="main">

<table class="two-column-content">
<tr>
<td width="160px">
 <img src="{{baseUrl}}/admin/images/JamesGosling.png" width="150px">
</td>
<td>

==**The main language** used in this module is Java==. You should use
Java for all programming activities, the project, and exam answers.

The module doesn’t “teach” Java. We assume you already know Java basics.
We expect you to learn on your own any Java constructs not covered in your previous modules.

</td>
</tr>
</table>

#### Java coding standard
    
This module follows the ==[OSS-NUS Java coding standard]({{java_coding_standard}})==.

==**In the project you are required to follow basic and intermediate guidelines**== (those marked as :star: and :star::star:). In other programming activities in the module, we recommend (but not require) you to follow the coding standard.

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("programmingLanguages", show_main_text) }}