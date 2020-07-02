{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("programmingLanguages") %}
<div id="main">

<table class="two-column-content">
<tr>
<td width="160px">
 <img src="{{baseUrl}}/admin/images/JamesGosling.png" width="150px">
</td>
<td>

==**The main language** used in this module is Java==. You should use
Java for all programming activities, the project, and exam answers.

<span tags="m--cs2103">

The module doesn’t “teach” Java. We assume you already know Java basics.
We expect you to learn on your own any Java constructs not covered in your previous modules.
The exam expects you to know Java to the extent that you should be familiar with it by virtue of using it in the module exercises/projects.
</span>

</td>
</tr>
</table>

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>

We require you to use **Java 11** (the Oracle version or the OpenJDK version) for all module work. It is your duty to ensure the code you write (and executables you produce) are compatible with that version of Java. ==Any incompatibilities will be considered as bugs==.
</box>

#### Java coding standard
    
This module follows the ==[this Java coding standard]({{url_java_coding_standard}})==.

<div tags="m--cs2113">

==**You are required to follow basic guidelines**== (those marked as :star:) in the module projects. Intermediate and advanced guidelines are optional.
</div>
<div tags="m--cs2103">

==**You are required to follow basic and intermediate guidelines**== (those marked as :star: and :star::star:) in the module projects. Advanced guidelines are optional.
</div>

</div>

{% endcall %}
