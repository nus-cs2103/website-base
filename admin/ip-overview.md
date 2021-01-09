{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("ip-overview") %}
<div id="main">

<div id="title">

</div>
<div id="body">

<div tags="m--tic4002">

**The TIC4002 iP is a continuation of the iP you did in TIC4001.** How it differs:
* If some parts of the TIC4001 iP was not done well, you can strengthen them now.
* Some increments that were optional in TIC4001 iP will no longer be optional.
* Some new increments will be added.
* The bar you need to get full marks is higher.

As you know, the iP is based on the generic project called [_Project Duke_](../se-book-adapted/projectDuke/index.html).

</div>
<div tags="m--cs2103 m--cs2113 m--tic4001">

**The objectives of the individual project (iP)** is to learn/refresh the basics of,
* Java
* OOP
* IDEs
* Git and GitHub
* Project automation tools
* Code quality

</div>
<div tags="m--tic4001">

**The iP is very similar to the project you did in TIC2002 but** with the following differences:
* **Faster pace**: You'll need to finish the project within 6 weeks.
* **Better tools**: You'll be using industry-strength tools more %%e.g., use an IDE instead of an online editor%%
* **Higher rigor**: You are expected to follow a more systematic process %%e.g., using Git and GitHub more%%.
* **Higher bar**: The code quality is expected to be higher and the functionality should be more robust %%e.g., required to follow some code quality guidelines%%.

**If you didn't do well in the TIC2002 project**, this is another chance for you to catch up and level up your skills in preparation for the team project that is coming up later.

**If you did well in the TIC2002 project**, use this as an opportunity to stretch yourself and improve your skills further %%e.g., go beyond the minimum requirements, try different design options%%
</div>
<div tags="m--cs2103 m--cs2113 m--tic4001">

**All skills you will learn in the iP will be useful in the team project (tP)**. Some of the iP code can even be adapted for the tP.<br>
{{ icon_tip }} The more you do in the iP and farther you push beyond the minimal expectations, the easier it will be in your tP.

**The iP is based on the generic project called [_Project Duke_](../se-book-adapted/projectDuke/index.html)**, the overview of which is given below.

<include src="dukeFragment.md" boilerplate var-header="**Overview**" var-fragment="text.md#intro" />
<br>

**The iP is to be done over the first half of the semester**.

<box type="warning">

* **Volatile requirements ahead!**: Some requirements will only be released later (or could be changed along the way), to simulate how requirements of a project may not be available at the start or stay the same during the project.
* **Requirements may differ between students!**: Note that some requirements that are to be released later could be different from one student to another.
</box>
</div>

</div>
</div>

{% endcall %}
