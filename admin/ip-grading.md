{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("ip-grading") %}
<div id="main">

<div id="title">

</div>
<div id="body">

To get full marks, you should achieve **at least some iP deliverables in most weeks** (i.e., at least in 4 out of weeks 1-7) and achieve **more than 80% of all deliverables** by the end.
* Requirements marked as <span class="badge badge-pill badge-secondary">optional</span> or <span class="badge badge-pill badge-secondary">if-applicable</span> are not counted when calculating the percentage of deliverables.
* When a requirement specifies a `minimal` version of it, simply reaching that minimal version of the requirement is enough for it to be counted for grading -- however, we recommend you to go beyond the minimal; the farther you go, the more practice you will get.

</div>
</div>

{% endcall %}
