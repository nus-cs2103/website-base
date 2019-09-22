{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. Do any final clean-ups
1. Submit the final version {{ timing_badge('by Monday 2359') }}
{% endcall %}
<div id="body">

#### {{ thumb(1) }} Do any final clean-ups

* Finish leftover increments from the previous weeks, if any
* Do any code cleanups, if necessary
* Update the User Guide, if necessary

#### {{ thumb(2) }} Submit the final version {{ timing_badge('by Monday 2359', "secondary") }}

* Submission is to be done via GitHub releases. If there were any changes to the code since the last release, do a new release.
* {{ icon_important_big_red }} The jar file should be ==cross-platform and should work in a computer that has Java 11==.

<div class="indented">
<panel minimized >
<div slot="header" class="card-title">

{{ icon_tip }} **Getting more out of the iP**
</div>

**If you wish to cite the iP in your resume**, you can do more to make it look more impressive to a potential employer. These improvements are not considered for grading and can be done after the semester is over. Some ideas:
* **Improve the GUI**: Make the UI look nicer, unique, and memorable. You can get inspiration from [what others have done](ip-showcase.html) (but remember to give credit if you reuse any code from them).
* **Add a demo** video or an animated gif to your user guide to show how the app works.
* **Improve code quality**: iP is the right size to cite as an example of your code quality. You can use the RepoSense link (<span class="badge badge-light badge-pill text-monospace">**</>**</span>) in the [iP showcase page](ip-showcase.html) to point to your iP code.
* **Add more features.**

On a somewhat related note, you can also **create similar product websites for your other projects** (projects from other modules, pet projects).
</panel>

</div>

</div>
</div>
{% endmacro %}

{{ show_admin_page("ip-w06", show_main_text) }}