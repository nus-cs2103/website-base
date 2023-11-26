{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import embed_topic with context %}

{% call show_admin_page("peerEvaluations") %}
<div id="main">

<div id="intro">

This course leverages peer feedback/evaluations in many ways. In particular, we do several rounds of peer evaluations using TEAMMATES.

{{ embed_topic("tools.md#teammates", "Admin " + icon_embedding + " Tools → TEAMMATES", "3", indent="1") }}

{{ icon_important_big_red }} Submitting peer evaluations is compulsory. ==If you routinely miss submitting peer evaluations, you can lose participation marks.==
</div>

<div id="practicePeerEvaluations">
<include src="peerEvaluations-practice-fragment.md" />
</div>

<div id="midtermPeerEvaluations">
<include src="peerEvaluations-midterm-fragment.md" />
</div>

<div id="finalPeerEvaluations">
<include src="peerEvaluations-final-fragment.md" />
</div>

### Session: `Responses to Peer Evaluations`

* This is a chance for you to submit your objections to the ratings you received in the Final Peer Evaluation.

<span id="giving-peer-feedback">

### How peer evaluations are used

* Peer evaluations are rarely used directly to calculate marks. They are mostly used to flag cases that need further investigation.
* When investigating such cases to decide if and how much the marks should be adjusted based on peer evaluations, we consider factors such as the following:
  * Is there a consensus among team members? We do not want an extreme input from one team member to unduly affect the outcome. In many cases, we discard the highest and lowest ratings received before calculating the average.
  * Do the other data points (e.g., LoC written, tutor feedback, commit history) corroborates the peer evaluations?
* In some cases, a lower contribution rating given be peers (even if corroborated by other data) might not affect marks at all  e.g., if the lower contribution still meets the bar for earning full marks for that component.

### Guidelines for giving peer feedback

Giving constructive feedback to others is a valuable skill for software engineers. It is also an intended learning outcome of this course. Half-hearted/trivial feedback will not earn participation marks.

Here are some things to keep in mind:

* Assume you are giving feedback to a colleague, not a friend. Keep the tone of your feedback reasonably professional. Do not use offensive language or slang.
* The feedback should be honest and consistent. Giving positive qualitative feedback (e.g. `Thanks for all the hard work!` and negative ratings (e.g. `Equal share - 40%`) to the same team member is not being honest.
* State your expectations early. All too often students give positive/neutral feedback early (hoping that the team member will improve later) and trash the team member in the final evaluation (because the he/she did not improve as expected). However, this could be confusing to the recipient. It is better to give negative feedback early so that the team member gets a clear signal that he/she needs to improve.

### Guidelines for interpreting contribution ratings

When you receive results of a peer evaluation question about contribution, use it mainly to compare the team view to your own view.
* Example 1:<br>
  _Your view (of your own contribution)_&nbsp;: <span class="text-success">**E+10%**</span> %%i.e., 10% more than an equal share%%<br>
  _Team view (of your own contribution)_: <span class="text-success">**E+8%**</span><br>
  Conclusion: The team's view is quite similar to yours.
* Example 2:<br>
  _Your view (of your own contribution)_&nbsp;: <span class="text-success">**E+15%**</span> %%i.e., 10% more than an equal share%%<br>
  _Team view (of your own contribution)_: <span class="text-success">**E+3%**</span><br>
  Conclusion: The team's thinks you did significantly less than you claimed you did.

</span>

</div>

{% endcall %}
