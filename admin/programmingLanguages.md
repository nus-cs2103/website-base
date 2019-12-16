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
    
This module follows the ==[this Java coding standard]({{java_coding_standard}})==.

==**In the project you are required to follow basic and intermediate guidelines**== (those marked as :star: and :star::star:). In other programming activities in the module, we recommend (but not require) you to follow the coding standard.

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>

We require you to use **Java 11** (the Oracle version or the OpenJDK version) for all module work. It is your duty to ensure the code you write (and executables you produce) are compatible with that version of Java. ==Any incompatibilities will be considered as bugs==.
</box>

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("programmingLanguages", show_main_text) }}