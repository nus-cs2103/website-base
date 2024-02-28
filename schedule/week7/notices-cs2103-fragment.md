{% from "common/macros.njk" import embed_topic, get_date, show_as_tab, timing_badge with context %}
<box type="info" header="****==Where is the recess week?==****">

* **It's in the middle of week 7**. As you know, {{ course_pair }} week starts early. But we will honor the official timing of the recess week. Think of it like this:
  * `{{ get_date(date_w7_start, 0, time='') }}`: {{ course_pair }} **Week 7 starts**
  * `{{ get_date(date_w7_start, 1, time='') }} -  {{ get_date(date_w7_start, 9, time='') }}`: Recess week (**Week 7 put on hold**)
  * `{{ get_date(date_w7_start, 10, time='') }}`: {{ course_pair }} **Week 7 resumes**
* **Recess week days are omitted from deadline calculations.** For example, the quiz early submission deadline is week 7 Monday ({{ get_date(date_w7_start, 10, time='') }}), not recess week Monday.
* **We have not scheduled any _regular_ course activities during recess week**. But you may be asked to catch up on missed activities in the previous weeks %%e.g., late submissions for the iP%%.
</box>

<panel type="info" header="##### ==[MUST-WATCH]== Course Briefing Segment - tP (Part 2)" expanded >

<include src="../../admin/courseBriefings.md#course-briefing-w7" />

</panel>
<p/>