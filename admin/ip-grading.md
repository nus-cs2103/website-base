{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("ip-grading") %}
<div id="main">

<div id="title">

</div>
<div id="body">

****Total: `{{ marks_ip }}` marks****

**Implementation [`{{ marks_ip_implementation }}` marks]**: To get full marks, you should achieve,
* Achieve **more than 90% of all deliverables** by the end.
* Requirements marked as <span class="badge badge-pill badge-secondary">optional</span> or <span class="badge badge-pill badge-secondary">if-applicable</span> are not counted when calculating the percentage of deliverables.
* When a requirement specifies a `minimal` version of it, simply reaching that minimal version of the requirement is enough for it to be counted for grading -- however, we recommend you to go beyond the minimal; the farther you go, the more practice you will get.

**Project Management [`{{ marks_ip_pm }}` marks]**: To get full marks, you should achieve,
* Submit _some_ deliverables in at least 4 out of the 6 iP weeks (i.e., week 2 - week {{ ip_last_week }})
* Follow other requirements specified (e.g., how to use Git/Github for each increment, do peer reviews) in at least 4 weeks

**Documentation [`{{ marks_ip_documentation }}` marks]**: To get full marks, you should achieve,
* The product web site and the user guide is reasonable

<box type="tip" seamless>

You can monitor your iP progress (as detected by our scripts) in the [iP Progress Dashboard]({{ url_ip_progress_dashboard }}) page.
</box>

</div>
</div>

{% endcall %}
