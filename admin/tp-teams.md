{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-teams") %}
<div id="main">

<img src="{{baseUrl}}/admin/images/team.png" width="300px"><br>
<small>%%[Picture: The team that was at the top of early Google]%%</small>
<p/>

#### When to form teams
{% if not tic4002 %}
{% set session = "lecture" if tic4001 or tic4002 else "tutorial" %}
{% if has_t %}* {{ course }}T: Your team will be formed by the CS2101 side.{% endif %}
* {{ (course + ":") if not tic4001 }} Team forming will be done at the _start_ of the week 3 {{ session }}. If you are not there at the team forming time and others in the class are unaware which team you wanted to be in, we'll have to put you into a team randomly.
{% else %}
* Teams forming will be done during the first lecture.
{% endif %}

#### Team size

* The default ==team size is {{ "four" if tic4001 or tic4002 else "five"}}==.

#### Team composition

{% if tic4001 %}
* **You can either form teams yourselves or let us put you in teams.**
{% elif tic4002 %}
* There are two options:<br>
  Option 1: Everyone stays with their TIC4001 team for TIC4002 as well.<br>
  Option 2: No one is allowed to have their TIC4001 team members in the TIC4002 team.
* One of the two options will be chosen based on a vote. The selection option will apply to the whole class. A mixture is not possible due to the small class size.
{% else %}
* **We allow some freedom in choosing team members**, subject to these constraints:
  * **All team members should be in the same tutorial.** ==Delay forming teams until your place in a tutorial is confirmed.== We do not allow changing tutorials to team up with your preferred team mates.
  * **Teams of a single nationality are not allowed**  unless the only language common among all team members is English. e.g. an all-Singaporean team that include both Chinese and Malay students. %%Rationale: to train you to work in multicultural teams, to ensure that English is used for all project communication%%
  * **No more than one exchange students per team** %%Rationale: to increase interaction between exchange students and NUS students.%%
  * **Same gender teams are discouraged but allowed.** %%Rationale: to train you for mixed-gender work environments.%%
* **If you prefer not to form teams yourselves**, not to worry; we'll put you in a team.
{% endif %}
* **We may have to modify teams** when circumstances call for it. There is no avenue for you to object. Staying with your preferred team is not guaranteed.

</div>
<div id="teamIdFormat">

#### Team ID

* **To be given to you after forming teams.**

{% if tic4001 %}
* **Has the form `{MODULE_CODE}-{TEAM_NUMBER}`** e.g, `{{ course }}-2` means you are in team `2`.
{% elif tic4002 %}
* **Has the form `TIC4002-F18-TEAM_NUMBER`** e.g, `TIC4002-F18-2` means you are in team `2`. The `TIC4002-F18-` prefix is needed to comply with some tools that we'll be using in the course.
{% else %}
* **Has the form `TUTORIAL_ID-TEAM_NUMBER`** e.g, `{{ course }}-W14-2` means you are in tutorial `{{ course }}-W14` (i.e., in course `{{ course }}`, on `Wednesday`, at `1400-1500`), team `2`.

<div class="indented-level2">

{{ embed_topic("tutorials.md#tutorialTimetable", "Admin " + icon_embedding + " Tutorials → Tutorial IDs", "3") }}
</div>
<p>
{% endif %}

</div>
<div id="teamCommunication" tags="m--cs2103 m--cs2113">

#### Team Communications

* **Use English** for all team communications, both spoken and written.
* **We recommend at least one 1-2 hour ==synchronous (online or f2f)== project meeting per week**, in addition to any asynchronous communicating. %%Reason: Having all members available at the same time will facilitate easier collaboration and more peer-learning%%.
  <!--* **We recommend at least one 1-2 hour ==face-to-face== project meeting per week**, in addition to any online meetings. %%Reason: you need to know how to run both types of project meetings%%. The project meeting time can be used to discuss project related things, but also, can be used as a time for team members to work on the project tasks individually (having all members in the same place will facilitate easier collaboration and more peer-learning).-->

  * **Fix a weekly 1-2 hour time slot for project meetings** after the team has been finalized (latest by the end of week 3 {{ session }}). ==All members are expected to attend weekly project meetings== (not doing so could lower the peer evaluation ratings you receive, which in turn will be factored into your grade). You should also fix a venue for the meetings, if you prefer F2F meetings.
  * {{ icon_tip }} **The best time for the weekly project meeting** is the period {{ date_first_lecture | date(format_full_day, 1) }}, {{ date_first_lecture | date(format_full_day, 2) }}, {{ date_first_lecture | date(format_full_day, 3) }}, {{ date_first_lecture | date(format_full_day, 4) }} i.e., soon after the lecture but well ahead of the deadline for weekly tasks. %%Reason: _After_ the lecture → you'll have the knowledge required for upcoming project tasks; _before_ the deadline → you can use the meeting to deal with weekly project tasks.%%

</div>

{% endcall %}
