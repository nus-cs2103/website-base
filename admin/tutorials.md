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

Module | Venue | Time | ~~%%Tutorial ID<br>in LumiNUS%%~~<br>==(don't use this!)== | **Our Tutorial ID**<br>==(use this!)== | Tutors<br>([contact details]({{ instructors_page }}))
-------|-------|------|------------------------------------------------------------|----------------------------------------|-------
<include src="tutorial-schedule-{{ module }}-S{{ S }}.mbdf" inline />

</div>
</panel>

<panel type="seamless" header="### Tutorial Structure" expanded >
<div id="tutorialStructure">

**What happens during the tutorial**:

* A tutorial group is handled by two tutors. Each tutor will work with two teams.
* The tutor will _facilitate_ tutorial activities, observe your progress, and give feedback. If you are facing difficulties with a weekly activity, the tutor can direct you to get help from another student in the tutorial.

* Please ==bring your laptop to tutorials.== You'll need it for tutorial tasks.

<div class="indented-level2">
{{ embed_topic("appendixC-faq.md#admin-faq-noLaptop", "Admin " + icon_embedding + " Appendix C(FAQ): What if I don't carry around a laptop?", "4") }}
</div>

<br/>

**The role of our tutors** is different from tutors in other modules.

* **No direct tech help**: Tutors are prohibited from giving direct technical help, other than to give you some general direction to finding a solution. %%Rationale: We want you to learn the vital survival skill of troubleshooting technical problems.%%

<div class="indented-level2">
{{ embed_topic("appendixD-help.md#main", "Admin " + icon_embedding + " Appendix D: How to get Help in " + module_pair, "2") }}
</div>

<br/>

* **No ‘teaching’**: Tutors are prohibited from “teaching” concepts that are covered in lectures or other learning resources given to you as self-learning is a vital part of the module. For example, ==the tutor will not do a mini-lecture at the start of the tutorial==. Of course tutors can help you clarify doubts under the right circumstances.

<div class="indented-level2">
{{ embed_topic("appendixD-help.md#questions-for-tutros", "Admin " + icon_embedding + " Appendix D (extract): Questions suitable for tutor", "2") }}
</div>

<br/>

* **No leading from the front**: Tutors are not expected to lead your project effort. They will not tell you how to do project tasks or when to do project tasks. You have to figure those out yourselves. But tutors will give you feedback on how you are doing (or have done) project tasks so that you can improve further.   

**Timing/venue:**

* Please refer to the {{ schedule_link }} for further details on each tutorial.
* You are expected to arrive on time. ==Punctuality is considered for participation marks.==
* You may leave the class 15 minutes before the hour if you have another class right after. There is no need to wait till the tutor dismisses you. However, inform the tutor (as a courtesy) before leaving if you leave before the class is dismissed.
* ==Vacate the table 5 minutes before the hour== so that the next group can start on time.
* In the past, many students have requested to increase the tutorial duration because a mere hour is barely enough to get through all the tutorial tasks. Increasing the tutorial time is not possible due to lack of venues and tutors. Instead, let's try to make the best of the one hour available by coming well prepared and starting on time. Note that ==the better prepared you are, the higher the chance of completing e all activities allocated to a tutorial== within time.

**Grading:**

* Your conduct in tutorials will be evaluated by team members and the tutor which can affect your participation marks.

</div>
</panel>
</div>

{% endcall %}
