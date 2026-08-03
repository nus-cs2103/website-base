{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import show_faq with context %}

{% call show_admin_page("programmingLanguages") %}
<div id="main">

<table class="two-column-content">
<tbody>
<tr>
<td width="160px">
 <pic eager src="{{baseUrl}}/admin/images/JamesGosling.png" width="150px"></pic>
</td>
<td>

**The main language used in this course is Java**. You should use
Java for all programming activities, the project, and exam answers.

<span tags="m--cs2103">

This course does not teach Java directly. We assume you already know Java basics.
We expect you to learn on your own any Java constructs not covered in your previous courses.
The exam expects Java knowledge you would normally gain from using it in the course exercises and projects.
</span>

</td>
</tr>
</tbody>
</table>

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>

We require you to use **Java {{ java_version }}** (the [Oracle version](https://www.oracle.com/java/technologies/downloads/#java{{ java_version }}) or an alternative such as OpenJDK) for all coursework. It is your responsibility to ensure the code you write (and executables you produce) is compatible with that version of Java. ==Any incompatibilities will be considered bugs==.

**You are strongly discouraged from using a Java version other than {{ java_version }}.** If you need to use a different version for another course, use this as an opportunity to learn how to manage multiple Java versions on your computer.

Refer to the [se-edu/guides Java installation guides](https://se-education.org/guides/tutorials/javaInstallation.html) for help with installing, verifying, configuring, and switching between Java versions.

{% if cs2103 %}

<panel type="danger" header="[IMPORTANT] Advisory for :fab-apple: Mac users" expanded >

Mac users should use the specific Azul JDK {{ java_version }} distribution recommended in [this guide](https://se-education.org/guides/tutorials/javaInstallationMac.html).

To reiterate, #r#having Java {{ java_version }} is not enough##; you need ==the precise **Azul** JDK<strong>+JavaFX</strong> version specified== in the page linked above.

</panel>


{% endif %}

</box>

</div>

{% endcall %}
