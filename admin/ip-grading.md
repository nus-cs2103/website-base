{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("ip-grading") %}
<div id="main">

<div id="title">

</div>
<div id="body">

**iP serves mostly a _formative_ role in this course** i.e., it aims to ensure everyone has achieved a basic competency level that is a prerequisite to survive the tP (it does not aim to rank you based on strength or differentiate strong programmers from the rest). Hence, it is graded somewhat like an S/U component and almost everyone is expected to receive full marks for the iP.

****Full marks for the iP is `{{ marks_ip }}`****.{.text-info}

* **Meeting all the bars specified below** you earn your iP full  `{{ marks_ip }}` marks.
* **Falling below _any_ of the bars specified below** will limit your iP score to less than half the marks.{.text-danger}

That is, you either get full marks, or less than half the marks.

<box>

##### :fas-trophy: Implementation [`{{ marks_ip_implementation }}` marks]{.text-info}

* **More than 90% of all deliverables** completed.<br>
    Requirements marked as <span class="badge rounded-pill bg-secondary">optional</span> or <span class="badge rounded-pill bg-secondary">if-applicable</span> are not counted when calculating the percentage of deliverables.<br>
    When a requirement specifies a `minimal` version of it, simply reaching that minimal version of the requirement is enough for it to be counted for grading -- however, we recommend you to go beyond the minimal; the farther you go, the more practice you will get.{% if cs2103 %}
* **Has a GUI** that it at least as good as the one given in the JavaFx tutorial.{% endif %}
* **No major bugs.**
* **Reasonable use of OOP** e.g., at least some use of inheritance, code divided into classes in a sensible way (e.g., `Ui`, `Storage`, `Parser`, `Storage`, `Todo`, `Deadline`, `Event` etc.).
* **At least half of public methods/classes have javadoc comments.**
* **Reasonable code quality:**
  * No blatant violations of the coding standard (both Java and Git conventions).
  * The code is neat e.g., no chunks of commented out code.{% if cs2103 %}
  * Reasonable use of SLAP e.g., no very-long methods or deeply nested code.{% endif %}
* **At least some errors are handled using exceptions.**{% if cs2103 %}
* **At least two methods unit tested well** using JUnit.{% endif %}
</box>
<div tags="m--cs2103 m--cs2113 m--tic4001">
<box>

##### :fas-trophy: Project Management [`{{ marks_ip_pm }}` marks]{.text-info}

* **Submitted _some_ deliverables** in at least 4 out of the {{ '5' if cs2103 else '6' }} iP weeks (i.e., week 2 - week {{ '6' if cs2103 else '7' }})
* **Followed other requirements specified** (e.g., how to use Git/GitHub for each increment, do peer reviews) in at least 4 weeks
</box>
<box>

##### :fas-trophy: Documentation [`{{ marks_ip_documentation }}` marks]{.text-info}

The product Website and the user guide:

* **Provides enough guidance** to the user. Covers all non-trivial features.
* **No major formatting errors** in the published view.
</box>
</div>
<div tags="m--tic4002">

**Project Management [`{{ marks_ip_pm }}` marks]**: To get full marks, you should achieve,
* Submit _some_ deliverables in at least 3 out of the 5 iP weeks (i.e., week 2 - week 6)
* Follow other requirements specified (e.g., how to use Git/GitHub for each increment) in at least 4 weeks

**Documentation [`{{ marks_ip_documentation }}` marks]**: To get full marks, you should achieve the following.
* The user guide: not hard to read, covers all features, no major formatting errors in the published view.
* The developer guide: Explains the design of the project using appropriate UML diagrams and descriptions.
</div>

<box type="tip" seamless>

**You can monitor your iP progress**{.text-success} (as detected by our scripts) in the [iP Progress Dashboard]({{ url_ip_progress_dashboard }}) page.
</box>

</div>
</div>

{% endcall %}
