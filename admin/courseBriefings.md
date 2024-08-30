{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import embed_topic, show_as_tab, timing_badge with context %}
{% from "common/topics.njk" import  panopto with context %}

{% call show_admin_page("courseBriefings") %}
<div id="main">

<p class="lead text-secondary"><em>Course briefing videos</em> cover general admin instructions and aim to guide you on important components of the course.</p>

**Course briefings are delivered as pre-recorded videos**, so that they can be made shorter, and you can speed-watch them if you wish, to save time.

**Most course briefing videos are categorized MUST-WATCH** as they contain important information that you need to know to increase your effort-to-gain ratio, and get the best out of this course.

**They are listed below for reference only.** When it is time for you to watch a certain course briefing video, it will appear in the current schedule page of the course website.


<!-- ==================================================== -->

<panel type="info" header="#### Week 1 Course Briefings" expanded>
<div id="course-briefing-w1">
<box seamless>

**{{ icon_graded }} Watching course briefing videos counts for participation.**<br>
When watching a briefing video for the first time, avoid <tooltip content="dragging a slider or timeline bar back and forth">scrubbing</tooltip> or jumping ahead/around in the video timeline, as this can interfere with the video platform's capturing of what part of the video you actually watched. However, watching at faster speeds is fine.

**:fas-closed-captioning: We have added closed captioning support** for course briefing videos.
</box>

****1. Welcome to the Course****:{.text-info}
{{ panopto(desc="1 min", "999708f4-bc1d-45bb-85a3-b1c400342f2c", start_week="0") }}

<span class="text-info">****2. Course Goals****</span>: How the goals of this course shape its structure (possibly different from other courses), and how it should be approached by students.
{{ panopto(desc="9 mins", "a4d6f92e-b12f-4046-853b-b0fb01058143", start_week="0") }}


<span class="text-info">****3. Week 1 Briefing****</span>: As this is the first weekly briefing, **it also covers some general points relevant to all future weeks**.

{{ panopto(desc="4 mins", "267ac3b6-25a9-48cf-b3e3-b1c400f8696c", start_week="0") }}
</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### Week 2 Course Briefings" expanded>
<div id="course-briefing-w2">

This week's briefing videos start with a detour.

<div class="indented-level2">

---

<span class="text-info">****0. Detour: SDLC Basics****</span>: Watch the following video covering the [week 2 topic 'SDLC Process Models Basics']({{ baseUrl }}/schedule/week2/topics.html#W2-2), as the concepts covered in there are referenced in the rest of the course briefing.
{{ panopto(desc="6 mins -- %%Detour: **SDLC Basics**%%", "84a0119c-8f76-46fc-a256-b0f90098e59f", start_week="1") }}

---
</div>


<span class="text-info">****1. Iterative + Brownfield = ???****</span>: How the iterative and brownfield approach taken by the course impacts your learning experience.
{{ panopto(desc="6 mins", "e074cbed-2afb-46f6-81bc-b0fb01057eb8", start_week="1") }}

<span class="text-info">****2. Challenges and Solutions****</span>: How to tackle three challenges you'll face in the course, namely, _information overload_, _workload_, and _technical problems_.
{{ panopto(desc="11 mins", "e23c1d7e-bc39-45ff-98c0-b1cd0079a400", start_week="1") }}

---

<span class="text-info">****3. Week 1->2 Briefing****</span> (Week 1 Recap + Week 2 Preview): This video recaps Week 1 and gives a preview of what you need to do in Week 2.<br>
%%Note: While weekly briefings are normally done in hybrid mode, this week's briefing is released as a pre-recorded video, to allow you to get started with week 2 tasks early.%%

{{ panopto(desc="4 mins", "30dad6c2-bc2f-4918-8122-b1cd0043ede5", start_week="1") }}
</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### Week 3 Course Briefings" expanded>
<div id="course-briefing-w3">


****CS2103/T Pitfalls (and how to avoid them)****{.text-info}

{{ panopto(desc="9 mins", "036e3b1c-3cf0-446e-9281-b100012b50da", start_week="2") }}

</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### Week 4 Course Briefings" expanded>
<div id="course-briefing-w4">


****tP Briefing (Part 1 -- Getting Started)****{.text-info}

{{ panopto(desc="9 mins", "ecf50649-072a-416b-8382-b10900fd2f81", start_week="3") }}

</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### Week 7 Course Briefings" expanded>
<div id="course-briefing-w7">

<box type="warning" header="Noticed anything odd about the videos below?" seamless>

As you watch the videos below, you might realize that while the voice is 'sort of' like prof's, the accent is certainly different from prof's. This is because in these videos we used an ==AI-driven text-to-speech tool== to create the narrations, as an experiment.
</box>

****tP Briefing (Part 2a -- v1.1, Workflow)****{.text-info}


{{ panopto(desc="9 mins", "3de4b41b-758d-4784-aa26-b11e00f29217", start_week="7") }}

****tP Briefing (Part 2b -- v1.2-v1.4, PE, Grading, Workload)****{.text-info}

{{ panopto(desc="11 mins", "caa70bbc-8869-4f8b-a898-b11f00a3fd5a", start_week="7") }}

</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### Week 13 Course Briefings" expanded>
<div id="course-briefing-w13">

****Final Exam:****{.text-info} This video contains an overview of the final exam structure and resources that you can use to prepare for it.

{{ panopto(desc="12 mins", "2ab962b5-554e-41be-9df3-b14f00fd2cb8", start_week="13") }}

****Course Topics Recap aka the 'Big Picture':****{.text-info} This video explains how course topics fit into a big picture, and as a bonus, ==touches on some exam-like questions== as well.

{{ panopto(desc="19 mins", "e1bf94be-36e3-4ab1-8261-b14f00fd2cc9", start_week="13") }}

</div>
</panel>

<!-- ==================================================== -->

</div>
{% endcall %}
