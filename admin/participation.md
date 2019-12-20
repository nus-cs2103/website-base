{% macro show_main_text() %}
<div id="main">

**To receive full 5 marks allocated for participation, meet the criteria {{ thumb("A", "info") }}, {{ thumb("B", "info") }}, and {{ thumb("C", "info") }}.**

**{{ thumb("A", "info") }} Earn at least half of weekly participation points in at least 10 weeks.**
  * In-lecture quiz:
    * Answered at least 80% of the questions correctly: 2 points
    * Answered 40-80% questions correctly: 1 point
  * Post-lecture quiz:
    * Answered at least 80% of the questions correctly: 3 points
    * Answered 60-80% questions correctly: 2 points
    * Answered 40-60% questions correctly: 1 point
  * Missing compulsory administrative requirements %%e.g., forgot to submit peer evaluations%%: -2 for each miss

<div class="indented">

{{ icon_info }} As the lecture on Week `N` covers topics for Week `N+1`, the Lecture `N`'s in-lecture and post-lecture quiz points are counted for Week `N+1`
</div>

**{{ thumb("B", "info") }} Received good peer evaluations**

<div class="indented">

{{ embed_topic("peerEvaluations.md#peerEvaluation-criteria", "Admin " + icon_embedding + " Peer Evaluations → Criteria", "participation-peerEvals", "3") }}

* -1 for each _professional conduct_ criterion in which you score below average (based on the average of ratings received).
* No penalty for scoring low on _competency criteria_.

In addition, you can receive a bonus marks in the following ways. Bonus marks can be used to top up your participation marks should your marks from the above falls below 5.
* Receiving good ratings for all 10 peer evaluations criteria: 1 mark
* Being very helpful to classmates %%e.g., multiple helpful posts in forum%%: 1 mark

</div>

**{{ thumb("C", "info") }} Tutorial attendance/participation not too low**

<div class="indented">

Low attendance/participation can affect participation marks directly (i.e., attended fewer than 7) or indirectly (i.e., it might result in low peer evaluation ratings).
</div>

{{ thumb("Examples:", "secondary") }}

* Alicia earned 1/2, 3/5, ++2/5++, 5/5, 5/5, 5/5, 5/5, 5/5, 5/5, 5/5, 4/5, 5/5 in the first 12 weeks. As she received at least half of the points in 11 of the weeks, she gets 5 participation marks. Bonus marks are not applicable as she has full marks already.
* Benjamin managed to get at least half of the participation points in 9 weeks only, which gives him 5-1 = 4 participation marks. But he received good peer ratings for all criteria, and hence get a bonus mark to make it 5/5.
* Chun Ming met the participation points bar in 8 weeks only, giving him 5-2 = 3 marks. He lost 2 more marks because he received multiple negative ratings for two criteria, giving him 1/5 participation marks.

<panel type="info" header="##### Where to find your participation marks progress" expanded no-close no-switch >

**Participation marks are available in [this page]({{ participation_marks_page }}).**

* The important column is the <span class="text-monospace">==Weeks Count==</span> column. It tells you how many weeks you have met the bar for the criterion <span class="badge badge-info badge-pill">A</span>). Your target is to hit 10 weeks.
* Participation of a week is usually calculated based on two quizzes. For example, week 4 score is calculated based on,
  * `W4-Q1`: previous week's (i.e., lecture 3) in-lecture quiz
  * `W4-Q2`: previous week's (i.e., lecture 3) post-lecture quiz
* Participation bar for weeks 1-3 have been simplified as follows %%(to account for late enrollments, LumiNUS problems etc.)%%:
  * Week 1: submitted pre-module survey or pre-lecture quiz
  * Week 2: submitted at least one of the quizzes
  * Week 3: did reasonably in both quizzes or did well in one of the quizzes
* Quizzes for Week 4 and thereafter are counted as explained in <span class="badge badge-info badge-pill">A</span> above.

{{ icon_info }} If you have queries about the participation marks, please email `{{ module | lower }}@comp.nus.edu.sg`.
</panel>

</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic, thumb with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("participation", show_main_text) }}
