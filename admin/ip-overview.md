{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("ip-overview") %}
<div id="main">

<div id="title">

</div>
<div id="body">

The objectives of the individual project (iP) is to learn/refresh the basics of,
* Java
* OOP
* IDEs
* Git and GitHub
* Code quality

All skills you will learn in the iP will be useful in the team project (tP). Furthermore, some of the code you will write in iP can be adapted for the tP.

The iP is based on the generic project called [_Project Duke_](../se-book-adapted/projectDuke/index.html), the overview of which is given below.

<include src="dukeFragment.md" boilerplate var-header="**Duke - Overview**" var-fragment="text.md#intro" />
<br>

The project is to be **done over the first half of the semester**.

<box type="warning">

* **Volatile requirements ahead!**: Some requirements will only be released later (or could be changed along the way), to simulate how requirements of a project may not be available at the start or stay the same during the project.
* **Requirements may differ between students!**: Note that some requirements that are to be released later could be different from one student to another.
</box>

</div>
</div>

{% endcall %}
