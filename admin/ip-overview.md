{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("ip-overview") %}
<div id="main">

<div id="title">

</div>
<div id="body">

<div tags="m--cs2103 m--cs2113">

**The objectives of the individual project (iP)** is to learn/refresh the basics of,
* Java
* OOP
* IDEs
* Git and GitHub
* Project automation tools
* Code quality

</div>
<div tags="m--cs2103 m--cs2113">

**All skills you will learn in the iP will be useful in the team project (tP)**. Some of the iP code can even be adapted for the tP.<br>
{{ icon_tip }} The more you do in the iP and farther you push beyond the minimal expectations, the easier it will be in your tP.

**The iP is based on the generic project called [_Project Duke_](../se-book-adapted/projectDuke/index.html)**, the overview of which is given below.

<include src="dukeFragment.md" boilerplate var-header="**Overview**" var-fragment="text.md#intro" />
<br>

**The iP is to be done over the first half of the semester**.

</div>

</div>
</div>

{% endcall %}
