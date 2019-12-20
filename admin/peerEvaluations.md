{% macro show_main_text() %}
<div id="main">

This module leverages peer feedback/evaluations in many ways. In particular, we do several rounds of peer evaluations using TEAMMATES.

{{ embed_topic("tools.md#teammates", "Admin " + icon_embedding + " Tools → TEAMMATES", "peerEvaluations-teammates", "3") }}

{{ icon_important_big_red }} Submitting peer evaluations is compulsory. ==If you routinely miss submitting peer evaluations, you can lose participation marks.==

<div id="peerEvaluation-criteria">
<box background-color="white" border-color="grey" border-left-color="gold">

#### Peer Evaluation Criteria: Professional Conduct
* **Professional Communication** :
  * Communicates sufficiently and professionally. e.g. Does not use offensive language or excessive slang in project communications.
  * Responds to communication from team members in a timely manner (e.g. within 24 hours).
* **Punctuality**: Does not cause others to waste time or slow down project progress by frequent tardiness.
* **Dependability**: Promises what can be done, and delivers what was promised.
* **Effort**: Puts in sufficient effort to, and tries their best to keep up with the module/project pace. Seeks help from others when necessary.
* **Quality**: Does not deliver work products that seem to be below the student's competence level i.e. tries their best to make the work product as high quality as possible within her competency level.
* **Meticulousness**:
  * Rarely overlooks submission requirements.
  * Rarely misses compulsory module activities such as pre-module survey.
* **Teamwork**: How willing are you to act as part of a team, contribute to team-level tasks, adhere to team decisions, etc. Honors all collectively agreed-upon commitments e.g., weekly project meetings.
</box>
<box background-color="white" border-color="grey" border-left-color="gold">

#### Peer Evaluation Criteria: Competency
* **Technical Competency**: Able to gain competency in all the required tools and techniques.
* **Mentoring skills**: Helps others when possible. Able to mentor others well.
* **Communication skills**: Able to communicate (written and spoken) well. Takes initiative in discussions.
</box>
</div>

<span id="giving-peer-feedback">

#### Guidelines for Giving Peer Feedback

Giving constructive feedback to others is a valuable skill for software engineers. It is also an intended learning outcome of this module. Half-hearted/trivial feedback will not earn participation marks.

Here are some things to keep in mind:

* Assume you are giving feedback to a colleague, not a friend. Keep the tone of your feedback reasonably professional. Do not use offensive language or slang.
* The feedback should be honest and consistent. Giving positive qualitative feedback (e.g. `Thanks for all the hard work!` and negative ratings (e.g. `Equal share - 40%`) to the same team member is not being honest.
* State your expectations early. All too often students give positive/neutral feedback early (hoping that the team member will improve later) and trash the team member in the final evaluation (because the he/she did not improve as expected). However, this could be confusing to the recipient. It is better to give negative feedback early so that the team member gets a clear signal that he/she needs to improve.

</span>

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import embed_topic with context %}
{{ show_admin_page("peerEvaluations", show_main_text) }}
