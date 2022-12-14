{% from "common/macros.njk" import embed_topic, show_as_tab, thumb with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("participation") %}
<div id="main">

**To receive full {{ marks_participation}} marks allocated for participation, meet the criteria {{ thumb("A", "info") }}, {{ thumb("B", "info") }}, and {{ thumb("C", "info") }}.**

****{{ thumb("A", "info") }} Earned more than half of weekly participation points in at least 10 weeks.****
<div tags="m--cs2103 m--cs2113">

  * Weekly quiz(es), if any:
    * Quizzes open around the lecture time and stay open until the next lecture starts. In some weeks, there will be two quizzes %%(because two smaller quiz is easier for you to manage than one big quiz)%%.
    * If multiple attempts are allowed, we take the _best_ attempt, not the _latest_ attempt.
    * When awarding participation points for quizzes, we look for two conditions:
      * Condition 1: submitted **__early__** i.e., within four days of the lecture i.e., lecture day (Friday) + three more days -> Monday %%(reason: to encourage learning the weekly topics _before_ doing the weekly tasks)%%
      * Condition 2: answered **__correctly__** i.e., least 70% of the answers are correct %%(reason: to discourage random answers)%%
    * You earn:
      * 3 points if you satisfy both conditions.
      * 2 points if only one of the conditions is satisfied.
      * 1 point if submitted but both conditions are not satisfied.{% if cs2113 %}
  * Weekly programming exercise (if any):
    * 3 points if you submitted correct solutions for at least 75% of the exercises
    * 2 points if you submitted correct solutions for 50-74% of the exercises
    * 1 point if you submitted correct solutions for 25-49% of the exercises{% endif %}
  * TEAMMATES peer evaluation sessions: 2 points per session
  * Other weekly activities:
    * There could be other activities related to the lecture, tutorial, or the administration of the module.
    * Refer the activity description for evaluation criteria.
    * Each activity earns 2 points unless specified otherwise.
</div>

<div tags="m--tic4001 m--tic4002">

  * Weekly quiz(es):
    * Quizzes open around the lecture time and stay open until the next lecture starts.
    * If multiple attempts are allowed, we take the _best_ attempt, not the _latest_ attempt.
    * When awarding participation points for quizzes, we look for two conditions:
      * Condition 1: submitted **__early__** i.e., within four days of the lecture i.e., lecture day + three more days %%(reason: to encourage learning the weekly topics _before_ doing the weekly tasks)%%
      * Condition 2: answered **__correctly__** i.e., least 70% of the answers are correct %%(reason: to discourage random answers)%%
    * You earn:
      * 3 points if you satisfy both conditions.
      * 2 points if only one of the conditions is satisfied.
      * 1 point if submitted but both conditions are not satisfied.
  * Other weekly activities:
    * There could be other activities related to the lecture, or the administration of the module.
    * Refer the activity description for evaluation criteria.
</div>

<div class="indented">

<span tags="m--cs2113">

{{ icon_info }} Lecture in week `N`:
* In-lecture quiz and other activities are counted for week `N` lecture participation.
* Post-lecture quiz (if any) is counted for Week `N+1`
</span>
</div>

****{{ thumb("B", "info") }} Received good peer evaluations****

<div class="indented">

* -1 for each _professional conduct_ criterion in which you score below average (based on the average of ratings received).
{{ embed_topic("peerEvaluations-midterm-fragment.md#teamMemberEvaluation-conduct", "Admin " + icon_embedding + " Peer Evaluations → Criteria (Conduct)", "3", indent=2) }}


* No penalty for scoring low on _competency criteria_.
{{ embed_topic("peerEvaluations-midterm-fragment.md#teamMemberEvaluation-competency", "Admin " + icon_embedding + " Peer Evaluations → Criteria (Competency)", "3", indent=2) }}


</div>

****{{ thumb("C", "info") }} {{ "Lecture" if tic4002 else "Tutorial" }} attendance/participation not too low****

<div class="indented">

Low attendance/participation can affect participation marks directly (i.e., attended fewer than 7) or indirectly (i.e., it might result in low peer evaluation ratings).
</div>

<panel type="info" header="**+ Bonus Marks**" expanded no-close no-switch >

In addition, you can receive bonus marks in the following ways. Bonus marks can be used to top up your participation marks ==but only if your marks from the above falls below {{ marks_participation }}==.
* [For lecture participation] Participated in lecture activities (e.g., in lecture polls/quizzes) in at least 8 lectures: 1 mark{% if cs2103 %}
* [For in-video quizzes] Answered in-video quizzes in at least 7 weeks: 1 mark<br>
  {{ icon_info }} <span id="in-video-quiz-info">Starting from week 3, some pre-recorded lecture videos in the <span class="text-primary">{{ show_as_tab('Topics', icon_tab_topics) }}</span> tab will contain in-video quizzes. Videos containing quizzes are labelled <span class="badge rounded-pill bg-danger"><big>{{ icon_video }} Video</big></span> <span class="badge rounded-pill bg-warning text-dark"><big>Q+</big></span> (instead of the usual <span class="badge rounded-pill bg-danger"><big>{{ icon_video }} Video</big></span>)</span>{% endif %}
* [For perfect peer ratings] Received good ratings for all 10 peer evaluations criteria: 1 mark
* [For helping classmates] Was very helpful to classmates %%e.g., multiple helpful posts in forum%%: 1 mark

</panel>
<p/>

{% if marks_participation == "5" %}
{{ thumb("Examples:", "secondary") }}

* Alicia earned 1/2, 3/5, !!2/5!!, 5/5, 5/5, 5/5, 5/5, 5/5, 5/5, 5/5, 4/5, 5/5 in the first 12 weeks. As she received at least half of the points in 11 of the weeks, she gets 5 participation marks. Bonus marks are not applicable as she has full marks already.
* Benjamin managed to get at least half of the participation points in 9 weeks only, which gives him 5-1 = 4 participation marks. But he participated in 10 lectures, and hence get a bonus mark to make it 5/5.
* Chun Ming met the participation points bar in 8 weeks only, giving him 5-2 = 3 marks. He lost 2 more marks because he received multiple negative ratings for two criteria, giving him 1/5 participation marks.
{% endif %}

<panel type="info" header="##### Where to find your participation marks progress" expanded no-close no-switch >

**Your participation progress can be tracked in [this page]({{ url_participation_dashboard }})** from week 3 onward.
</panel>

</div>

{% endcall %}
