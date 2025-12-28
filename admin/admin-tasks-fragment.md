{% from "common/admin.njk" import policies, show_admin_summary, topics with context %}
{% from "common/macros.njk" import embed_topic, get_date, show_admin_sections_to_read, show_as_tab, show_faq, show_gm_lesson_link, thumb, timing_badge with context %}
{% from "admin/ip-tasks-fragment.md" import show_xp_page  with context %}
{% from "_course-" + course + "/weeklyAdminTopics-fragment.md" import weekly_admin_topics with context %}
{% from "_course-" + course + "/weeklyAdminTasks-fragment.md" import weekly_admin_tasks with context %}

<span id="teammates-link-recovery-tip">{{ icon_tip }} If you did not receive the submission link, you can get TEAMMATES to resend the link by going to [TEAMMATES link recovery page](https://teammatesv4.appspot.com/web/front/help/session-links-recovery)
  and entering your NUSNET email address (try the `e______@u.nus.edu` before trying the 'friendly' email address). Remember to check your spam folder as well.</span>
{#====================================================================================================================#}
{# Tasks
{#====================================================================================================================#}
<span id="heading_submit_pre_lecture_quiz">Submit prereq topics quiz</span>
<div id="desc_submit_pre_lecture_quiz">

* **Read prerequisite  [{{ show_as_tab('Topics', icon_tab_topics) }}](../schedule/week1/topics.html)** allocated for week 1. **Submit `Week 1 Quiz (aka prereq topics quiz)`** (on Canvas) to demonstrate your grasp of those topics.<br>
   **This quiz counts for participation** (as indicated by the {{ icon_graded }} icon above).

{{ show_faq("whenCanWeSeeQuizAnswers") }}

{{ embed_topic(baseUrl+"/admin/participation.md#main", "Admin " + icon_embedding + " **Participation**", "2", indent="1") }}

</div>
{#====================================================================================================================#}
<span id="heading_set_up_tools">Set up the tools</span>
<div id="desc_set_up_tools">

* Follow the tool <span class="border pe-1 ps-1" style="color:purple">**:fas-hard-hat: Preparation**</span> instructions given in the following panels.

{{ embed_topic(baseUrl+"/admin/programmingLanguages.md#main", "Admin " + icon_embedding + " **Programming Language** (and #r#the Java version you are required to use##)", "2", indent="1") }}
{{ embed_topic("tools.md#github", "Admin " + icon_embedding + " **Tools - GitHub**", "2", indent="1") }}
<div class="indented-level1">
<panel header="**Tools - Git {{ s }}{{ s }}**" minimized>

Installing and configuring Git is covered in {{ show_gm_lesson_link("gitPrep", "T1L2. Preparing to Use Git") }}. No action required until the course schedule reaches that lesson.
</panel>
</div>

{{ embed_topic("tools.md#ide", "Admin " + icon_embedding + " **Tools - IDE**", "2", indent="1") }}

{{ embed_topic("tools.md#communication", "Admin " + icon_embedding + " **Tools - Communication**", "2", indent="1") }}
<div tags="m--tic2002">
{{ embed_topic("tools.md#coursemology", "Admin " + icon_embedding + " **Tools - Coursemology**", "2", indent="1") }}
</div>
</div>
{#====================================================================================================================#}
<span id="heading_submit_pre_course_survey">Submit the pre-course survey</span>
<div id="desc_submit_pre_course_survey">

* **Submit the pre-course survey** (==compulsory== because it collects some important information about you e.g., your GitHub username.) -- will be open on Canvas, by Week 1 Monday.
</div>
{#====================================================================================================================#}
<span id="heading_learn_about_the_course">Learn about the course</span>
<div id="desc_learn_about_the_course">

<box type="tip" seamless>

<include src="../book/about/usage.md#tip-about-popup-url" />
</box>

* Read the following admin info about the course.

{{ embed_topic("usingThisWebsite.md#essential", "Admin " + icon_embedding + " **Using this website [essential info]**", "1", indent="1", type="danger", status="collapsed") }}
{{ embed_topic(baseUrl+"/admin/courseExpectations.md#main", "Admin " + icon_embedding + " **Course expectations and ==topic levels==**", "1", indent="1", type="danger") }}
{{ embed_topic("usingThisWebsite.md#more", "Admin " + icon_embedding + " **Using this website [more info]**", "3", indent="1", type="info", status="collapsed") }}
{{ embed_topic(baseUrl+"/admin/weeklySchedule.md#main", "Admin " + icon_embedding + " **Weekly schedule**", "2", indent="1", type="warning") }}


{{ embed_topic(baseUrl+"/admin/courseOverview.md#main", "Admin " + icon_embedding + " **Course overview**", "4", indent="1", type="success") }}
</div>
{#====================================================================================================================#}
<span id="heading_attend_the_first_lecture">Attend the first {{ lecture_name }}</span>
<div id="desc_attend_the_first_lecture">

* Attend the first {{ lecture_name }} on {{ get_date(date_first_lecture, time='') }}(==**compulsory**==).

{{ embed_topic(baseUrl+"/admin/lectures.md#main", "Admin " + icon_embedding + " **" + lecture_name_upper + "s**", "1", indent="1") }}

</div>
{#====================================================================================================================#}
<span id="heading_follow_the_git_learning_trail">Get started on the Git learning trail</span>
<div id="desc_follow_the_git_learning_trail">

* Get started on learning Git and GitHub (used a lot in this course). The relevant lessons are in the [{{ show_as_tab('Topics', icon_tab_topics) }}](../schedule/week1/topics.html#w1-6-rcs-getting-started-with-git) tab.

</div>
{#====================================================================================================================#}
<span id="heading_submit_first_post_lecture_quiz">Submit weekly quiz</span>
<div id="desc_submit_first_post_lecture_quiz">

* **Read weekly topics** allocated for this week. **Submit the `Weekly Quiz`** (on Canvas) to test your knowledge of those topics.<br>
  Weekly quizzes are counted for [participation]({{ baseUrl }}/admin/participation.html).

{{ show_faq("whenCanWeSeeQuizAnswers") }}
</div>
{#====================================================================================================================#}
<span id="heading_submit_first_coding_exercises">Submit coding exercises via Coursemology</span>
<div id="desc_submit_first_coding_exercises">

* Submit the coding exercises allocated for the current week. Most exercises are auto-graded. Keep trying until the system accepts your code as the correct solution.
* If you encounter problems, post in the [forum]({{ url_forum }}).

{{ embed_topic("tools.md#coursemology", "Admin " + icon_embedding + " **Tools - Coursemology**", "2", indent="2") }}
</div>
{#====================================================================================================================#}
<span id="heading_submit_coding_exercises">Submit coding exercises via Coursemology</span>
<div id="desc_submit_coding_exercises">

* As before, submit the coding exercises allocated for the current week, and any pending exercises from previous weeks.
</div>
{#====================================================================================================================#}
<span id="heading_get_connect_with_comm_channels">Get connected to our communication channels</span>
<div id="desc_get_connect_with_comm_channels">

* If you haven't done so already, follow the 'Preparation' instructions of the following panel, to get connected with the communication channels used by the course.

{{ embed_topic("tools.md#communication", "Admin " + icon_embedding + " **Tools - Communication**", "3", indent="1") }}
</div>
{#====================================================================================================================#}
<span id="heading_submit_post_lecture_quiz">Submit weekly quiz</span>
<div id="desc_submit_post_lecture_quiz">

* **Weekly quiz**: Read weekly topics allocated for this week and submit the weekly quiz before the quiz deadline{% if cs2103 %} %%(i.e., before the following
{{ lecture_name }})%%{% endif %}.
</div>
{#====================================================================================================================#}
<span id="heading_form_teams">[{{ course }} students only] Form teams during the tutorial</span>
<div id="desc_form_teams">

* See the [{{ show_as_tab("Tutorial", icon_tutorial) }}](../schedule/week3/tutorial.html) tab for more info.
</div>
{#====================================================================================================================#}
<span id="heading_form_teams_non_t">Form teams during the tutorial</span>
<div id="desc_form_teams_non_t">

* The teaching team will guide the team forming.
</div>
{#====================================================================================================================#}
<span id="heading_accept_github_invitations">Accept GitHub invitation from the course organization</span>
<div id="desc_accept_github_invitations">

* We will be adding you all to {{ course_org }} github org. **Please accept the invitation sent by GitHub** as you need to be a member of the org for some of the future course activities. If you did not receive the invitation link, you can use the link [https://github.com/orgs/{{ course_org }}](https://github.com/orgs/{{ course_org }}) (==you need to log in to GitHub first== -- otherwise the invitation will not show up).<br>
  {{ icon_tip }} If you are unable to view [this repo](https://github.com/{{ course_org }}/membership-check), you have not joined the org yet.
* Worth `2` participation points
</div>
{#====================================================================================================================#}
<span id="heading_practice_peer_evaluations_on_TEAMMATES">Prelim peer evaluation on TEAMMATES</span>
<div id="desc_practice_peer_evaluations_on_TEAMMATES">

* You should receive the submission link by Monday noon.<br>
  <include src="admin-tasks-fragment.md#teammates-link-recovery-tip" inline />

<div class="indented-level1">

<span class="text-danger">{{ icon_important_big_red }} The deadline for this task is strict</span>, unlike the deadline for other weekly project work.
</div>
{{ embed_topic("peerEvaluations.md#intro", "Admin " + icon_embedding + " Peer Evaluations → Introduction", "3", indent="1") }}
{{ embed_topic("peerEvaluations.md#practicePeerEvaluations", "Admin " + icon_embedding + " Peer Evaluations → Session: Prelim Peer Evaluation", "1", indent="1", status="expanded") }}
{{ embed_topic("appendixB-policies.md#policy-deadlineExtensions", "Admin " + icon_embedding + " **Course Policies → Policy on Deadline Extensions**", "4", indent="1") }}
</div>
{#====================================================================================================================#}
<span id="heading_submit_midterm_feedback_for_the_course">{% if not cs2113 %}[optional]{% endif %} Submit midterm feedback for the course</span>
<div id="desc_submit_midterm_feedback_for_the_course">

* **An anonymous survey to submit feedback about the course and the teaching team** will open on Canvas by Monday. Please take a few minutes to give us your feedback.
</div>
{#====================================================================================================================#}
<span id="heading_submit_midterm_peer_evaluations">Submit midterm peer evaluations on TEAMMATES</span>
<div id="desc_submit_midterm_peer_evaluations">

* **Midterm Peer Evaluation** will open on TEAMMATES. You will receive the submission link by {{ get_date(date_w7_start, 5, time='10:00') }}.<br>
  <include src="admin-tasks-fragment.md#teammates-link-recovery-tip" inline />

{{ embed_topic("peerEvaluations.md#midtermPeerEvaluations", "Admin " + icon_embedding + " Peer Evaluations → Session: Midterm Peer Evaluation", "1", indent="2", status="expanded") }}
</div>
{#====================================================================================================================#}
<span id="heading_submit_final_peer_evaluations">Submit final peer evaluation on TEAMMATES</span>
<div id="desc_submit_final_peer_evaluations">

* Submission will open within one day after the tP final submission (i.e., sometime in {{ date_final_submission | date(format_normal, 1)}}).<br>
  <include src="admin-tasks-fragment.md#teammates-link-recovery-tip" inline />

{{ embed_topic("peerEvaluations.md#finalPeerEvaluations", "Admin " + icon_embedding + " Peer Evaluations → Session: Final Peer Evaluation", "1", indent="2", status="expanded") }}
</div>
{#====================================================================================================================#}
<span id="heading_submit_pe_readiness_quiz">Submit the _PE-Readiness Quiz_</span>
<div id="desc_submit_pe_readiness_quiz">

* Submit this quiz (on Canvas) to confirm that you know important details about the PE.
</div>
{#====================================================================================================================#}
<span id="heading_join_catcher_load_testing">{% if not catcher_load_testing %}~~Take part in the CATcher load testing~~{% else %}Take part in the CATcher load testing{% endif %}</span>
<div id="desc_join_catcher_load_testing">
{% if not catcher_load_testing %}
* This task is not applicable for this semester...
{% else %}
* Attend the live {{ lecture_name }} and take part in the CATcher load/stress testing session that will take place during the first 15 minutes of the
{{ lecture_name_short }}. More instructions will be provided during the {{ lecture_name_short }}.
{% endif %}
</div>
{#====================================================================================================================#}
<span id="heading_submit_reuse_declaration">Submit the declaration about code reuse</span>
<div id="desc_submit_reuse_declaration">

* Submit the Canvas survey to declare that you have followed the proper procedure for reusing/adapting code from elsewhere. You need to submit this ==even if you did not reuse any code==.

<div class="indented-level1">
<panel header="{{ "Admin " + icon_embedding + " Policy on reuse" }}" peek>
<include src="appendixB-policies.md#policy-reuse" />
</panel>
</div>

</div>
{#====================================================================================================================#}
<span id="heading_submit_pe_mode_selection">Submit the PE mode selection</span>
<div id="desc_submit_pe_mode_selection">

* Submit the Canvas survey to declare which mode (i.e., remote or F2F) you intend to use for the PE. The panel below has some information you can use to make the decision.<br>
  Please consider carefully before choosing, and stick to the selected mode afterward --
it will be <span class="text-danger">difficult to change your PE mode after the deadline</span> given above.

<div class="indented-level1">
<panel header="{{ "Admin " + icon_embedding + " tP → PE → Extract (PE modes)" }}" peek>
<include src="tp-pe-fragment.md#pe-mode-info" />

...

<include src="tp-pe-fragment.md#pe-proctoring-info" />
</panel>
</div>

</div>
{#====================================================================================================================#}
<span id="heading_submit_feedback_for_tutors">Submit feedback for tutors</span>
<div id="desc_submit_feedback_for_tutors">

* [Not urgent] **A gentle reminder to submit feedback for your tutor** via the semester-end
 student feedback exercise, if you can spare a few minutes.<br>
  They will be disappointed if only a few students cared enough to give feedback.<br>
* **Please ==don't rate the 'other' tutor==** appearing in the submission form but didn't tutor you.
  That is another tutor teaching in the same time slot as yours.<br>
  In particular, don't give a `Neutral` ratings to that 'unknown' tutor as it can affect their
  performance evaluation.

</div>
{#====================================================================================================================#}
{#====================================================================================================================#}

{% macro show_weekly_admin_tasks(week_num) %}
{{ show_xp_page(week_num, weekly_admin_tasks['week' + week_num], '../../admin/admin-tasks-fragment.md') }}

{% set admin_topics_to_show = weekly_admin_topics['week' + week_num] %}
{% if (admin_topics_to_show | length) != 0 %}
{{ show_admin_sections_to_read(topics, policies, faqs, weekly_admin_topics['week' + week_num], is_flat=false ) }}
{% endif %}
{% endmacro %}
