{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import as_tag with context %}

{% call show_admin_page("ip-grading") %}
<div id="main">

<div id="title">

</div>
<div id="body">

**iP plays mostly a _formative_ role in this course**, i.e., it aims to ensure everyone has achieved the basic competency level needed for the tP (it does not aim to rank you based on programming ability or differentiate strong programmers from the rest). Hence, it is graded somewhat like an S/U component and almost everyone is expected to receive full marks for the iP.

****The iP is worth `{{ marks_ip }}` marks****.{.text-info}

{% if cs2103 %}
* **If you meet all the bars specified below**, you earn the full `{{ marks_ip }}` marks for your iP.
* **If you fall below _any_ of the bars specified below**, your iP score will be less than half the marks.{.text-danger}

That is, you either get full marks or less than half the marks.
{% elseif cs2113 %}
* **Meeting the bars specified below for each aspect** will earn you full `{{ marks_ip }}` marks for iP.
* **Falling below the bars specified for _any_ of the aspects below** will limit your iP score to less than half the marks in that aspect.{.text-danger}

That is, you either get full marks, or less than half the marks for each aspect.
{% endif %}
<box>

##### :fas-trophy: Implementation [`{{ marks_ip_implementation }}` marks]{.text-info}

* **More than 90% of all deliverables** have been completed in the final version of the iP submitted.<br>
    Requirements marked as <span class="badge rounded-pill bg-secondary">optional</span> or <span class="badge rounded-pill bg-secondary">if-applicable</span> are not counted when calculating the percentage of deliverables.<br>
    When a requirement specifies a `minimal` version, reaching that minimal version is enough for it to be counted for grading. However, we recommend you go beyond the minimal version; the farther you go, the more practice you will get.{% if cs2103 %}
* **Has a GUI** that is at least as good as the one reached by !!part 4!! of the JavaFX tutorial (i.e., features covered in part 5 are not required) and <tooltip content="i.e., a user can use the chatbot via the GUI">fit for purpose</tooltip>.
* **Has done at least two <span class="badge rounded-pill bg-secondary">optional</span> increments using AI assistance**, as stated in [Week 6 iP instructions]({{baseUrl}}/admin/ip-w6.html).{% endif %}
* **No major bugs.**
* **Reasonable use of OOP**, e.g., at least some use of inheritance, with code divided into classes in a sensible way (e.g., `Ui`, `Storage`, `Parser`, `Todo`, `Deadline`, `Event`, etc.).
* **At least half of the public methods/classes have Javadoc comments.**
* **Reasonable code quality:**
  * No blatant violations of the coding standard (both Java and Git conventions).
  * The code is neat, e.g., no chunks of commented-out code.{% if cs2103 %}
  * Reasonable use of SLAP, e.g., no very long methods or deeply nested code.{% endif %}
* **At least some errors are handled using exceptions.**{% if cs2103 %}
* **At least two methods have good unit tests** using JUnit.{% endif %}
</box>
<div tags="m--cs2103 m--cs2113">
<box>

##### :fas-trophy: Project Management [`{{ marks_ip_pm }}` marks]{.text-info}

* **Submitted _some_ deliverables** in at least 4 out of the {{ '5' if cs2103 else '6' }} iP weeks (i.e., week 2 to week {{ '6' if cs2103 else '7' }})
* **Followed the other specified requirements** (e.g., using Git/GitHub for each increment and doing peer reviews) in at least 4 weeks{% if cs2103 %}<br>
  <span id="how-to-fix-git-standard">{{ icon_important_big_red }} **To qualify for full marks, your last 5 iP commits need to comply with [our convention for Git commit message subjects]({{ baseUrl }}/admin/standardsAndConventions.html)** (i.e., your {{ as_tag("Git Standard", tag_style="success") }} tag is green). If this item is not green for you, add more commits containing small code tweaks until you satisfy this requirement instead of modifying past commit messages (which requires force-pushing). %%(Reason: this will hopefully help you remember the convention better in the tP)%%.</span> {% endif %}
</box>
<box>

##### :fas-trophy: Documentation [`{{ marks_ip_documentation }}` marks]{.text-info}

The product website and the user guide:

* **Provide enough guidance** to the user. Cover all non-trivial features.
* **No major formatting errors** in the published view.
</box>
</div>

**Grading is mostly based on a manual check of your final submission.** Automated checks done along the way mainly help you self-monitor your progress.

<box type="tip" seamless>

**You can track your iP progress**{.text-success} (as detected by our scripts) on the [iP Progress Dashboard]({{ url_ip_progress_dashboard }}) page.
</box>

</div>
</div>

{% endcall %}
