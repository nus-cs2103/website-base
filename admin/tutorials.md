{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tutorials") %}
<div id="main">

<panel type="seamless" expanded >
<span slot="header" class="card-title"><markdown>### Tutorial Timetable</markdown></span>
<div id="tutorialTimetable">

<box>

{{ icon_important_big_red }} Our tutorial IDs are different from Canvas. Format: `{{ course }}{{ "T" if cs2103 }}-W11` means a tutorial of `{{ course }}{{ "T" if cs2103 }}` course, held on `Wednesday` at `1100`, and so on.<br>
If there are parallel slots for the same course code, a suffix of `a` or `b` is added e.g., `{{ course }}{{ "T" if cs2103 }}-W11a`

</box>

<box type="info" tags="m--cs2103" header="****Zoom Links & Venue****" id="venue-and-links" icon=":fas-info-circle:">

**The first two tutorials (i.e., weeks 3 and 4) will be conducted fully online (via Zoom).**
{% if (current_week | int) <= 4 %}
* Zoom links for tutorial sessions will be available in [Canvas course homepage]({{ url_canvas_home }}), from week 3 Tuesday %%(i.e., 1 day before the first tutorial of the semester)%%.<br>
* You may use the tutorial venue (given in the table below) to join the Zoom session if you wish, but if you do,
    * please keep noise level low, as there will be other students doing the same.
    * while you may sit together with team members, you should ==participate in the tutorial _individually_== e.g., do not project one person's screen to the TV, or discuss answers with others unless the tutor prompts you to.
    * if you face Wi-Fi connectivity issues, try connecting to SSID `eduroam` (you need to use your full NUSNET email address and password `e____@u.nus.edu/*****` to login).
{% endif %}

**The subsequent tutorials will be conducted in F2F mode**. {% if (current_week | int) <= 4 %}More info coming soon ...{% else %}Note the following about F2F tutorials:


* The venue is given in the table below.
* We will be using Zoom in F2F tutorials as well (same Zoom link as before, given in [Canvas course homepage]({{ url_canvas_home }})), as it's needed for,<br>
  (a) screen-sharing the slides,<br>
  (b) collecting answers via PM or polls,<br>
  (c) recording the tutorial for your future reference.
* As before, some parts of the tutorial are to be done individually while some parts will involve discussions.<br>
  Please help to keep the noise level low (as there are two parallel tutorials in the same venue),<br>
  (a) by limiting conversations to parts that the tutor directs you to have a discussion,<br>
  (b) and not speaking too loudly during those discussions.
* {{ icon_Q }} FAQ: Are you allowed to attend the tutorial via Zoom instead?<br>
  Answer: By default, no.<br>
  Reason: it goes against the purpose of F2F tutorials (i.e., to get the whole team to meet physically) and the NUS directive to move all small classes to F2F mode.<br>
  However, you can request (by emailing `{{ course | lower }}@comp.nus.edu.sg`) to attend the tutorial of a specific week via Zoom, if you have a valid reason (e.g., MC, taking part in an NUS-related event).<br>
  {{ icon_Q }} FAQ: What happens if I join a tutorial via Zoom, without getting permission to do so?<br>
  There is no penalty, but that tutorial will not count for participation. See [here](participation.html#:~:text=Sufficient%20tutorial%20attendance/participation) for the bar you need to meet for tutorial participation.
* If you face Wi-Fi connectivity issues, try connecting to SSID `eduroam` (you need to use your full NUSNET email address and password `e____@u.nus.edu/*****` to login).{% endif %}
</box>

<include src="../_course-{{ course }}/timetables-fragment.md#tutorials-s{{ S }}" optional />

</div>
</panel>

<panel type="seamless" header="### Tutorial Structure" expanded >
<div id="tutorialStructure">

**The mode**

{% if cs2113 %}* Tutorials will be conducted in F2F, on campus.{% else %}
* The initial few tutorials will be through Zoom; the rest will be F2F.{% endif %}
* A tutorial group is handled by two tutors. Each tutor will work with two teams.
* Zoom will be used (even during F2F tutorials) for projecting slides and {% if cs2113 %}(occasionally) {% endif %}collecting chat responses.
* MS Teams will be used for file sharing.

<br/>
<div tags="m--cs2103">

**Slides and tutorial recordings**:
* The Zoom recording of a tutorial will be made available to you after the tutorial.
* <span class="text-danger">Slides used in tutorials will not be distributed to students.</span> You are expected to take notes (or screenshots) during the tutorial as necessary. Reasons:
  1. Tutorial slides are meant to help the tutor deliver the tutorial, and not meant to be used as reference materials for you to study later). ==When some content is suitable as a reference material, we'll provide you a copy of it.==
  1. To encourage some level of active engagement with the materials (e.g., taking notes) which is known to increase retention.
  1. To discourage 'no need to bother now; can look at the slides near the exam' attitude -- because most of the materials covered in tutorials are applicable to the project immediately.
</div>


**The role of our tutors** is different from tutors in other courses.

* **Not a source of admin information**: Given the humongous amount of admin info contained in this course and the fact that it is constantly evolving, tutors may not be aware of the recent subtle changes to the admin information. To safeguard you from receiving incorrect admin info, tutors are prohibited from answering admin queries. If you have an admin query, please post in the [forum]({{ url_forum }}) (or email the prof at `{{ course | lower }}@comp.nus.edu.sg` but only if the question is not appropriate for the forum).

* **No feedback/help for yet-to-be-graded components**: Tutors are prohibited from giving inputs for components not graded yet. %%Reason: work submitted for grading should be your own.%%

* **No direct tech help**: Tutors are prohibited from giving direct technical help, other than to give you some general direction to finding a solution. %%Rationale: We want you to learn the vital survival skill of troubleshooting technical problems.%%

{{ embed_topic(baseUrl+"/admin/appendixD-help.md#main", "Admin " + icon_embedding + " Appendix D: How to get Help in " + course_pair, "2", indent="1") }}

<br/>

* **No ‘mini-lectures’**: Tutors are prohibited from 'teaching' concepts that are covered in the learning resources given to you %%(reason: self-learning is a vital part of the course)%%. For example, ==the tutor will not do a mini-lecture at the start of the tutorial==. But tutors can help you clarify doubts under the right circumstances, as described in the panel below.

{{ embed_topic("appendixD-help.md#questions-for-tutors", "Admin " + icon_embedding + " Appendix D (extract): Questions suitable to ask the tutor", "2", indent="1") }}

<br/>

**Timing/venue:**

* Please refer to the {{ url_schedule }} for further details on each tutorial.
* You are expected to be present on time. ==Punctuality is considered for participation marks.==

<!--
* You may leave the class 15 minutes before the hour if you have another class right after. There is no need to wait till the tutor dismisses you. However, inform the tutor (as a courtesy) before leaving if you leave before the class is dismissed.
* ==Vacate the table 5 minutes before the hour== so that the next group can start on time.
-->

* In the past, many students have requested to increase the tutorial duration because a mere hour is barely enough to get through all the tutorial tasks. Increasing the tutorial time is not possible due to lack of venues and tutors. Instead, let's try to make the best of the one hour available by coming well prepared and starting on time. Note that ==the better prepared you are, the higher the chance of completing all activities allocated to a tutorial== within time.

**Grading:**

* Your conduct in tutorials will be evaluated by team members and the tutor which can affect your participation marks.

**FAQ:**

* Q: What if I can't attend due to a valid reason (e.g., MC)?<br>
  A: The following course policy applies.

{{ embed_topic("policies-fragment.md#policy-validAbsences", "Admin " + icon_embedding + " Policies → Absences due to valid reasons", "4", indent=1) }}

</div>
</panel>
</div>

{% endcall %}
