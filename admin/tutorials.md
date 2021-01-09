{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tutorials") %}
<div id="main">

<panel type="seamless" expanded >
<span slot="header" class="card-title"><markdown>### Tutorial Timetable</markdown></span>
<div id="tutorialTimetable">

<box>

{{ icon_important_big_red }} Our tutorial IDs are different from LumiNUS. Format: `{{ module }}T-W09` means a tutorial of `{{ module }}T` module, held on `Wednesday` at `0900`, and so on.

</box>

Module | Venue | Time | ~~%%Tutorial ID<br>in LumiNUS%%~~<br>==(don't use this!)== | **Our Tutorial ID**<br>==(use this!)== | Tutors<br>([contact details](instructors.html))
-------|-------|------|------------------------------------------------------------|----------------------------------------|-------
<include src="../_module-{{ module }}/timetables.mbdf#tutorials-s{{ S }}" inline trim optional />

</div>
</panel>

<panel type="seamless" header="### Tutorial Structure" expanded >
<div id="tutorialStructure">

**The mode**

* Tutorials will be conducted using Zoom.
* MS Teams will be used for file sharing.
* A tutorial group is handled by two tutors. Each tutor will work with two teams.
* The tutor will _facilitate_ tutorial activities, observe your progress, and give feedback.

<!--
* Please ==bring your laptop to tutorials.== You'll need it for tutorial tasks.

{{ embed_topic("appendixC-faq.md#admin-faq-noLaptop", "Admin " + icon_embedding + " Appendix C(FAQ): What if I don't carry around a laptop?", "4", indent=2) }}
-->

<br/>

**Slides and tutorial recordings**:
* The Zoom recording of a tutorial will be made available to you after the tutorial.
* <span class="text-danger">Slides used in tutorials will not be distributed to students.</span> You are expected to take notes (or screenshots) during the tutorial as necessary.


**The role of our tutors** is different from tutors in other modules.

* **Not a source of admin information**: Given the humongous amount of admin info contained in this module and the fact that it is constantly evolving, tutors may not be aware of the recent subtle changes to the admin information. To safeguard you from receiving incorrect admin info, tutors are prohibited from answering admin queries. If you have an admin query, please post in the [forum]({{ url_forum }}) (or email the prof at `{{ module | lower }}@comp.nus.edu.sg` but only if the question is not appropriate for the forum).

* **No inputs for yet-to-be-graded components**: Tutors are prohibited from giving inputs for components not graded yet. %%Reason: work submitted for grading should be your own.%%

* **No direct tech help**: Tutors are prohibited from giving direct technical help, other than to give you some general direction to finding a solution. %%Rationale: We want you to learn the vital survival skill of troubleshooting technical problems.%%

<div class="indented-level2">
{{ embed_topic("appendixD-help.md#main", "Admin " + icon_embedding + " Appendix D: How to get Help in " + module_pair, "2") }}
</div>

<br/>

* **No ‘mini-lectures’**: Tutors are prohibited from 'teaching' concepts that are covered in lectures or other learning resources given to you %%(reason: self-learning is a vital part of the module)%%. For example, ==the tutor will not do a mini-lecture at the start of the tutorial==. Of course tutors can help you clarify doubts under the right circumstances.

<div class="indented-level2">
{{ embed_topic("appendixD-help.md#questions-for-tutros", "Admin " + icon_embedding + " Appendix D (extract): Questions suitable to ask the tutor", "2") }}
</div>

<br/>

**Timing/venue:**

* Please refer to the {{ url_schedule }} for further details on each tutorial.
* You are expected to be present on time. ==Punctuality is considered for participation marks.==

<!--
* You may leave the class 15 minutes before the hour if you have another class right after. There is no need to wait till the tutor dismisses you. However, inform the tutor (as a courtesy) before leaving if you leave before the class is dismissed.
* ==Vacate the table 5 minutes before the hour== so that the next group can start on time.
-->

* In the past, many students have requested to increase the tutorial duration because a mere hour is barely enough to get through all the tutorial tasks. Increasing the tutorial time is not possible due to lack of venues and tutors. Instead, let's try to make the best of the one hour available by coming well prepared and starting on time. Note that ==the better prepared you are, the higher the chance of completing e all activities allocated to a tutorial== within time.

**Grading:**

* Your conduct in tutorials will be evaluated by team members and the tutor which can affect your participation marks.

</div>
</panel>
</div>

{% endcall %}
