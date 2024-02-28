{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import embed_topic, show_as_tab, timing_badge with context %}
{% from "common/topics.njk" import  panopto with context %}

{% call show_admin_page("courseBriefings") %}
<div id="main">

<p class="lead text-secondary"><em>Course briefing videos</em> cover general admin instructions and aim to guide you on important components of the course.</p>

**Course briefings are delivered as pre-recorded videos**, so that they can be made shorter, and you can speed-watch them if you wish, to save time.

**Most course briefing videos are categorized MUST-WATCH** as they contain important information that you need to know to increase your effort-to-gain ratio, and get the best out of this course.

**They are listed below for reference only.** When it is time for you to watch a certain course briefing video, it will appear in the current schedule page of the course website.<br>
**We track their viewership** and remind when you don't watch them on time.

<!-- ==================================================== -->

<panel type="info" header="#### Week 2 Course Briefings" expanded>
<div id="course-briefing-w2">

****1. Welcome to the Course****:{.text-info}
{{ panopto(desc="1 min", "5503e0be-24bb-4ba2-807f-b0fb01057eb9") }}

<span class="text-info">****2. Course Goals****</span>: How the goals of this course shape the way it is run (possibly different from other courses), and how it should be approached by students.
{{ panopto(desc="9 mins", "a4d6f92e-b12f-4046-853b-b0fb01058143") }}

<div class="indented-level2">

---

<span class="text-info">****2.a. Detour: SDLC Basics****</span>: At this point, watch the following video covering the [week 2 topic 'SDLC Process Models Basics'](topics.html#W2-2), as the concepts covered in there are referenced in the rest of the course briefing.
{{ panopto(desc="6 mins -- %%Detour: **SDLC Basics**%%", "84a0119c-8f76-46fc-a256-b0f90098e59f") }}

---
</div>


<span class="text-info">****3. Iterative + Brownfield = ???****</span>: How the iterative and brownfield approach taken by the course impacts your learning experience.
{{ panopto(desc="6 mins", "e074cbed-2afb-46f6-81bc-b0fb01057eb8") }}

<span class="text-info">****4. Challenges and Solutions****</span>: How to tackle three challenges you'll face in the course, namely, _information overload_, _workload_, and _technical problems_.
{{ panopto(desc="12 mins", "b98f7669-e5e1-4659-847e-b0fb01057ebc") }}

---

<span class="text-info">****5. First weekly briefing****</span>: As this is the first such weekly briefing, **it also covers some general points relevant to all future weeks**.

{{ panopto(desc="8 mins", "f8088218-b6d5-4cc5-a933-b0fb01057ec2") }}
</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### Week 3 Course Briefings" expanded>
<div id="course-briefing-w3">


****CS2103/T Pitfalls (and how to avoid them)****{.text-info}

{{ panopto(desc="9 mins", "036e3b1c-3cf0-446e-9281-b100012b50da") }}

</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### Week 4 Course Briefings" expanded>
<div id="course-briefing-w4">


****tP Briefing (Part 1 -- Getting Started)****{.text-info}

{{ panopto(desc="9 mins", "ecf50649-072a-416b-8382-b10900fd2f81") }}

</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### Week 7 Course Briefings" expanded>
<div id="course-briefing-w7">

<box type="warning" header="Noticed anything odd about the videos below?" seamless>

As you watch the videos below, you might realize that while the voice is 'sort of' like prof's, the accent is certainly different from prof's. This is because in these videos we used an ==AI-driven text-to-speech tool== to create the narrations, as an experiment.
</box>

****tP Briefing (Part 2a -- v1.1, Workflow)****{.text-info}


{{ panopto(desc="9 mins", "3de4b41b-758d-4784-aa26-b11e00f29217") }}

****tP Briefing (Part 2b -- v1.2-v1.4, PE, Grading, Workload)****{.text-info}

{{ panopto(desc="11 mins", "caa70bbc-8869-4f8b-a898-b11f00a3fd5a") }}

</div>
</panel>

<!-- ==================================================== -->

<panel type="info" header="#### More ..." expanded>
<div id="course-briefing-w4">

More course briefing videos (covering the exam, etc.) will be added in due course.

</div>
</panel>

</div>
{% endcall %}
