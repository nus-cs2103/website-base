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

**{{ thumb("B", "info") }} Received <tooltip content="No multiple `Below Average`/`Poor` ratings">good peer evaluations</tooltip>**

<div class="indented">

In addition, you can receive a bonus marks in the following ways. Bonus marks can be used to top up your participation marks should your marks from the above falls below 5.
* Receiving good ratings for all 10 peer evaluations criteria: 1 mark
* Being very helpful to classmates %%e.g., multiple helpful posts in forum%%: 1 mark

<div class="indented">

{{ embed_topic("peerEvaluations.md#peerEvaluation-criteria", "Admin " + icon_embedding + " Peer Evaluations → Criteria", "participation-peerEvals", "3") }}
</div>
</div>

**{{ thumb("C", "info") }} Tutorial attendance/participation not too low**

<div class="indented">

Low attendance/participation can affect participation marks directly (i.e., attended fewer than 7) or indirectly (i.e., it might result in low peer evaluation ratings).
</div>

{{ thumb("Examples:", "secondary") }}

* Alicia earned 1/2, 3/5, ++2/5++, 5/5, 5/5, 5/5, 5/5, 5/5, 5/5, 5/5, 4/5, 5/5 in the first 12 weeks. As she received at least half of the points in 11 of the weeks, she gets 5 participation marks. Bonus marks are not applicable as she has full marks already.
* Benjamin managed to get at least half of the participation points in 9 weeks only, which gives him 5-1 = 4 participation marks. But he received good peer ratings for all criteria, and hence get a bonus mark to make it 5/5.
* Chun Ming met the participation points bar in 8 weeks only, giving him 5-2 = 3 marks. He lost 2 more marks because he received multiple negative ratings for two criteria, giving him 1/5 participation marks.

</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic, thumb with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("participation", show_main_text) }}
