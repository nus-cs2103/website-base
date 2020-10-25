{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("ip-grading") %}
<div id="main">

<div id="title">

</div>
<div id="body">

****Total: `{{ marks_ip }}` marks****

**Implementation [`{{ marks_ip_implementation }}` marks]**: Requirements to get full marks:
* Achieve **more than 90% of all deliverables** by the end.
  * Requirements marked as <span class="badge badge-pill badge-secondary">optional</span> or <span class="badge badge-pill badge-secondary">if-applicable</span> are not counted when calculating the percentage of deliverables.
  * When a requirement specifies a `minimal` version of it, simply reaching that minimal version of the requirement is enough for it to be counted for grading -- however, we recommend you to go beyond the minimal; the farther you go, the more practice you will get.
* **The code quality** meets the following conditions:
  * Reasonable use of OOP e.g., at least some use of inheritance, code divided into classes in a sensible way
  * No blatant violations of the coding standard
  * At least some errors are handled using exceptions
  * At least half of public methods/classes have javadoc comments
  * The code is neat e.g., no chunks of commented out code
  * Reasonable use of SLAP e.g., no very-long methods or deeply nested code{% if cs2103 %}
  * Has some JUnit tests{% endif %}

**Project Management [`{{ marks_ip_pm }}` marks]**: To get full marks, you should achieve,
* Submit _some_ deliverables in at least 4 out of the {{ '5' if cs2103 else '6' }} iP weeks (i.e., week 2 - week {{ '6' if cs2103 else '7' }})
* Follow other requirements specified (e.g., how to use Git/Github for each increment, do peer reviews) in at least 4 weeks

**Documentation [`{{ marks_ip_documentation }}` marks]**: To get full marks, you should achieve,
* The product web site and the user guide is _reasonable_ (i.e., functional, not hard to read, covers all features, no major formatting errors in the published view).

<box type="tip" seamless>

You can monitor your iP progress (as detected by our scripts) in the [iP Progress Dashboard]({{ url_ip_progress_dashboard }}) page.
</box>

</div>
</div>

{% endcall %}
