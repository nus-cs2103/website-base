{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-teams") %}
<div id="main">

<pic eager src="{{baseUrl}}/admin/images/team.png" width="300px"></pic><br>
<small>%%[Picture: The team that was at the top of early Google]%%</small>
<p/>

#### When to form teams
{% set session = "tutorial" %}
**Teams will be formed around Weeks 2-3.** We'll let you know more details closer to the time.

#### Team composition constraints

**We allow some freedom in choosing team members**, subject to these constraints:

* **The default ==team size is five==.**
* **All team members should be in the same tutorial.** ==Delay forming teams until your place in a tutorial is confirmed.== We do not allow changing tutorials to team up with your preferred teammates.
* **Teams of a single nationality are not allowed** unless the only language common among all team members is English, e.g., an all-Singaporean team that includes both Chinese and Malay students. %%Rationale: to train you to work in multicultural teams and to ensure that English is used for all project communication.%%
* **No more than one exchange student per team.** %%Rationale: to increase interaction between exchange students and NUS students.%%{% if cs2113 %}
* **Same-gender teams are discouraged but allowed.** %%Rationale: to train you for mixed-gender work environments.%%{% endif %}
* **If you prefer not to form teams yourselves**, don't worry; we'll place you in a team.<br>
  **If you do not have enough team members**, we'll help fill the vacancies.
* **We may modify teams** when circumstances require it. You cannot object to such changes. Staying with your preferred team is not guaranteed.

{% if cs2103 %}<div id="submitting-formed-teams">

#### How to form teams

* **You may form teams of up to five members** on your own. You are #r#not allowed to form six-person teams on your own##.
* **You may form partial teams** (i.e., with two, three, or four members). We'll add more members to fill the remaining vacancies.
* **The teaching team can add more members to your team**, up to a team size of six. Therefore, even if you form a five-person team, we may assign you a sixth member.
* #r#**All five-member teams you form yourselves must comply with the nationality constraint**## stated above unless it is impossible for you to do so (i.e., all remaining students in your tutorial group do not satisfy the constraint).<br>
  Partial teams (i.e., with four or fewer members) are encouraged to comply with the nationality constraint to reduce the likelihood that the teaching team will dissolve them.
* **Ensure you have the consent of all proposed team members** before submitting the team details.
* Submission:
  * **==Submit your team details through the Canvas form==**, which will open early in Week 2. We'll announce it when it opens.
  * Only one person need to submit on behalf of the entire team. Coordinate among the team members to avoid double-submissions.
  * Please ensure the team member names you specify match their name as shown in Canvas (reason: these submissions are processed by a script).
  * {{ faq }} What if there is a change after we submit the team details?<br>
    **A:** The same person should resubmit the form with the updated details (Canvas does not allow you to edit previous submissions).
</div>
{% endif %}

<div id="teamIdFormat">

#### Team ID

* **Your team ID will be given to you after teams are formed.**
* **It has the form `TUTORIAL_ID-TEAM_NUMBER`**, e.g., `{{ course }}-W14-2` means you are in tutorial `{{ course }}-W14` (i.e., in course `{{ course }}`, on `Wednesday`, at `1400-1500`), team `2`.

<div class="indented-level1">

{{ embed_topic("tutorials.md#tutorialTimetable", "Admin " + icon_embedding + " Tutorials → Tutorial IDs", "3") }}
</div>
<p>

</div>
<div id="teamCommunication" tags="m--cs2103 m--cs2113">

#### Team communications

* **Use English** for all team communications, both spoken and written.
* **We recommend at least one 1-2-hour ==synchronous (online or F2F)== project meeting per week**, in addition to any asynchronous communication. %%Reason: Having all members available at the same time makes collaboration easier and supports more peer learning.%%
  <!--* **We recommend at least one 1-2 hour ==face-to-face== project meeting per week**, in addition to any online meetings. %%Reason: you need to know how to run both types of project meetings%%. The project meeting time can be used to discuss project related things, but also, can be used as a time for team members to work on the project tasks individually (having all members in the same place will facilitate easier collaboration and more peer-learning).-->

  * **Fix a weekly 1-2 hour time slot for project meetings** after the team has been finalized (latest by the end of the week 3 {{ session }}). ==All members are expected to attend weekly project meetings== (not doing so could lower the peer evaluation ratings you receive, which in turn will be factored into your grade). You should also choose a venue if you prefer F2F meetings.
  * {{ icon_tip }} **The best time for the weekly project meeting** is the period from {{ date_first_lecture | date(format_full_day, 1) }} to {{ date_first_lecture | date(format_full_day, 4) }}, i.e., soon after the
{{ lecture_name }} but well ahead of the deadline for weekly tasks. %%Reason: _After_ the {{ lecture_name_short }} → so that you've been briefed about upcoming project tasks; _well ahead of_ the deadline → so that you can use the meeting to plan or do weekly project tasks.%%<br>
    But it's OK to choose a time slot outside that recommended period if you cannot find a suitable time within it.

</div>
</div>

{% endcall %}
