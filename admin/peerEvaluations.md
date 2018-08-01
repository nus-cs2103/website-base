{% macro show_main_text() %}
<div id="main">

We use the [TEAMMATES](http://teammatesv4.appspot.com/) online peer evaluation system to conduct several rounds of peer-evaluations.
All peer evaluations will be taken into account when determining your participation marks. The system also allows you to give anonymous feedback to your teammates.

<span id="extra-requirements">

**Extra Requirements:** [considered for participation marks]

* :exclamation: Submitting peer evaluations is compulsory. ==If you routinely miss submitting peer evaluations, you can lose participation marks.==
* :bulb: TEAMMATES normally allows students to access it without using Google login. In this module, we encourage (but not require) you to login to TEAMMATES using your Google account and complete your profile with a <trigger trigger="click" for="modal:peerEvaluations-suitablePhoto">suitable profile photo</trigger>. %%Reason: {{ module_pair }} is a big class. This profile helps us to remember you better, even after the module is over.%%

<modal title="%%Admin {{ icon_embedding }} Project → Deliverables → Website (extract)%%" id="modal:peerEvaluations-suitablePhoto">
  <include src="project-deliverables.md#profile-photo" />
</modal>

</span>

<div id="peerEvaluation-criteria">

<big>**Peer evaluation criteria: professional conduct**</big>
* **Professional Communication** : 
  * Communicates sufficiently and professionally. e.g. Does not use offensive language or excessive slang in project communications.
  * Responds to communication from team members in a timely manner (e.g. within 24 hours).
* **Punctuality**: Does not cause others to waste time or slow down project progress by frequent tardiness.
* **Dependability**: Promises what can be done, and delivers what was promised.
* **Effort**: Puts in sufficient effort to, and tries their best to, keep up with the module/project pace. Seeks help from others when necessary.
* **Quality**: Does not deliver work products that seem to be below the student's competence level i.e. tries their best to make the work product as high quality as possible within her competency level.
* **Meticulousness**:
  * Rarely overlooks submission requirements.
  * Rarely misses compulsory module activities such as completing the TEAMMATES profile or peer review.
* **Teamwork**: How willing are you to act as part of a team, contribute to team-level tasks, adhere to team decisions, etc.

  
<big>**Peer evaluation criteria: competency**</big>
* **Technical Competency**: Able to gain competency in all the required tools and techniques.
* **Mentoring skills**: Helps others when possible. Able to mentor others well.
* **Communication skills**: Able to communicate (written and spoken) well. Takes initiative in discussions.
</div>

<span id="giving-peer-feedback">

Giving constructive feedback to others is a valuable skill for software engineers. It is also an intended learning outcome of this module. Half-hearted/trivial feedback will not earn participation marks.

Here are some things to keep in mind:

* Assume you are giving feedback to a colleague, not a friend. Keep the tone of your feedback reasonably professional. Do not use offensive language or slang.
* The feedback should be honest and consistent. Giving positive qualitative feedback (e.g. `Thanks for all the hard work!` and negative ratings (e.g. `Equal share - 40%`) to the same team member is not being honest.
* State your expectations early. All too often students give positive/neutral feedback early (hoping that the team member will improve later) and trash the team member in the final evaluation (because the he/she did not improve as expected). However, this could be confusing to the recipient. It is better to give negative feedback early so that the team member gets a clear signal that he/she needs to improve.

</span>

The final peer evaluation (in week 13) is graded. In that peer-evaluation you will be asked to evaluate the work of your team members and another team. The quality and accuracy of your evaluation will affect your grade and your evaluations will be considered as a data point in determining the grade of the team members.

<img src="{{baseUrl}}/admin/images/peer evaluations.png" width="600px">



</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("peerEvaluations", show_main_text) }}