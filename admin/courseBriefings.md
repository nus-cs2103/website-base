{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import embed_topic, show_as_tab, timing_badge with context %}
{% from "common/topics.njk" import  panopto with context %}

{% call show_admin_page("courseBriefings") %}
<div id="main">

<p class="lead text-secondary"><em>Course briefing videos</em> cover general administrative instructions and highlight important parts of the course.</p>

**Course briefings are delivered as pre-recorded videos** so they can be shorter, and you can watch them at a faster speed to save time if you wish.

**Most course briefing videos are categorized as MUST-WATCH** as they contain important information you need to increase your effort-to-gain ratio and get the most out of this course.

**They are listed below for reference.** When it is time for you to watch a specific course briefing video, it will appear in the current schedule page of the course website.


<!-- ==================================================== -->

<panel type="info" header="#### Week 1 Course Briefings" expanded>
<div id="course-briefing-w1">
<box seamless>

**{{ icon_graded }} Watching course briefing videos counts for participation.**<br>
When watching a briefing video for the first time, avoid <tooltip content="dragging the slider or timeline bar back and forth">scrubbing</tooltip> or jumping around in the video timeline, as this can interfere with the video platform's tracking of which parts of the video you actually watched. However, watching at faster speeds is fine.

**:fas-closed-captioning: We have added closed captioning support** for course briefing videos.

<pic src="images/ccButton.png" />
</box>

****1. Welcome to the Course****:{.text-info}
{{ panopto(desc="1 min", "0daed9ac-c6a5-4c28-9f81-b4a1011018c3", start_week="1") }}

<span class="text-info">****2. How CS2103/T is Different from other courses****</span>: Knowing how the course differs from other typical course will help you navigate it better. {{ icon_graded }}
{{ panopto(desc="4 mins", "8603c97e-1f9e-41cb-9dbe-b4a101103a3c", start_week="1") }}

<span class="text-info">****3. Week 1 Briefing****</span>: As this is the first weekly briefing, **it also covers some general points relevant to all future weeks**. {{ icon_graded }}

{{ panopto(desc="5 mins", "f31df0c1-a01a-4191-a902-b4a1011b10b8", start_week="1") }}
</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### Week 2 Course Briefings" expanded>
<div id="course-briefing-w2">

This week's briefing videos start with a detour.

<div class="indented-level2">

---

<span class="text-info">****0. Detour: SDLC Basics****</span>: Watch the following video covering the [week 2 topic 'SDLC Process Models Basics']({{ baseUrl }}/schedule/week2/topics.html#W2-2), as the rest of the course briefing refers to those concepts. {{ icon_graded }}
{{ panopto(desc="6 mins -- %%Detour: **SDLC Basics**%%", "84a0119c-8f76-46fc-a256-b0f90098e59f", start_week="1") }}

---
</div>

<span class="text-info">****1. Iterative + Brownfield = ???****</span>: How the iterative and brownfield approach used in the course affects your learning experience. {{ icon_graded }}
{{ panopto(desc="6 mins", "c97a1f22-4236-4d17-b004-b4a5005841cb", start_week="1") }}

<span class="text-info">****2. Challenges and Solutions****</span>: How to tackle three challenges you will face in the course: _information overload_, _workload_, and _technical problems_.
{{ panopto(desc="16 mins", "70bdbe1a-c372-48f4-b9b5-b4a40112f693", start_week="1") }}

---

<span class="text-info">****3. Week 1→2 Briefing****</span> (Week 1 Recap + Week 2 Preview): This video recaps Week 1 and gives a preview of what you need to do in Week 2. {{ icon_graded }}<br>
%%Note: While weekly briefings are normally done in hybrid mode, this week's briefing is released as a pre-recorded video so you can start week 2 tasks early.%%

{{ panopto(desc="6 mins", "7418be6b-cece-43df-8858-b4a401197f57", start_week="1") }}
</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### Week 3 Course Briefings" expanded>
<div id="course-briefing-w3">


****CS2103/T Pitfalls (and how to avoid them)****{.text-info} {{ icon_graded }}

{{ panopto(desc="9 mins", "036e3b1c-3cf0-446e-9281-b100012b50da", start_week="2") }}

</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### Week 4 Course Briefings" expanded>
<div id="course-briefing-w4">


****tP Briefing (Part 1 -- Getting Started)****{.text-info}

{{ panopto(desc="9 mins", "ecf50649-072a-416b-8382-b10900fd2f81", start_week="4") }}

</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### Week 7 Course Briefings" expanded>
<div id="course-briefing-w7">

<box type="warning" header="Noticed anything odd about the videos below?" seamless>

In these two videos, we used an ==AI-driven text-to-speech tool== to create parts of the narration as an experiment. See if you can spot the AI-generated parts.
</box>

****tP Briefing (Part 2a -- v1.1, Workflow)****{.text-info} {{ icon_graded }}


{{ panopto(desc="6 mins", "6369aa21-199d-4cab-b1cc-b1ee00b56107", start_week="7") }}

****tP Briefing (Part 2b -- v1.2-v1.6, PE, Grading, Workload)****{.text-info} {{ icon_graded }}

{{ panopto(desc="6 mins", "b7750694-17a9-42a9-b975-b1ee00ae4e9a", start_week="7") }}

</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### Week 13 Course Briefings" expanded>
<div id="course-briefing-w13">

****Final Exam:****{.text-info} This video gives an overview of the final exam structure and resources you can use to prepare for it.

<div id="exam-briefing-video">

{{ panopto("659fa8f5-e1e3-42ba-9452-b4280057bdeb", desc="[Course Briefing Video] Final Exam %%(10 minutes)%%", start_week="12") }}
</div>

****Course Topics Recap, aka the 'Big Picture':****{.text-info} This video explains how course topics fit into the big picture and, as a bonus, ==discusses some exam-like questions==.

<div id="topics-video">

{{ panopto(desc="[Course Briefing Video] Topics overview + ==some exam-like questions== %%(19 mins)%%", "9c609cb0-9037-457f-ad95-b38a00833adb", start_week="12") }}
</div>

</div>
</panel>

<!-- ==================================================== -->

</div>
{% endcall %}
