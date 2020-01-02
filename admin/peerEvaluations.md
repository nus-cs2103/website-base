{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import embed_topic with context %}

{% call show_admin_page("peerEvaluations") %}
<div id="main">

<div id="intro">

This module leverages peer feedback/evaluations in many ways. In particular, we do several rounds of peer evaluations using TEAMMATES.

{{ embed_topic("tools.md#teammates", "Admin " + icon_embedding + " Tools → TEAMMATES", "3", indent="1") }}

{{ icon_important_big_red }} Submitting peer evaluations is compulsory. ==If you routinely miss submitting peer evaluations, you can lose participation marks.==
</div>

<div id="practicePeerEvaluations">
<include src="peerEvaluations-practice.mbdf" />
</div>

<div id="midtermPeerEvaluations">
<include src="peerEvaluations-midterm.mbdf" />
</div>

<div id="finalPeerEvaluations">
<include src="peerEvaluations-final.mbdf" />
</div>

### Session: `Responses Peer Evaluation`

* This is a chance for you to submit your objections to the ratings you received in the Final Peer Evaluation

<span id="giving-peer-feedback">

### Guidelines for Giving Peer Feedback

Giving constructive feedback to others is a valuable skill for software engineers. It is also an intended learning outcome of this module. Half-hearted/trivial feedback will not earn participation marks.

Here are some things to keep in mind:

* Assume you are giving feedback to a colleague, not a friend. Keep the tone of your feedback reasonably professional. Do not use offensive language or slang.
* The feedback should be honest and consistent. Giving positive qualitative feedback (e.g. `Thanks for all the hard work!` and negative ratings (e.g. `Equal share - 40%`) to the same team member is not being honest.
* State your expectations early. All too often students give positive/neutral feedback early (hoping that the team member will improve later) and trash the team member in the final evaluation (because the he/she did not improve as expected). However, this could be confusing to the recipient. It is better to give negative feedback early so that the team member gets a clear signal that he/she needs to improve.

</span>

</div>

{% endcall %}
