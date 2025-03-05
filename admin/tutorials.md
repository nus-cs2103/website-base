{% from "common/macros.njk" import embed_topic, show_as_tab, show_faq with context %}
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
* Zoom links for tutorial sessions will be available in [Canvas course homepage]({{ url_canvas_home }}), from week 3 Tuesday %%(i.e., 1 day before the first tutorial of the semester)%%.
* Zoom tutorials require you to **use a video camera**. Use a device with a camera, or have a second device (e.g., hand phone) to use as a video camera.
* You may use the tutorial venue (given in the table below) to join the Zoom session if you wish, but if you do,
    * please keep the noise level low, as there will be other students doing the same.
    * while you may sit together with team members, you should ==participate in the tutorial _individually_== e.g., do not project one person's screen to the TV, or discuss answers with others unless the tutor prompts you to.
    * if you face Wi-Fi connectivity issues, try connecting to SSID `eduroam` (you need to use your full NUSNET email address and password `e____@u.nus.edu/*****` to login).
{% endif %}

**The subsequent tutorials will be conducted in F2F mode**. {% if (current_week | int) <= 4 %}More info coming soon ...{% else %}Note the following about F2F tutorials:


* The venue is given in the table below.
* We will be using Zoom in F2F tutorials as well (same Zoom link as before, given in [Canvas course homepage]({{ url_canvas_home }}))

{{ show_faq("tutorialWhyZoomInF2f", is_compact=1) }}
{{ show_faq("tutorialWhyF2f") }}

* As before, some parts of the tutorial are to be done individually while some parts will involve discussions.<br>
  Please help to keep the noise level low (as there are two parallel tutorials in the same venue),<br>
  (a) by limiting conversations to parts that the tutor directs you to have a discussion,<br>
  (b) and not speaking too loudly during those discussions.

{{ show_faq("tutorialByZoom", is_compact=1) }}
{{ show_faq("tutorialZoomWithoutPermission", is_compact=1) }}
{{ show_faq("tutorialCannotReachInTime") }}
<panel header="**Facing ==Wi-Fi issues== while in NUS?**" minimized>

Try connecting to SSID `eduroam` (you need to use your full NUSNET email address and password `e____@u.nus.edu/*****` to login).

If you continue to face recurring Wi-Fi issues at certain NUS locations while your friends don't seem to have such problems, the problem may be specific to your notebook. Workarounds:
  * Connect the notebook to the Wi-Fi hotspot of your mobile device -- but this will add up your mobile data usage.
  * Use a Wi-Fi dongle -- these have worked for some students, and are generally cheap ($10-20).
</panel>
{% endif %}
</box>

<include src="../_course-{{ course }}/timetables-fragment.md#tutorials-s{{ S }}" optional />
{% if cs2103 %}<include src="../_course-{{ course }}/timetables-fragment.md#modals" optional />{% endif %}

</div>
</panel>

<panel type="seamless" header="### Tutorial Structure" expanded >
<div id="tutorialStructure">

##### The mode

{% if cs2113 %}* Tutorials will be conducted in F2F, on campus.{% else %}
* The initial few tutorials will be through Zoom; the rest will be F2F.{% endif %}
* A tutorial group is handled by two tutors. Each tutor will work with two teams.
* Zoom will be used (even during F2F tutorials) for projecting slides and {% if cs2113 %}(occasionally) {% endif %}collecting chat responses.
* MS Teams will be used for file sharing.

<br/>

##### Slides{% if cs2103 %} and recordings

* The Zoom recording of a tutorial will be made available to you after the tutorial.{% endif %}
* <span class="text-danger">Slides used in tutorials will not be distributed to students.</span> You are expected to take notes (or screenshots) during the tutorial as necessary. Reasons:
  1. Tutorial slides are meant to help the tutor deliver the tutorial, and not meant to be used as reference materials for you to study later). ==When some content is suitable as a reference material, we'll provide you a copy of it.==
  1. To encourage some level of active engagement with the materials (e.g., taking notes) which is known to increase retention.
  1. To discourage 'no need to bother now; can look at the slides near the exam' attitude -- because most of the materials covered in tutorials are applicable to the project immediately.

##### Tutor's role

The role of our tutor's is different from tutors in other courses.

* **Not a source of admin information**, as per the course policy given below:

{{ embed_topic("policies-fragment.md#policy-adminQuestions", "Admin " + icon_embedding + " Policies → **Policy on admin questions**", "1", indent=1) }}

* **No feedback/help for yet-to-be-graded components**: Tutors are prohibited from giving inputs for components not graded yet, as per the course policy given below:

{{ embed_topic("appendixB-policies.md#policy-feedbackOnProjectWork", "Admin " + icon_embedding + " **Policy on feedback for project work**", indent=1, level=2) }}

* **No direct tech help**: Tutors are prohibited from giving direct technical help, other than to give you some general direction to finding a solution.

{{ show_faq("tutorialWhyTutorCannotGiveTechHelp") }}


{{ embed_topic(baseUrl+"/admin/appendixD-help.md#main", "Admin " + icon_embedding + " Appendix D: **How to get Help** in " + course_pair, "2", indent="1") }}

* **No ‘mini-lectures’**: Tutors are prohibited from 'teaching' concepts that are covered in the learning resources given to you %%(reason: self-learning is a vital part of the course)%%. For example, ==the tutor will not do a mini-lecture at the start of the tutorial==. But tutors can help you clarify doubts about topics covered in the tutorial.

{{ show_faq("tutorialWhatTutorsCanAnswer", is_compact=1) }}

##### Timing/venue:

* Please refer to the {{ url_schedule }} (click on the {{  show_as_tab("Tutorial", icon_tutorial) }} tab) for further details on each tutorial.

<!--
* You may leave the class 15 minutes before the hour if you have another class right after. There is no need to wait till the tutor dismisses you. However, inform the tutor (as a courtesy) before leaving if you leave before the class is dismissed.
* ==Vacate the table 5 minutes before the hour== so that the next group can start on time.
-->

{{ show_faq("tutorialLength") }}

##### Grading:

* Your conduct in tutorials will be evaluated by team members and the tutor which can affect your [Participation marks](participation.md).
* You are expected to be present on time. ==Punctuality is considered for participation marks.==

{{ show_faq("tutorialWhatIfMissedDueToValidReason", is_compact=1) }}
{{ show_faq("tutorialWhatIfMissedDueToOtherReason") }}

</div>
</panel>
</div>

{% endcall %}
