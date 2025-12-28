{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import as_tag, button, embed_topic, get_date, show_as_tab, show_as_rounded_tab, show_faq, show_gm_lesson_link, show_tp_goals, show_tp_week_intro, show_tp_week_outro, show_tp_iterations_gantt, thumb, thumb_small, timing_badge with context %}
{% from "admin/ip-tasks-fragment.md" import show_xp_page  with context %}
{% from "_course-" + course + "/weeklyTpTasks-fragment.md" import weekly_tp_tasks  with context %}
{% from "_course-" + course + "/studentData-fragment.md" import tp_dg_review_allocation with context %}
{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}


{#====================================================================================================================
 # Common fragments
 #====================================================================================================================#}
<div class="indented" tags="m--cs2103" id="feature-freeze-details">

<box type="warning" seamless>

**The goal of freezing features in the pre-release iteration is to minimize latent bugs** by avoiding behavior changes unless they are strictly necessary, so that we minimize the possibility of introducing more bugs.<br>
In a real project, minor or critical changes might be allowed even near a deadline -- but in the tP, it is hard to enforce such a rule objectively. Instead, we enforce a quantitative limit that is easier to enforce: <span class="text-danger">**no more than 10% or 50 LoC (whichever is higher) of the functional code is allowed to be changed during the iteration {{ version_final }}**</span>.<br>
Finer details of this limit are given below (**also see [Q0] and [Q1]** given under FAQs):

* **The feature freeze ==starts at 10am on the PE-D day==.** Any code updated after that deadlines is counted against the feature freeze.
* **The limit is applied per member**. That is, we compare the amount of code attributed to each member (as per the tP code dashboard) against the portion of that code that was changed during the feature freeze. Any penalty for violating the feature freeze will be applied to that member only.
* **The limit applies to functional code only**. More specifically, all changes (including blank lines and comments) to any code file inside the `src\main` folder  and sub-folders. The feature freeze doesn't apply to test code, documentation, or non-code files (e.g., images).
* **The calculation is based on the [tP code dashboard]({{ url_tp_dashboard }})**, as 'of the total functional LoC attributed to you at the end of `{{ version_final }}`, what percentage was edited by you during the feature freeze?'.
* **The penalty for violating the feature freeze will be case-by-case basis**, but not smaller than `-2`.
* **We will allow 5% a margin-of-error on top of the 10%** -- so, you will not be penalised if you exceed 10% by a tiny bit (i.e., up to 15%).
* **There is no limit on the nature of changes you can do** to functional code, but we **strongly recommend to choose based on,**<br>
  a) the **priority** (i.e., how important the change is), and,<br>
  b) the **risk** (i.e., the risk of the change introducing new bugs).

**Using 'Planned Enhancements' DG section to counter known feature flaws:** Given you are not allowed to update functional code freely in {{ version_final }}, we allow you to optionally add a section named `Appendix: Planned Enhancements` to the end of the DG. More details in the panel below:

{{ embed_topic("tp-deliverables-dg-fragment.md#planned-enhancements-info", "Admin " + icon_embedding + " tP → Deliverables → DG (extract): Planned Enhancements", "3", indent="1") }}

****FAQs on the feature freeze:****

<panel type="seamless" header="**==[Q0]==** **How exactly is the LoC limit calculated**?" minimal>

**A:** The calculation is based on your LoC !!at the end!! of the `{{ version_final }}`, not the current LoC.

Furthermore, it is based on 'in the final code, how many lines are attributed to you (by the code dashboard)'.<br>
<pic src="images/tpCodeDashboardLoc.png" />

Example (note: LoC numbers refer to lines of functional code only): Suppose you currently have `600 LoC` of code under your name. At the end of the `{{ version_final }}` you ended up with,

* `650 LoC` %%(you added some code, and edited some other code)%%:<br>
  → Of that `650 LoC`, you could have added/edited up to `650 * 10% = 65 LoC` during the feature freeze.
* `550 LoC` %%(lower than you started with because you deleted some code)%%:<br>
  → Of that `550 LoC`, you could have added/edited up to `550 * 10% = 55 LoC` during the feature freeze.
* `400 LoC` %%(because you deleted a lot of code)%%:<br>
  → `400 * 10% = 40 LoC` is less than `50 LoC`. You could have added/edited up to `50 Loc` of that `400 LoC`.

So, **deleting lines does not count as a change** (only editing and adding are counted as changes) but deleting lines reduces the number of LoC attributed to you, and hence, reduces the number of lines you can change during the feature freeze.

**Editing the same line multiple times** (in different commits/PRs) still counts as one line.
</panel>

<panel type="seamless" header="**==[Q1]==** How can a student **calculate/track how much code s/he can change**?" minimal>

**A:** Keep in mind that the calculation is based on your LoC at the end of the `{{ version_final }}`, not the current LoC (the current LoC can still provide a rough estimate). You may use the following two code dashboards to find the current functional code LoC attributed to you:

1. [**tP Code Dashboard (Functional Code Only)**]({{ url_tp_dashboard_fc_only }}) -- this is the normal tP code dashboard, but configured to show functional code changes only. From there, you can find how many functional LoC is attributed to you, as per the most recent code dashboard update.<br>
  <pic src="images/tpCodeDashboardLoc.png" />
1. [**tP Code Dashboard (Feature Freeze Period Only)**]({{ url_tp_feature_freeze_dashboard }}) -- this shows changes to functional code during the feature freeze period only. You can use this LoC number against the number you found in (1) above to estimate the percentage of LoC that you touched during the feature freeze period.

The above two dashboard links are also available in the top navigation menu of the course website (see under `Project Links`).

Both code dashboards are currently set to auto-update every three hours.
</panel>

<panel type="seamless" header="**[Q2]** Suppose fixing a bug will violate the feature freeze but not fixing it can incur a penalty during the PE. How do we decide **which option is less costly**?" minimal>

**A:** No single bug can incur a penalty of more than `-2`, which is the minimum penalty for violating the feature freeze.

Product design is hard, and achieving a very good design takes experience, skill, and multiple iterative refinements. Hence, having some bugs at this stage is natural. Accordingly, bugs will not be penalized in the following cases:

* If it is a feature flaw that will be fixed by an item you listed in the _Planned enhancements_ DG section (as mentioned above).
* After the bug is reported during the PE, you successfully argued it as 'not in scope' (i.e., fixing it is of lower priority than the work done already, and hence it is justifiable to be postponed to a future version). Reporters of such bugs will earn partial credit.

In addition, you can mitigate the impact of such bugs and thus lower its severity by tweaking the UG (e.g., explain the feature better, clearly state the limitations and guide users to work around those limitations).
</panel>

<panel type="seamless" header="**[Q3]** Are **minor/cosmetic code refactoring** counted against the feature freeze?" minimal>

**A:** Yes, all changes are counted. If Git sees the line as 'modified', it will be counted as a changed line.
</panel>

<panel type="seamless" header="**[Q4]** Change percentage is counted using **all lines or non-blank lines only**?" minimal>

**A:** For simplicity, we'll be using all lines.
</panel>

<panel type="seamless" header="**[Q5]** Can we **squeeze in more changes into the feature freeze** by 'clever hacks' (e.g., combining multiple lines etc.)?" minimal>

**A:** All cases of changes near to the limit will be examined manually. If we notice any such attempts to 'game the system', they will be penalized accordingly.
</panel>

<panel type="seamless" header="**[Q6]** Can I **borrow the unused 'change quota'** of another member?" minimal>

**A:** No. But there is no restriction against one member helping to fix a feature of another member.

</panel>

<panel type="seamless" header="**[Q7]** Can we **add entirely new features** during the feature freeze?" minimal>

**A:** This is strongly discouraged as it goes against the spirit of the feature freeze. That said, we enforce the feature freeze based only on the _amount_ of code changed, not the _nature_ of the code change.

</panel>

<panel type="seamless" header="**[Q8]** We already merged a PR that violates the feature freeze. Now what?" minimal>

**A:** No penalty if you revert the change for the final submission. You can use [GitHub's _Revert PR_ feature](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/reverting-a-pull-request) for this. Failing that, you'll need to reverse the merge commit of the offending PR manually, or at least do another PR to reverse the effect of the previous feature freeze violation.
</panel>

<panel type="seamless" header="**[Q9]** How to decide between recording a feature flaw as a 'known issue' (in the UG) and a 'planned enhancement' (in the DG)?" minimal>

**A:**

* UG's 'Known Issues' is a way to caution users about limitations of the app. In terms of grading, informing users of an issue can reduce the severity of the issue, but they are not totally immune from being reported/penalized as bugs.<br>
  DG's 'Planned Enhancements' are immune from PE bug reporting. It's mostly for PE purposes (i.e., a course-specific item); not something you see often in real DGs.
* There is no limit to how many known issues you can list in the UG, but listing many will put the product in a negative light.
* You can list the same item in both, in which case the presentation/details of it can vary between the two too (as the two documents are meant for two different audiences).
</panel>

</box>
</div>
<div id="alert-time-sensitive">
<div class="indented">
<box type="important" icon=":fas-hourglass-half:" seamless>

<span class="text-danger">**This task is time-sensitive.**</span> If done later than the [deadline](weeklySchedule.html#:~:text=for%20exact%20dates.-,Deadline%20for%20weekly%20tasks,-The%20soft%20deadline), it will not be counted as 'done' (i.e., no grace period).
</box>
</div>
</div>

<div id="stretched-due-to-holiday">
{% if pe_schedule_stretched %}
<box type="important" seamless>

**This iteration is normally done in {{ "one week" if cs2103 else "two weeks" }}, but is spread over {{ "two" if cs2103 else "three" }} weeks** due to clashes with holidays. So, do the amount of work you would normally do if this was only {{ "one week" if cs2103 else "two weeks" }} long (i.e., no need to do more work because there is an extra week for this iteration).

**The [tP progress dashboard]({{ url_tp_progress_dashboard }}) will stay in Week 11 for an extra week** (i.e., even when we are in Week 12), to reflect that you can use Week 12 to do Week 11 tP tasks %%i.e., pending Week 11 tasks will not turn red until end of week 12%%.
</box>
{% endif %}
</div>

<div id="level-up-coverage">
<box>

**{{ icon_tip }} Ways to level up your tP game:**{.text-success}

* **Consider increasing test coverage** by adding more tests if it is lower than the level you would like it to be. Take note of our expectation on test code (given in the panel below).

{{ embed_topic("tp-expectations.md#testing-expectations", "Admin " + icon_embedding + " tP → Grading → **Expectation on testing**", "3", indent="1") }}

* **After you have sufficient code coverage, fix remaining code quality problems** and bring up the quality to your target level. Note that the quality of the code attributed to you accounts for a significant component of your final score, graded individually (based on the code attributed to you by the [tP code dashboard]({{ url_tp_dashboard }})).{% if cs2103 %}<br>
  ==**This is your last chance to improve code quality**==, given that the amount of code changes you can do during the feature-freeze in {{ version_final }} is very limited.
{% endif %}

{{ embed_topic("tp-grading.md#projectGrading-codeQuality-criteria", "Admin " + icon_embedding + " tP → Grading → **Code Quality Tips**", "3", indent="1") }}
</box>
</div>

{#====================================================================================================================
 # CS2103 Weekly Intros
 #====================================================================================================================#}
{% call show_tp_week_intro("cs2103", 3) %}

**This week, we kick off the tP** with a few light individual and team tasks, described in the sections below.

<box type="info" seamless>

{{ icon_individual }} **indicates an individual task** %%(i.e., each team member has to do the task, graded individually)%%<br>
{{ icon_team }} **indicates a team task** %%(i.e., some or all members may do the work; graded for the whole team)%%.<br>
{{ icon_team_rep }} **indicates one-person-per-team task** %%(i.e., one member can do the task on behalf of the team, although other members are welcome to pitch in)%%.
</box>

<box type="tip" seamless>

**Stronger teams are welcome to stay one week ahead of the tP schedule.** However, do not move ahead more than one week, as doing tP in a short burst will interfere with some of its learning outcomes.
</box>
{% endcall %}
 {#====================================================================================================================#}
{% call show_tp_week_intro("cs2103", 4) %}

**This week, the tP focus is on setting a project direction** i.e., decide on the type of users your product will target, and the value it will provide for those users (what problem does it solve?)<br>
**Weekly project meetings, and keeping notes of project details** is two other things we'll start from this week.
{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2103", 5) %}

++**Connecting the dots so far ...**++{.text-info}

* **We already know that the tP will be done in breadth-first iterative manner**, each iteration delivering a working version that will be evolved further by subsequent iterations. Now is a good time for us to plan those iterations.{ texts="['A.','B.','C.','D.']" t-class="fw-bold text-info" }
* **Intuitively, it feels like we should decide features of the final version first**, and then, work our way backwards to plan intermediate versions.<br>
  **But that approach is not advisable, due to the difficulty of reliably estimating the effort** each feature will need, _especially because you are not experienced in doing similar projects_. So, any such long-range plan is likely to be highly inaccurate anyway.
* **Instead, our approach is  to ==assume the current iteration is the last iteration.==**<br>
  Then, we aim to deliver the best possible product at the current iteration, based on available time.<br>
  We execute the iteration accordingly, and even tweak the plan further along the way, as needed.<br>
  After the iteration is over, we plan the next iteration as if _it's_ the last iteration. But that time, we can factor in the experience from the previous iteration to do a better job of planning.<br>
 **How is that better?**
  * **More practical**: Shorter-term plans have a better chance of being accurate and doable.{{ bullet_tick_green }}
  * **Planning improves over time**: You get multiple 'clean shots' at project planning. Each try can learn from the previous tries. Hence, more learning.
  * **Lower risk**: As each iteration produces a working product, you always have a working product, which practically eliminates the risk failing to deliver a working product by the final deadline.
* **However, it does not mean we simply keep adding features without any plan** and declare whatever we have at the end as the 'final product'. Instead, we should still set targets, and follow a plan that aims to hit those targets.<br>
  Thus, we can adopt the following two **P**lanning **S**trategies:
  <box type="important" id="ps1-and-ps2" seamless>

  * **We should have a clear overall _direction_**.This ensures we always head in the right direction, even if the final product is not defined precisely yet. { icon="" texts="['PS1.', 'PS2.']"  t-class="fw-bold text-danger" }
  * **An iteration should start by defining a precise target for it**, aligned with the project direction. This ensures we always have a concrete target to aim for.
  </box>

  Along PS1, we have already defined (in the previous week) the _target user profile_, and the _problem addressed_.<br>
  Along PS2, we have not done anything yet.

++**What's happening this week:**++{.text-info}

{{ show_tp_iterations_gantt("tpGanttChart-preIterations.png", 800, 52, 62) }}

* The task {{ thumb_small("1") }} (_Brainstorm user stories_) takes one more step in the direction of PS1 above, by **brainstorming all the capabilities the target user might want the final product to provide**.<br>
  Note: We are not aiming for a precise design of the final end product. As per B, we don't need such a precise design this early in the project.
* The task {{ thumb_small("2") }} (_Choose user stories for the MVP version_) takes the first step in the direction of PS2 above, by **narrowing down the user requirements** to a smaller subset that we can deliver in an earlier iteration.

{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2103", 6) %}

++**Connecting the dots so far ...**++{.text-info}

Previously, we mentioned the following two project planning strategies:
<blockquote>

<include src="tp-tasks-fragment.md#ps1-and-ps2" />
</blockquote>

Last week,
* to help with PS1, we collected potential user stories for the final product.
* to help with PS2, we selected a subset of those user stories for an MVP version of the product.


++**What's happening this week:**++{.text-info}

{{ show_tp_iterations_gantt("tpGanttChart-preIterations.png", 800, 77, 80) }}

This week, we focus on two fronts:

* **The first front (which aligns with PS2) moves towards defining a precise target for the first version** (i.e., MVP): task {{ thumb_small("1") }} translates the selected user stories into a _feature list_ and task {{ thumb_small("2") }} expands that feature lists to a more precise _feature specification_.
* **On the other front, we prepare to start coding work**. Tasks {{ thumb_small("3") }} (_Set up the project repo_), and {{ thumb_small("4") }} (_Get familiar with the codebase_) help with that.


++**Things to note:**++{.text-info}

* **tP tasks progress is graded**. Completing individual and team tasks are considered for grading the _project management_ component of your project grade. That said, unless a deliverable is marked 'time-sensitive', there is no penalty for missing a deadline provided you catch up with most of them within a few days after the deadline.{{ bullet_important_red }}

{{ embed_topic("tp-grading.md#project-management-grading", "Admin " + icon_embedding + " tP → **Grading → Project Management**", "3", indent="1") }}

{{ embed_topic("weeklySchedule.md#deadline-definition", "Admin " + icon_embedding + " Weekly schedule → **Deadline for weekly tasks**", "1", indent="1") }}

* **Most aspects of project progress are tracked using automated scripts.** ==Please follow our instructions closely or else the script will not be able to detect your progress==. There will be no partial credit for work that did not follow the instructions precisely, but in most cases you can get the work to be counted simply by rectifying the non-compliance.{{ bullet_important_red }}

{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2103", 7) %}

++**What's happening this week:**++{.text-info}

**This week, we do the first tP iteration: {{ version_practice }}.**

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 5, 22) }}

**Each tP iteration focuses on a specific #g#learning outcome##, a corresponding #g#product goal##, and a #g#strategy##** that we'll use to achieve both. The ones for this tP iteration (i.e., {{ version_practice }}) are given below:

{{ show_tp_goals(version_practice, "v11-goals") }}

<div class="indented-level3">

<include src="tp-timeline.md#lo-above-product" />
</div>

**We consider this iteration a 'practice' iteration**. Reason: As this is the first time your team is working on this codebase, we first focus on learning the workflow that you need to follow as a team. In this practice iteration, we limit ourselves to some document updates only (to minimize the risk of breaking the codebase).

Specifically, we start with a workflow practice session (in task {{ thumb_small("1") }}), and proceed to do some further documentation updates in tasks {{ thumb_small("2") }} and {{ thumb_small("3") }}.

++**Things to note:**++{.text-info}

{{ show_faq("tpIterationDeadline") }}
{{ show_faq("tpMissingIterationDeadlines") }}
{{ show_faq("tpV11Scope") }}

<include src="tp-common-fragments.md#error-commit-message-subject" />
<include src="tp-common-fragments.md#error-pr-from-master" />

<box type="tip" icon=":fab-git-alt:" icon-size="2x" seamless>

++**Start using Git via the CLI**++{.text-success .font-monospace}

If you have been using Sourcetree (or other GUI) for Git before, we strongly recommend that you ==move towards using the CLI to perform Git tasks== in the second half of the semester. Doing so will strengthen your Git knowledge (because CLI takes you closer to what's actually happening, while GUIs might hide such details).<br>
But you can continue to use your favorite Git GUI for a more 'visual' view of your repo, side-by-side with the CLI e.g., from Sourcetree, you can open a gitbash terminal, run the command in that terminal, and see the result in the GUI.
</box>

{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2103", 8) %}

++**What's happening this week:**++{.text-info}

Having practiced the workflow in the previous iteration, **this week's iteration {{ version_first }} adds the first wave of functional code changes.**

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 19, 37) }}
{{ show_tp_goals(version_first, "v12-goals") }}

The _breadth-first iterative_ approach requires each intermediate version to be a full working product. However, to make things a bit easier for you (as you are only getting started with the project), **you need not release any new product version at the end of this iteration.** This means you have the freedom to create PRs for small code changes, without the pressure to implement a feature end-to-end within one PR (or even within this iteration).

++**Things to note:**++{.text-info}

* {{ icon_important_big_red }} **Read <trigger trigger="click" for="modal:appE-reusePolicy">our reuse policy %%(in Admin: Appendix B)%%</trigger>**, in particular, ==how to give credit when you reuse code from the Internet or classmates==:
<modal large header="Admin {{ icon_embedding }} Appendix B: Policies → Policy on Reuse" id="modal:appE-reusePolicy">
<include src="appendixB-policies.md#policy-reuse"/>
</modal>

* **Note the individual and team expectations of the tP**, if you haven't done so already.

{{ embed_topic("tp-expectations.md#functionalityExpectations", "Admin " + icon_embedding + " tP: Functionality Expectations", "3", indent="1") }}
{{ embed_topic("tp-expectations.md#individualExpectations", "Admin " + icon_embedding + " tP: Individual Expectations (and ==guidance on work distribution==)", "3", indent="1") }}
{{ embed_topic("tp-expectations.md#teamExpectations", "Admin " + icon_embedding + " tP: Team Expectations", "3", indent="1") }}
{{ embed_topic("tp-supervision.md#making-project-decisions", "Admin " + icon_embedding + " tP → Supervision (Extract) → **Tutor's role in making project decisions**", "3", indent="1") }}

<include src="tp-common-fragments.md#error-header-comment-phrasing" />


{% endcall %}
{#---------------------------------------------------#}
{% call show_tp_week_outro("cs2103", 8) %}
<box type="info" icon=":bi-emoji-surprise:" icon-size="2x" seamless>

<span class="text-info">**Shocked by iP to tP transition?**</span> Around this time you will realize how the speed you can implement things in the tP is significantly slower compared to the iP. As discouraging as this might feel, there are several ways this can contribute towards the learning outcomes of this course, and it is not expected to affect your tP grade either.

<panel type="seamless" header="More on this ...">

1. **It is important to realize that working in larger codebases is a much slower affair.** The number of lines an engineer can write per day is often limited to a double-digit value, [even going as low as 20](https://medium.com/modern-stack/how-much-computer-code-has-been-written-c8c03100f459#:~:text=As%20we%20can%20see%2C%20a,in%20a%20given%20working%20year.)).
1. **The speed varies from project to project**, and naturally, is slowest at the start when you are very new to the project. Even so if you are new to working with legacy code. On the positive side, the iterative approach we use gives us room to adjust targets based on the actual speed you can deliver in the tP codebase.
1. **The slowness of progress can be partly due to design flaws** of the current codebase (i.e., the design makes code changes harder than necessary). Keep a lookout for such cases, and if you can think of design tweaks that makes the code easier to change, go ahead and try them out. Such work can earn credit too.

Finally, we don't expect each of you to put into the tP more _effort_ than you put into the iP (i.e., as the progress in the tP is expected to be slower, it is not necessarily write as much code or implement as many features as you did in the iP). Keep in mind the tP had been done by thousands of students before, and we are well aware that the amount of new features that you can deliver in the tP is not much. So, the slow progress will not affect your tP grade, as that is already factored into the grading. **What is needed is for you to recalibrate your own tP expectations/plans to match the reality of the tP environment** -- such recalibration is a learning outcome of the course too.
</panel>
</box>

<box type="info" seamless>

**Feel free to improve AB3 in any way you see fit.**{.text-info} While not very 'buggy', AB3 is not 'perfect' either (it is not meant to be a 'model solution'). In particular, ==find and fix any bugs it has==. If you are not sure if something is a bug or an intended behavior, you can post in the forum to check.<br>
While we are on the topic, also note that the architecture of AB3 doesn't suit every kind of application either. As you gain more experience in other application domains, you will learn different types of architectures that you can add to the collection of different architectures that you can consider for future projects. The same goes for the tool chain and the tech stack of AB3. Therefore, **do not try to apply AB3 as a template for _every_ other project you encounter in the future**.
</box>

{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2103", 9) %}

++**What's happening this week:**++{.text-info}

**This week, we deliver the first working version of the product (i.e., the MVP)**, thus finishing what we started in the previous iteration.

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 32, 52) }}
{{ show_tp_goals(version_mvp + " (MVP)", "v13-goals") }}

As per the learning outcome of this iteration (given above), our focus is on !!delivering a product on time!!. So, %%in task {{ thumb_small("1")}}%%, we start by setting up a plan to reach that goal, and then execute on it %%in task {{ thumb_small("2")}}%% , while making course corrections as we go (if needed).

++**Things to note:**++{.text-info}

<box type="info" seamless>

**Iteration vs milestone vs version:**{.text-info}

**An _iteration_ can aim to reach zero or more _milestones_, some of which can be the release of a product _version_**. So, they are three different things.<br>
 For convenience, the tP uses a version number to refer to all three. For example, when we say _iteration `{{ version_mvp }}`_, we mean _the iteration that ends in the milestone `{{ version_mvp }}` (that also happens to deliver the product version `{{ version_mvp }}`)_.
</box>

<box type="info" seamless>

**How to define version numbers?**{.text-info}

While there is no universal set of rules on choosing version numbers for a product, **there is a convention named [SemVer](https://semver.org/) that is well-defined and widely used**. Our tP version numbers (`{{ version_mvp }}`, `{{ version_penultimate }}`, `{{ version_final }}` etc.) do not follow SemVer strictly though.
</box>

This is your first 'proper' iteration that delivers a product. Ensure you ==remember how you are expected to 'manage' an iteration== (graded), given in the panel below:

{{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking", "Admin " + icon_embedding + " Appendix E(extract): **Project schedule tracking**", "1", indent="1") }}

{% endcall %}
{#---------------------------------------------------#}
{% call show_tp_week_outro("cs2103", 9) %}

Phew! Hope your first product release went well, and was on time. If it didn't, not to worry; we have more tries to get it right.

For now, give some thoughts to the following questions (the answer will be needed for an activity in the next iteration):

* Were you able to deliver on time? If not, why?
* How do initial effort estimations compare to actual effort? Took more or less effort than anticipated?

{% endcall %}

{#====================================================================================================================#}
{% call show_tp_week_intro("cs2103", 10) %}

++**What's happening this week:**++{.text-info}

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 48 if pe_schedule_ideal else 45, 67) }}
{{ show_tp_goals(version_alpha, "v14-goals") }}

**In this iteration, we learn from past iterations, and aim to better plan and better deliver another functional increment** that would get you very very close to the final version in terms of raw functionality.<br>
We call this the _alpha version_ because **this version is meant to be good enough for <tooltip content="testing done by internal testers">_alpha testing_</tooltip>** of the product.

First, %%in task {{ thumb_small("1")}}%% we look back at the previous iteration, to see what we can learn from it.<br>
Then, %%in {{ thumb_small("2")}}%% we plan features to be implemented in this version, while aiming to come very close to the final product's feature set.<br>
Finally, %%in {{ thumb_small("3")}}%% we implement those features to deliver the `{{ version_alpha }}`.

++**Things to note:**++{.text-info}

{{ show_faq("tpHowMuchToGetFullMarks") }}

<box type="warning" header="Heads up: this is a BIG week of the tP!" seamless>

Ideally, the tP work should be distributed equally across all tP works. In practice though, this can be uneven based on your other commitments %%e.g., most did less work in week 7-8 due to midterm exams%%.

==If you were to pick one tP week to push the hardest, this week should be it!== That is because in this iteration you need to implement all features that you plan to include in the final version (but they need not be fully polished).
</box>

{% endcall %}
{#---------------------------------------------------#}
{% call show_tp_week_outro("cs2103", 10) %}

**Have any suggestions to improve AB3?**{.text-info}

Now that you have worked with AB3 codebase for a while, if you have any suggestions on how to improve AB3 (for future batches), feel free to post/discuss them in the [forum]({{ url_forum }}).<br>
%%Examples: places where the design/code can be simplified, hard to understand parts of the code, tips you can share with future batches, ...%%

{% endcall %}

{#====================================================================================================================#}
{% call show_tp_week_intro("cs2103", 11) %}

++**What's happening this week:**++{.text-info}

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 65 if pe_schedule_ideal else 80, 80) }}
{{ show_tp_goals(version_penultimate, "v15-goals") }}

**This iteration focuses on applying internal quality control before the product is exposed to outsiders**. %%'Outsiders' here refer to other teams that will be testing your product during the practical exam dry run (PE-D).%%<br>
In {{ thumb_small("1")}}, you will do an alpha testing of your own product, and record bugs, which can then be fixed during {{ thumb_small("2")}}.<br>
Keeping in mind that this is your last chance to do _any_ feature enhancements (due to the _feature freeze_ in iteration {{ version_final }}), in task {{ thumb_small("3")}} you will decide which final touches you would want to implement, and proceed to implement them.<br>
At the same time, the UG and the DG needs to be updated, as given in task {{ thumb_small("4")}}.

++**Things to note:**++{.text-info}

<include src="tp-tasks-fragment.md#stretched-due-to-holiday" />

<box type="info" seamless>

**Remind yourself of the project grading criteria**:

{{ embed_topic("tp-grading.md#main", "Admin " + icon_embedding + " **tP → Grading**", "1") }}
</box>

{% endcall %}

{#====================================================================================================================#}
{% call show_tp_week_intro("cs2103", 12) %}

++**What's happening this week:**++{.text-info}

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 78 if pe_schedule_ideal else 75, 90 if pe_schedule_ideal else 80) }}

{% if pe_schedule_ideal %}
{{ show_tp_goals(version_final, "v16-goals") }}
{% elseif pe_schedule_late %}
We are still in iteration `{{ version_penultimate }}`, due to this iteration being stretched over two weeks.
{% endif %}

++**Things to note:**++{.text-info}

<box type="important" seamless>

**Remind yourself of our policy on reuse** (e.g., ==how to give credit for reused code==):

{{ embed_topic("appendixB-policies.md#policy-reuse", "Admin " + icon_embedding + " Policy on reuse", "1", indent="1") }}
</box>

{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2103", 13) %}

++**What's happening this week:**++{.text-info}

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 90 if pe_schedule_ideal else 86, 85 if pe_schedule_ideal else 92) }}
{{ show_tp_goals(version_final, "v16-goals") if pe_schedule_late else '' }}

{% endcall %}
{#====================================================================================================================
 # CS2113 Weekly Intros
 #====================================================================================================================#}
{% call show_tp_week_intro("cs2113", 3) %}

{{ show_tp_iterations_gantt("tpGanttChart-preIterations.png", "800", 1, 60) }}

{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2113", 4) %}

{{ show_tp_iterations_gantt("tpGanttChart-preIterations.png", "800", 23, 28) }}

++**Things to note:**++{.text-info}

{{ icon_important_big_red }} Timely completion of the weekly tP tasks can improve the _project management_ component of your tP grade.
{{ embed_topic("tp-grading.md#project-management-grading", "Admin " + icon_embedding + " tP → Grading → Project Management", "3", indent="1") }}

{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2113", 5) %}

{{ show_tp_iterations_gantt("tpGanttChart-preIterations.png", "800", 44, 48) }}

{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2113", 6) %}

{{ show_tp_iterations_gantt("tpGanttChart-preIterations.png", "800", 65, 48) }}

{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2113", 7) %}

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 5, 38) }}

**In this week, we get ready to start tP iterations**. We start by planning the first iteration.

{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2113", 8) %}

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 17, 47) }}

++**Things to note:**++{.text-info}

<include src="tp-common-fragments.md#error-commit-message-subject" />
<include src="tp-common-fragments.md#error-header-comment-phrasing" />
<include src="tp-common-fragments.md#error-pr-from-master" />
{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2113", 9) %}

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 30, 50) }}

++**Things to note:**++{.text-info}

<include src="tp-common-fragments.md#error-low-pr-comments" />

{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2113", 10) %}

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 50 if pe_schedule_ideal else 43, 70) }}

++**Things to note:**++{.text-info}

* **Set moderate targets for functionality.** Adding more functionality than needed will not earn you more marks but can expose you to higher risk of bugs.<br>
  **Focus on improving the process and the quality** instead.
* **Move in small steps, and keep the product working at each step.** If it breaks, you will only have to examine the latest change for the cause of the breakage.

<include src="tp-tasks-fragment.md#stretched-due-to-holiday" />
{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2113", 11) %}

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 63 if pe_schedule_ideal else 58, 70) }}

++**Things to note:**++{.text-info}

* **Aim to reach the final version in this iteration itself**: ==After this iteration is over, you get a chance to fix your tP bugs (in the project, as well as documentation) without any penalty.== What's more, others will help you find those bugs (via tutorial activities and the PE Dry Run happening at the end of this iteration).<br>
  To take advantage of the above, try to make your {{ version_penultimate }} (product, DG, and UG) as close to what you intend to submit as your final version (i.e., {{ version_final }}).{% if pe_schedule_late %}
* **You have two weeks to finish tP tasks listed under this week** due to the extra week added on account of holidays.{% endif %}

{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2113", 12) %}

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 78 if pe_schedule_ideal else 73, 80 if pe_schedule_ideal else 70) }}
{% if pe_schedule_late %}
++**Things to note:**++{.text-info}

Use this week extra week to finish up any leftover work from the previous week.
{% endif %}
{% endcall %}
{#====================================================================================================================#}
{% call show_tp_week_intro("cs2113", 13) %}

{{ show_tp_iterations_gantt("tpGanttChart-iterations.png", "", 90 if pe_schedule_ideal else 85, 80 if pe_schedule_ideal else 90) }}

{% endcall %}
{#====================================================================================================================#}
{# Steps
{#====================================================================================================================#}
<span id="heading_get_familiar_with_ab3">{{ icon_individual }} %%Individual Task%%: Explore AB3 features</span>
<div id="desc_get_familiar_with_ab3">

* **Objectives:** (1) To get each of you to think of ways to improve AB3 (2) To detect any Java version compatibility issues between your local set up and the expected Java version.

* **Submission:** via [Canvas survey named `tP: AB3 Initial Experience`]({{ url_canvas_home }}/quizzes) by ==<span class="text-danger">{{ get_date(date_w3_start, 5, time="23:59") }}</span>==

* **Steps:**
    1. Download the latest released version %%(i.e., the jar file)%% of AB3 from [its upstream repo](https://se-edu.github.io/addressbook-level3/UserGuide.html).
    1. Get it running on your computer. Play around with it to familiarize yourself with its current features.
    1. Add yourself to the list of contacts in AB3 (using the `add ...` command).
    1. Take a screenshot of the AB3 Window, while it shows your own contact info you added earlier. Save it as a `.png` file.
    1. Think about how the AB3 user experience can be improved, for example, by tweaking the command format, or the GUI, or the features. Note them down as a list of feature suggestions, as free text (i.e., no specific format).<br>
       Suggested: Try to come up with at least 5 ways to improve AB3, while also trying to go beyond the simple/obvious ones (i.e., this is a chance to be insightful but also creative).<br>
       Also keep the following tP constraints/recommendations in mind when doing this, as improvements that are not aligned with [tP constraints](tp-constraints.html) are unlikely to be useful later.
       {{ embed_topic("tp-constraints.md#Constraint-Typing-Preferred", "Admin " + icon_embedding + " tP Constraints → Constraint-Typing-Preferred", "2", indent="2") }}
       {{ embed_topic("tp-constraints.md#Recommendation-CLI-First", "Admin " + icon_embedding + " tP Constraints → Recommendation-CLI-First", "2", indent="2") }}
       {{ embed_topic("tp-constraints.md#Recommendation-Realistic", "Admin " + icon_embedding + " tP Constraints → Recommendation-Realistic", "2", indent="2") }}

<div class="indented-level1">

6. Use the Canvas survey mentioned above to submit the screenshot and the feature suggestions.<br>
   Note: The feature suggestions you submit will be shared with the team members later, so that your team can use them when designing the tP product later.
</div>

</div>
{#====================================================================================================================#}
<span id="heading_set_up_meeting_time">{{ icon_team }} %%Team Task%%: Set up a project meeting time</span>
<div id="desc_set_up_meeting_time">

* After forming teams, **set up a weekly project meeting time/venue (and communication channels) with your team members**:

{{ embed_topic("tp-teams.md#teamCommunication", "Admin " + icon_embedding + " **Teams → Communication**", "2", indent="1") }}

* #r#**Submission** (one person per team):## via Canvas. Submission will open Friday evening, after team forming is complete for all tutorials. We'll let you know when it is open.<br>
  Details to submit:
  * `Which day of the week, and at what time, your team will hold weekly team meetings?` {texts="['i.', 'ii.', 'iii.', 'iv.', 'v.']"}
  * `What is the mode (online or F2F)?`
  * `If F2F, where will you be meeting? If Online, which software will you be using for the meeting?`
  * `Have all teams explicitly agreed to the above plan? If anyone has not agreed, state who and why (e.g., uncontactable).`


{{ show_faq("tpUncontactableMembers") }}
</div>
{#====================================================================================================================#}
<span id="heading_check_collective_ip_status">{{ icon_team }} %%Team Task%%: Check up on team's collective iP status</span>
<div id="desc_check_collective_ip_status">

* Check with all team members if any of them needs help doing the iP, and source within the team to provide the needed help as much as you can %%e.g., offer to sit with them while they do the iP so that you can try to help when needed.%%<br>


<box type="tip" seamless>Mentorship within the team is highly-encouraged and rewarded. Besides, it is in your interest to help team members level up before the tP coding begins, and also, a good early opportunity to build team spirit.</box>

{% if cs2103 %}
* #r#**Submission** (one person per team):## via Canvas. Submission will open Friday evening, after team forming is complete for all tutorials. We'll let you know when it is open.<br>
  After completing this task (i.e., after asking all team members if they need help for the iP, and coming up with a plan to help those who asked for help), one member should submit a brief summary of the status of this task.<br>
   e.g., `One member is slightly behind and one significantly behind. We plan to have a code-together session on Sunday so that we can help them if they encounter problems.`{% endif %}
</div>
{#====================================================================================================================#}
<span id="heading_start_weekly_meetings">{{ icon_team }} Start weekly project meetings</span>
<div id="desc_start_weekly_meetings">

* We recommend you start weekly project meetings now. You can use the meeting to do tP tasks, but also help each other do iP tasks. On a related note, ==it is also acceptable to discuss weekly Canvas quiz (if any) together with team members as you do the quiz== i.e., discuss and decide the answer collectively, but you should not give away your answers to someone who was not part of that discussion.
</div>
{#====================================================================================================================#}
<span id="heading_decide_project_direction">{{ icon_team }} Decide on an overall project direction %%(user profile, value proposition)%%</span>
<div id="desc_decide_project_direction">

* **Decide the target user profile, and value proposition**, as described in the panels below (tip: you can use your first project meeting for this):

<box type="warning" seamless>

As we are still at the early stages of identifying a problem to solve, do not think of the product (i.e., the _solution_) yet. That is, ==do not discuss the product features, UI, command format, and implementation details, etc.== unless they are pertinent to the user profile or the problem addressed.
</box>

<box type="tip" seamless>

<include src="../book/about/usage.md#tip-about-popup-url" />
</box>

{{ embed_topic(baseUrl+"/admin/tp-overview.md#main", "Admin " + icon_embedding + " **tP: Overview**", "3", indent="2") }}
{{ embed_topic(baseUrl+"/admin/tp-expectations.md#main", "Admin " + icon_embedding + " **tP: Expectations**", "3", indent="2") }}
{{ embed_topic(baseUrl+"/admin/tp-constraints.md#main", "Admin " + icon_embedding + " **tP: Constraints**", "3", indent="2") }}
{{ embed_topic("tp-grading.md#criteria-productDesign", "Admin " + icon_embedding + " **tP: Grading → ==Criteria Used for Grading the Product Design==**", "3", indent="2") }}

<box type="tip" seamless>

**Pick a CLI-friendly product domain**: Given `Recommendation-CLI-First` and `Constraint-Typing-Preferred` mentioned in the panels above, it makes sense to pick a product domain that is more suitable for CLI interactions i.e., a product that deals with easy-to-type textual data, needs a small number of data fields, and each data field is short. %%For example, {% if cs2113 %}a blog editor is an unsuitable product domain because it also deals with non-text data (e.g., images, videos) and some data fields are quite long (i.e., paragraphs of text). Similarly,{% endif %} keeping track of extensive employee records may be an unsuitable domain if there are many data fields per employee.%%
</box>


* <span class="text-danger">**Submission**:</span> Submit via TEAMMATES.
  * Details to submit:
    1. **Product name** (plain text only) %%e.g., ClientContactsPro%%<br>
       {{ icon_important_big_red }} Recommended to use **English characters only**. Using special characters, accented characters (e.g., è) etc. might feel 'cute' now, but you will regret it later when you need to involve the product name in submission file names etc.
    1. **Target user** profile (plain text only) %%e.g., freelance event photographers%%<br>
       This is a general description of the target user, <span class="text-danger">not the 'persona' you defined</span> (the latter serves as a concrete representation of the target user, for your internal use only).
    1. **Value proposition** i.e., what problem does the product solve? (plain text paragraph, <span class="text-danger">no more than 50 words</span>) %%e.g., provide fast access to client contact details, optimized for users who prefer a CLI%%<br>
       This is ==not a list of features== -- you should not think about exact features yet.
    1. **Link to the project notes document**: This should be an online document/page (not a folder) -- e.g., a GoogleDoc (not a Google Drive location) -- that is publicly accessible. If your project notes are in multiple locations/files, this one document should contain the link to the other documents with guidance on which link is for what.
  * You'll receive an email from TEAMMATES with the submission link. ==Only one member needs to submit== on behalf of the team. All members can view/update the submission.{% if cs2103 %}
  * {{ icon_info }} Submission link will be sent to you by {{ date_w4_start | date(format_normal, 3) }} %%(reason: we need a few days to set up the submission system _after_ teams have been finalized)%%.<br>{% endif %}{{ icon_info }} If you can't find the submission link, you can go to [TEAMMATES link recovery page](https://teammatesv4.appspot.com/web/front/help/session-links-recovery) and enter your NUSNET email account `e_______@u.nus.edu` to get TEAMMATES to resend the link.

{{ show_faq("tpChangeDirectionLater") if cs2103 }}


</div>
{#====================================================================================================================#}
<span id="heading_start_project_notes">{{ icon_team }} Start a collaborative doc to take project notes</span>
<div id="desc_start_project_notes">

* Keep project notes in an easy-to-use collaborative doc (Recommended: use a GoogleDoc). This document will be checked by the instructors at various points.<br>
  Remember to choose a tool that ==allow public _view_ access== e.g., GoogleDoc can be shared via a public link so that the document can be viewed by others. You'll be asked to submit this link to us in the next week.<br>
  {{ icon_important_big_red }} Make sure all your current and future project notes (if split into in multiple documents) are reachable via links given in this document and are viewable by the public.

</div>
{#====================================================================================================================#}
<span id="heading_brainstorm_user_stories">{{ icon_team }} Brainstorm user stories</span>
<div id="desc_brainstorm_user_stories">

<box type="info" tags="m--cs2103" seamless>

**You can do this step as if the tP is a greenfield project** (i.e., as if there is no AB3), to get the full experience of this activity. Some of the user stories you come up with may already be implemented in AB3, but that can be sorted out later.
</box>

<pic eager class="indented-level2" src="{{baseUrl}}/admin/images/v00.png" width="250px"></pic>

<div class="indented-level1">


* **Learn** [**the _recipe for brainstorming user stories_** in the textbook → Specifying Requirements → User Stories →  Usage]({{ baseUrl }}/se-book-adapted/chapters/specifyingRequirements.html#a-recipe-for-brainstorming-user-stories).<br>
  Also learn about <trigger trigger="click" for="modal:v10-brainstorming">brainstorming</trigger> and <trigger trigger="click" for="modal:v10-userstories">user stories</trigger>.{% if cs2103 %}<br>
  We recommend you view the following video, as it has some additional commentary on the recipe to be used:

{{ panopto("c0612db9-3cf1-4bab-a066-b07501387c0f", desc="Additional commentary on the recipe to be used") }}{% endif %}

* **==Follow the steps in the recipe mentioned above to arrive at user stories== for the product**, with your team members.  <span tags="m--cs2103"><span class="text-danger">If you don't follow the recipe mentioned above</span>, you could end up with a different set of user stories than otherwise.
  </span><br>
  **Keep records of all intermediate steps e.g., the persona, scope, narrative.**

* **User stories for what version?** At this stage, collect user stories to cover at least the final version you hope to deliver at the end of the semester. It is OK to go even beyond that %%(reason: we are simulating a project that will continue even after the semester is over)%%.{% if cs2103 %}<br>
  Do not omit user stories already covered by the features in AB3 %%i.e., the user story should be recorded even if AB3 already caters for it.%%{% endif %}

* **How many user stories?** Aim to collect more user stories than you can deliver in the project. %%Aim to create at least 30 user stories. Include all 'obvious' ones you can think of but also look for 'non-obvious' ones that you think are likely to be missed by other competing products.%%

* **User stories of what size?** Normally, it is fine to use _epic_-level user stories in the early stages of a project but given this is a small project, you may want to eventually break them down to smaller user stories (i.e., small enough for one person to implement in 1-2 days). Some examples (from the iP product domain):
  * {{ bad }} As a user, I can track my schedule, so that I can know when to do things.<br>
    %%Reason: too big, as _track_ can involve a lot of things.%%
  * {{ good }} As a user, I can add a time to a task, so that I can record when a task need to be done.
  * {{ good }} As a user, I can see the pending task that has the next earliest deadline, so that I can know what I need to do next.<br><br>

* **What format?**: You may use a sentence format or a table format but do maintain the prescribed three-part structure of a user story. In particular, ==try to include the _benefit_ part in most user stories== as that will come in handy when prioritizing user stories later.<br>
  {{ icon_tip }} **Use an online spreadsheet for recording user stories** (e.g., Google Sheets), if you are not sure which tool to use. -- they are easy to edit, share, color, and more importantly, sort/filter.

* **Submission** (to be checked by the tutor later):<br>
  * **Intermediate steps** (e.g., persona, narrative): These should be in your collaborative project document started in the previous week. Mark them clearly so that the tutor can detect them easily.
  * **Brainstormed user stories**:  Record them using an <!--~~write each user story in a piece of paper (e.g., yellow sticky note, index card, or just pieces of paper about the size of a playing card). Alternatively you can~~--> online tool (some examples given in <trigger trigger="click" for="modal:v10-onlinetools">[Textbook {{ icon_embedding }} Specifying Requirements → UserStories → Usage → (panel) Tool Examples ]</trigger>).<br>
  {{ icon_info }} If you put the user stories in a page/file other than your main collaborative project notes document (i.e., the one given [here]({{ baseUrl }}/admin/teamList.html)), ensure that page/file is viewable by the public, and the main document has a link to that page/file. Otherwise, the tutor will not be able to see your list of user stories.

<modal large header="Textbook {{ icon_embedding }}" id="modal:v10-brainstorming">
<include src="../book/gatheringRequirements/brainstorming/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>

<modal large header="Textbook {{ icon_embedding }}" id="modal:v10-userstories">
<include src="../book/specifyingRequirements/userStories/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>

<modal large header="Textbook {{ icon_embedding }} Specifying Requirements → UserStories → Usage → (panel)Tool Examples" id="modal:v10-onlinetools">
<include src="../book/specifyingRequirements/userStories/usage/tools.md"/>
</modal>


<div tags="m--cs2103" class="indented-level2">

{{ icon_tip }} **If you choose to use the GitHub issue tracker to manage user stories**, you need to set up your team's GitHub organization, team repo, and its issue tracker first. Instructions for doing those steps are in the panel below.

<panel header="%%Admin {{ icon_embedding }} Appendix E: GitHub (extract)%%" minimized>
  <include src="appendixE-gitHub.md#organization-setup"/>
  <include src="appendixE-gitHub.md#tp-team-repo-setup"/>
  <include src="appendixE-gitHub.md#issue-tracker-setup"/>
</panel>

</div>

</div>
</div>
{#====================================================================================================================#}
<span id="heading_prioritize_user_stories">{{ icon_team }} Choose user stories for the MVP version</span>
<div id="desc_prioritize_user_stories">
<div class="indented">

**Task: Of the user stories you have collected, select the ones you would put in an <popover content="**Minimum Viable Product**: a version with just enough features to effectively deploy the product, and no more">MVP</popover> version** of the product. The goal here is to come up with the _smallest possible product that is still usable_ so that it can be implemented quickly, and delivered at the end of an earlier iteration.
</div>

* **Try to limit the MVP to strictly must-have user stories only** i.e., <span class="text-danger">it's NOT what you _can_ or _want to_ put in the MVP, but what you _must_ have in the MVP</span>. If the product _can_ be of some use without a given user story, that user story should be left out of the MVP version, even if the omission makes the product hard to use, as long as the product is not _impossible_ to use %%e.g., in most cases a product can be used without an 'edit item' feature because the user can always delete an item and add a new item instead of editing an existing an item%%.
* {{ icon_important_big_red }} **Do not discuss features, UI, command format, or implementation details** yet. That would be like _putting the cart before the horse_. At this stage we are simply trying to choose which _user needs_ to fulfill first.
* **Don't worry about subsequent versions or the final version.** You can design them at a later time.
* **Don't worry about MVP being 'too small'.** You can always add more features to the MVP version if you finish it ahead of schedule.<br>
  {{ icon_tip }} You can also select an additional set of user stories that are _nice-to-have_ for the MVP, to be done but only if there's time left.
* **In the interest of keeping the MVP small, you can narrow the scope of MVP further** e.g., narrower target user, a smaller value proposition.

* **Suggested workflow:**
  1. **First stage**:
     * Divide the user stories among team members.
     * Each member will go through their user stories to discard (e.g., cross out, or move to a different location, but not delete) which are _definitely not needed_ for MVP.
  1. **Second stage**:
     * All members discuss the remaining user stories (i.e., the ones not discarded in the first stage), and try to trim the list further.

{{ show_faq("tpNotEnoughWorkToDivide") }}
{{ show_faq("tpShouldWeStartCoding") }}
{{ show_faq("tpOmitStoriesInAb3") if cs2103 }}
{{ show_faq("tpAllStoriesInAb3") if cs2103 }}
</div>
{#====================================================================================================================#}
<span id="heading_set_up_project_repo">{{ icon_team }} Set up the project repo</span>
<div id="desc_set_up_project_repo">

1. [{{ icon_team_rep }} one member] Set up the team org:<br>
   {{ icon_tip }} While only one member needs to do this, it may be useful to do this as a team while that member is screensharing, so that others get to see how it is done too.
   {{ embed_topic("appendixE-gitHub.md#organization-setup", "Admin " + icon_embedding + " Appendix E (extract): **tP Organization Setup**", "1", indent="1") }}

2. [{{ icon_team_rep }} one member] Set up the team repo (including the issue tracker):
   {{ embed_topic("appendixE-gitHub.md#tp-team-repo-setup", "Admin " + icon_embedding + " Appendix E (extract): **tP Team Repo Setup**", "1", indent="1") }}
   {{ embed_topic("appendixE-gitHub.md#issue-tracker-setup", "Admin " + icon_embedding + " Appendix E (extract): **Setting up the issue tracker**", "1", indent="1") }}

3. [{{ icon_individual }} each member] Set up individual forks:
   {{ embed_topic("appendixE-gitHub.md#tp-individual-fork-setup", "Admin " + icon_embedding + " Appendix E (extract): **tP Individual Fork Setup**", "1", indent="1") }}
</div>
{#====================================================================================================================#}
<span id="heading_get_familiar_with_the_code_base">{{ icon_individual }} Get familiar with the codebase</span>
<div id="desc_get_familiar_with_the_code_base">

{{ show_faq("tpIndividualOrTeam") }}

<box type="info" icon=":fas-clock:" seamless>

==Ideally, you should do this task in this week==, but you may take an extra week (i.e., by week 7) to finish.
</box>

* Do the following tutorials to get familiar with the codebase
<div class="indented-level2">

<panel type="info" header="Tutorial 1 - Tracing a Command Execution Path" expanded>

See [here](https://se-education.org/guides/tutorials/ab3TracingCode.html) for details.

We recommend that you put in a sincere effort into this tutorial because tracing through the code of an unfamiliar codebase is an important skill that you can learn by doing so; you will not be able to learn/practice later in the project as the code will no longer be 'unfamiliar' to you later.

**Submission** [optional]: Post an issue in your team's repo with the title `Tutorial: tracing code`. In the description, add a 2-3 screenshots you took while at various points of the tutorial. You may close the issue soon after.
</panel>
<panel type="info" header="Tutorial 2 - Adding a new Command" expanded>

See [here](https://se-education.org/guides/tutorials/ab3AddRemark.html) for details.

If you are an experienced programmer, you can add a different command than the one given in the tutorial.

**Submission:** Do your changes in a branch named `tutorial-adding-command`, push to your fork, and create a PR from your fork's `tutorial-adding-command` branch to your team repo's `master` branch. You may close the PR soon after (i.e., no need to merge the PR).

{{ show_faq("tpTestsForTutorial") }}
</panel>
<panel type="info" header="Tutorial 3 - Removing a field from an entity" expanded>

See [here](https://se-education.org/guides/tutorials/ab3RemovingFields.html) for details.

This tutorial is optional to do, but **at least give it a quick read**.

Submission: not required.
</panel>
</div>
</div>
{#====================================================================================================================#}
<span id="heading_conceptualize_first_version">{{ icon_team }} Conceptualize the MVP version</span>
<div id="desc_conceptualize_first_version">

* ****Task:**** Based on your user stories selected previously, conceptualize the MVP ==in the form of a <trigger trigger="click" for="modal:v10-featureLists">feature list</trigger>==.<br>

<modal large header="Textbook {{ icon_embedding }}" id="modal:v10-featureLists">
<include src="../book/specifyingRequirements/featureList/what/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>

* **Why?**: So far, we have user stories we want to include in the MVP version. But user stories simply tell us _user needs_. To move towards a product design, we need to design _features_ of the product that can fulfill those user needs.

* **Submission:** Note down the feature list in your online project notes document.

{{ show_faq("tpHowManyFeaturesInMvp") }}
</div>
{#====================================================================================================================#}
<span id="heading_draft_the_ug">{{ icon_team }} {% if cs2103 %}Draft the feature specification{% else %}Draft the UG{% endif %}</span>
<div id="desc_draft_the_ug">
<include src="tp-tasks-fragment.md#alert-time-sensitive" />
<div tags="m--cs2113">

* Draft a user guide in a convenient medium (e.g., a GoogleDoc) to describe what the product would be like when it is at {{ version_mvp }}.
  * We recommend that you follow the [AB3 User Guide]({{ url_ab3_upstream_website }}/UserGuide.html) in terms of structure and format.
  * As this is a draft only and the final version will be in a different format altogether %%(i.e., in Markdown format)%%, don't waste time in formatting, copy editing etc. You can also limit this to just the 'Features' section only and omit the other sections.<br>
  While the UG draft need not be 'polished', it should be detailed enough to tell the user how to use the product features in concern.
  * IMPORTANT:
    * Specify the precise/full command syntax for the CLI commands that you will deliver at {{ version_mvp }}.
      i.e., we want you to know exactly what you plan to deliver at {{ version_mvp }} -- while it is fine to change this plan later, it is still important to have a plan first.
    * Include all features that will be available in {{ version_mvp }}. There is no need to include features that will be delivered beyond {{ version_mvp }}.
  * Consider including examples of expected outputs too.
  * {{ icon_important_big_red }} **Submission** [one person per team]: Save the draft UG as a PDF file, name it `{team-id}.pdf` e.g., `{{ example_team_id }}.pdf`, and upload to Canvas.

</div>
<div tags="m--cs2103">

* **Deadline:** Recommended to finish by the regular weekly project deadline (i.e., before the next {{ lecture_name }}), but given the iP final submission is due this week, you may take until Sunday ({{ get_date(date_w6_start, 6) }}) to submit this.

* **Why?** In addition to helping towards PS2, this deliverable forces you to make some fine-grained product design decisions early, thus giving you a better idea about the complexities that lie ahead, and hence, a better sense of the effort that will be required.

* ****Task:**** **Collate into a document the _complete_ detailed description of the intended behavior of the MVP version of the product.**
  * The intended audience for this document is team members, not users (i.e., this is not a user guide).
  * Use a medium that is convenient for collaboration (e.g., a GoogleDoc).
  * The content need not be polished. Don't waste time in formatting, copy editing etc.
  * **For each feature, specify #r#all## of the following:**

<div class="indented-level2">
<box>

* **Feature**: Name of the feature %%e.g., Add contact%% {{ bullet_checkbox_selected_green }}
* **Purpose**: What it does<br><br>
* **Command format**: The precise command format of the command.
* **Example commands**: %%(to show how the command is used)%%<br><br>
* **For each parameter**, specify the following.<br>
  Yes, making these decisions is not easy -- and that's why we want you to think about them now rather than later. Feel free to discuss these validation rules in the forum.<br>
  * Acceptable values %%e.g., If a command takes a person name as a parameter, what inputs are accepted as valid person names?%% Some example aspect to consider:
    * Which formats are allowed for dates, times, telephone numbers, etc.?
    * How does extra/leading/trailing spaces affect the value -- for instance is 'John Doe' same as 'John&nbsp;&nbsp;&nbsp;Doe' (note the multiple spaces in the middle of the name)?
    * How does UPPER/lower case affects values -- is `John Doe` same as `john doe`?
    * It's not enough to state 'valid name'; you need to specify what rules will be used to determine if the input is a valid name.
  * Error message if the value is not acceptable
  * Rationale for the validity rule %%e.g., why only certain characters are allowed for person names?%%<br><br>
* **Outputs**: Precise expected outputs when the command,
  * succeeds %%e.g., changes in the GUI, messages shown to the user%%
  * fails %%e.g., what are the error messages shown when a specific parameter is invalid, missing, specified multiple times, etc.%%
* **Duplicate handling:** What rules are used to determine if two contacts are duplicates? %%e.g., is having the same name enough for two contacts to be considered duplicates, or all details need to be the same?%%<br>
How does the application react to such duplicate entries? Reject or accept? Why?
* **Possible errors:** A list of potential errors related to the feature (excluding the ones mentioned above already) %%e.g., editing a contact in a way that it becomes inconsistent with the rest of the data%%, and how the app responds to each error %%e.g., the error message%%.
* **Relevant UI mock-ups** (unless the UI will be exactly the same as AB3, in which case you should use AB3 screenshots in place of UI mock-ups): %%they can be hand-drawn or created using a tool such as PowerPoint, PlantUML, Figma, etc. -- they can be very low-fidelity mock-ups, as they are meant to be temporary%%

---

{{ icon_tip }} **Recommended: Decide priorities of finer aspects of features**, for example, as must-have (to implement in the MVP) and nice-to-have (i.e., to implement in the MVP only if there is time)<br>
   %%e.g., you can decide one date format that is to be supported in user commands as must-have and two other formats as nice-to-have.%%
</box>
</div>

* **What features should be in the MVP?** In our context, the MVP is considered as the must-have features of your product, for the intended target audience. That is, the product is _impossible_ (not merely inconvenient) to use without those features. %%For example, a product is impossible to use without an 'add' feature but can be used without a 'edit' feature (because deleting and re-adding can be used in place of editing).%%

* **It is OK to make compromises** when making product decisions -- every design option has costs and benefits, and sometimes, costs outweigh the benefits.<br>
For example, it is fine to restrict the person name to a certain length and a character set even if it is theoretically possible for those restrictions to conflict with some rare real-world person names. But you need to be aware of such conflicts, justify the restriction (e.g., ease of implementation/display), and know how users can work around such a conflict should they encounter it %%(e.g., if you app doesn't allow two contacts to have the same name but the user need to store two contacts which are different people with the same name, what should the user do?)%%.

* **You are welcome to (but not required to) follow AB3** when defining the behavior of the new features %%e.g., use similar command formats, input validation rules, error message formats%%.<br>

{{ show_faq("tpAb3FeatureInMvpSpec", is_compact=1) if cs2103 }}
{{ show_faq("tpNeedForNewFeatureInMvp") if cs2103 }}

* **Ensure feature-fit**: While doing this, ensure the features written by each member fit together to form a cohesive product, and meet other grading criteria of the _product design_ aspect. This might require several rounds of refinement. You are encouraged to peer-review feature details written by other team members and refine the overall product design together.

{{ embed_topic("tp-grading.md#criteria-productDesign", "Admin " + icon_embedding + " **tP: Grading → Product Design**", "3", indent="1") }}

* {{ icon_important_big_red }} **Submission** [one person per team]: Save the file as a PDF file, name it `{team-id}.pdf` e.g., `{{ example_team_id }}.pdf`, and upload to Canvas.
* **Grading criteria**: to be considered 'done', the feature spec. should meet all the following criteria:
  * Covers all features in the smallest set of features the product cannot do without.
  * Contains all details mentioned above for each of those features
  * Details seem well-thought-out (i.e., not a half-hearted attempt to satisfy the expected level of details)
</div>
<br>
<div id="divideDocs" class="indented">
  <box>

  {{ icon_tip }} Recommended: **Divide <tooltip content="i.e., work related to the User Guide and the Developer Guide">documentation work</tooltip> among team members so that each person does a non-trivial amount of documentation; preferably based on enhancements/features each person would be adding** %%e.g., If you are the person planing to add a feature X, you should be the person to describe the feature X in the User Guide and in the Developer Guide%%.

  %%Reason: In the final project evaluation your documentation skills will be graded based on sections of the User/Developer Guide you wrote.%%

  {{ embed_topic("tp-grading.md#criteria-documentation", "Admin " + icon_embedding + " **tP: Grading → Documentation**", "3") }}
  <p/>

  If you are not sure what we mean by 'enhancements/features each person would be adding' mentioned above, see the panel below for our recommendation on how to divide the tP work:
  {{ embed_topic("tp-expectations.md#individualExpectations", "Admin " + icon_embedding + " tP:  Individual Expectations on Implementation", "2") }}

  </box>
</div>
</div>
{#====================================================================================================================#}
<span id="heading_refine_product_design">{{ icon_team }} Refine the product design</span>
<div id="desc_refine_product_design">

* Review the UG draft to ensure the features written by each member fit together to form a cohesive product. Note that cohesiveness of the product can affect the grading of the _product design_ aspect.

{{ embed_topic("tp-grading.md#criteria-productDesign", "Admin " + icon_embedding + " **tP: Grading → ==Product Design==**", "3", indent="2") }}

</div>
{#====================================================================================================================#}
<span id="heading_update_website_aboutus_readme">{{ icon_team }} Update the project website</span>
<div id="desc_update_website_aboutus_readme">

<div class="indented-level1">

Now that you have learned the tP workflow, you can proceed to updating a few more tP documents, as per tasks ****A**** and ****B**** below, following the same workflow (optional to do parallel PRs though).

<box type="info" light>

**Recommended procedure for updating docs**:{.text-info}

1. Decide among yourselves who will update which parts of the document(s).<br>
   All team members are expected to contribute to all aspects of documentation %%(e.g., user docs, developer docs, diagrams)%%
1. Update the team repo by following the prescribed workflow:

{{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking", "Admin " + icon_embedding + " Appendix E(extract): **tP project schedule tracking**", "3") }}
<p/>

**Guidance on using documentation tools** (e.g., How to preview changes locally before committing/pushing) can be found in the relevant section of the Developer Guide of your team project website that you set up earlier. Given below is a shortcut, for your convenience:

* If your project is using **Jekyll** for documentation, refer [this Jekyll Guide @SE-EDU/guides](https://se-education.org/guides/tutorials/jekyll.html#:~:text=github.io/myrepo-,Updating%20documents,-Jekyll%20uses%20kramdown).
* If your project is using **Markbind** for documentation, refer [this MarkBind Guide @SE-EDU/guides](https://se-education.org/guides/tutorials/markbind-forked-sites.html#:~:text=latest%20%2D%2Dsave%2Ddev-,Updating%20documents,-MarkBind%20is%20a).

{{ icon_important_big_red }} **Each member must PR their part of the documentation work.** Reasons:

<div class="indented-level1">

1. We use Git data to detect contributions to documentation. If one person committed all documents on behalf of the entire team, our grading scripts will identify that person as the sole contributor to documentation.
1. Git authorship data will help you identify the person responsible for specific bugs in documentation %%-- in the final submission, only the person(s) responsible for each bug is penalised for that bug.%%
1. The project is intended as an exercise for you to practice using Git to manage changes to the same code in parallel.
</div>

{{ show_faq("githubIssuesMultipleDocAuthors") }}
</box>

</div>


****A: Update README page to match your project:****

* Add a UI mockup of your intended final product.
    Note that the ==image of the UI should be `docs/images/Ui.png`== so that it can be downloaded by our scripts. Limit the file to contain one screenshot/mockup only and ensure the new image is roughly the same `height x width` proportions as the original one. %%Reason: when we compile these images from all teams into one page ([example]({{ url_team_list }})), yours should not look out of place.%%<br>
    {{ info }} The UI mock up can be a hand-drawn sketch or created using a tool such as PowerPoint, PlantUML, Figma, etc. Don't spend a lot of time on this, as this will eventually be replaced by a screenshot of the actual product.<br>
    {{ icon_Q }} Can we use an AB3 screenshot for this? Only in the unlikely case that your final product UI is expected to look exactly the same as AB3.{ texts="['A1.', 'A2.', 'A3.', 'A4.']" }
* Update the link of the GitHub Actions _build status badge_ (<img src="https://github.com/se-edu/addressbook-level3/workflows/Java%20CI/badge.svg" alt="Build Status">) so that it reflects the build status of your team repo.
* Acknowledge the original source of the code e.g.,<br>
    `This project is based on the AddressBook-Level3 project created by the [SE-EDU initiative](https://se-education.org).`
* Update all remaining contents of the page to match your own project.

<box type="tip" seamless>

If you did the above updates correctly, your UI mock up and profile photos should appear in your project website and this [**Project List Page**]({{ url_team_list }}).
</box>

****B: Also update site-wide settings****, as necessary:

* You need to update the `AB-3` in the top navigation bar of your project website (it's in `docs/_config.yml` and `docs/_sass/minima/_base.scss` if using Jekyll; in `docs/_markbind/layouts/default.md` if using MarkBind).<br>

* More info on updating site-wide settings such as the above:
  * If using Jekyll: follow [the Jekyll Guide @SE-EDU/guides](https://se-education.org/guides/tutorials/jekyll.html#:~:text=the%20final%20outcome.-,Site%2Dwide%20settings,-Typically%2C%20the%20_config).<br>
  * If using MarkBind: follow [the MarkBind Guide @SE-EDU/guides](https://se-education.org/guides/tutorials/markbind-forked-sites.html#:~:text=edit%20source%20files.-,Site%2Dwide%20settings,-The%20markbind/tweaking).<br>

</div>
{#====================================================================================================================#}
<span id="heading_update_the_ug">{{ icon_individual }} %%[Optional] Update the UG%%</span>
<div id="desc_update_the_ug">

<box type="info" seamless>

Doing this task now means you'll have less to do later, but it is OK if you want to delay this until you have implemented the features.
</box>

* {% if cs2103 %}**Update the UG** in your tP repo. While you can reuse some content from the _feature specification_ that you did earlier, note that UG is intended for end users, and hence the format, level of details, pitching etc. need to match that audience. For example, the UG should not contain all the nitty-gritty details that is in the feature spec.
* **You can use the current AB3 UG for guidance** on the format/flow/tone/level-of-details etc.
  {% else %}**Move the draft UG content into the User Guide page** in your repository. Update the content/structure/formatting as necessary, to match the final form of the UG. If a feature is not implemented in the current version, you can either omit it from the UG or mark it as 'Coming soon' (e.g., `## Archiving contacts [coming soon]`).{% endif %}
* As <trigger trigger="click" for="modal:v11-divideDocs">mentioned before</trigger>, while it is more convenient for one person to update the entire UG, we strongly recommend that **each person updates their own part of the docs** so that we can easily track the contribution of each member using [RepoSense]({{ url_tp_dashboard }}).
* **The scope of this update can be `{{ version_mvp }}`** i.e., only update features that you plan to have in that version.<br>
  Furthermore, as you haven't implemented `{{ version_mvp }}` yet, this update will be somewhat speculative. The content may need to be tweaked later if the actual implementation of the feature deviated from the current plan.

<modal large header="About Dividing Documentation Work" id="modal:v11-divideDocs">
  <include src="tp-tasks-fragment.md#divideDocs"/>
</modal>
</div>
{#====================================================================================================================#}
<span id="heading_add_skeletal_ppp">{{ icon_individual }} Add a skeletal PPP</span>
<div id="desc_add_skeletal_ppp">

<box type="info" seamless>

At the end of the project, each member needs to create a Project Portfolio Page (PPP) to describe your contribution to the project. Let's create a skeletal version of the PPP now itself so that everyone becomes aware how detailed you need to be about your individual contributions at the end of the project.
</box>

* **Create a skeletal version of your _Project Portfolio Page (PPP)_**.
  * Just the headings are enough. You can write `to be added soon` as placeholders for content.
  * PDF conversion not required.
  * Follow the details in the panel below.

{{ embed_topic("tp-deliverables.md#tp-deliverables-ppp", "Admin " + icon_embedding + " tP → Deliverables → Project Portfolio Page", "2", indent="2") }}

</div>
{#====================================================================================================================#}
<span id="heading_update_dg_user_stories_etc">{{ icon_team }} Update the DG: user stories, glossary, NFRs, use cases</span>
<div id="desc_update_dg_user_stories_etc">

* **Add the following to the DG**, based on your project notes from the previous weeks. No need to update other sections, for now.<br>
  {{ icon_tip }} Some examples of these can be found in the [AB3 Developer Guide](https://se-education.org/addressbook-level3/DeveloperGuide.html#product-scope).

  * **Target user profile**, **value proposition**, and <trigger trigger="click" for="modal:v10-userstories">**user stories**</trigger>: Update the target user profile and value proposition to match the project direction you have selected. Give a list of the user stories (and update/delete existing ones, if applicable), including priorities. This can include user stories considered but will not be included in the final product.
  * <trigger trigger="click" for="modal:v10-usecases">**Use cases**</trigger>: Give <tooltip content="suggested: each member adds at least one use case">a few</tooltip> representative use cases (textual form) that need multiple steps to complete. %%e.g. Adding a tag to a person (assume the user needs to find the person first)%%
  * <trigger trigger="click" for="modal:v10-nfr">**Non-functional requirements**</trigger>: List whichever NFRs you think are reasonable for your product %%e.g. performance requirements, usability requirements, scalability requirements, etc.%%<br>
    {{ icon_tip }} Some of the given [project constraints](tp-constraints.md) can be framed as NFRs (e.g. `Constraint-Portable`) while others are purely for pedagogical/course-admin purposes (e.g., `Constraint-Incremental`).
  * <trigger trigger="click" for="modal:v10-glossary">**Glossary**</trigger>: Define terms that are worth recording.

<box type="info" seamless>

**The above DG sections should cover the _full requirements_ of the product**, some of which might not even get implemented by the end of this semester i.e., do not limit to just the requirements you intend to implement in the next iteration. Reason: All identified requirements need to be documented for future reference.

Furthermore, these sections will be graded at the final project evaluation, and any bugs in the content can cost you marks at that point. The panel below gives some relevant DG bug examples you can look out for:

<panel header="Admin {{ icon_embedding }} Tp Grading → Examples of DG Bugs (extract)" minimized>

<include src="tp-grading-bugs-fragment.md#userStoryBugs" />
<include src="tp-grading-bugs-fragment.md#useCaseBugs" />
<include src="tp-grading-bugs-fragment.md#nfrBugs" />
<include src="tp-grading-bugs-fragment.md#glossaryBugs" />
</panel>
</box>

<modal large header="Textbook {{ icon_embedding }} Specifying Requirements → Use Cases" id="modal:v10-usecases">
<include src="../book/specifyingRequirements/useCases/introduction/unit-inElsewhere-asFlat.md" boilerplate />
</modal>

<modal large header="Textbook {{ icon_embedding }}" id="modal:v10-nfr">
<include src="../book/requirements/nonFunctionalRequirements/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>

<modal large header="Textbook {{ icon_embedding }}" id="modal:v10-glossary">
<include src="../book/specifyingRequirements/glossary/what/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>

<modal large header="Textbook {{ icon_embedding }}" id="modal:v10-userstories">
<include src="../book/specifyingRequirements/userStories/introduction/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>

</div>
{#====================================================================================================================#}
<span id="heading_practice_workflow_with_sample_repo">{{ icon_team }} Practice the workflow with a sample repo</span>
<div id="desc_practice_workflow_with_sample_repo">

* We recommend that you practice the workflow we have prescribed for the tP (given in {{ show_gm_lesson_link("forkingWorkflow", "T10L2. Forking Workflow (with Branching)") }}) with your team members as described in the textbook section given in the panel below.<br>
  {{ icon_tip }} You can use your tP GitHub org for this exercise too.

</div>
{#====================================================================================================================#}
<span id="heading_do_a_practice_iteration">{{ icon_team }} Do a 'workflow practice' session</span>
<div id="desc_do_a_practice_iteration">

****Task:**** Do a workflow 'practice' session, to get all team members familiarized with the workflow you need to follow in the tP.

****Why?:****  **_The ability to modify a team-owned codebase in parallel_ is an important learning outcome of this course.** Following a suitable workflow is critical for achieving that. This practice iteration is for you to get used to the workflow that you need to follow in the tP.

<box type="tip" seamless>

**Strongly recommended to do this as a team activity** (preferably F2F, or else connected via Zoom/MSTeams). That will help you proceed faster (e.g., a PR can be merged soon after it has been created) and will also make it easy for you to help each other w.r.t. to the workflow matters.
</box>

****Steps:****

1. [one member] **Set up the issue tracker of your team repo**, if you haven't done so already.<br>
   In addition, **create a milestone named `{{ version_practice }}` and set an appropriate deadline** (i.e., same as, or earlier than, the iteration deadline)

   {{ embed_topic("appendixE-gitHub.md#issue-tracker-setup", "Admin " + icon_embedding + " Appendix E(extract): **tP Issue Tracker Setup**", "1", indent="1") }}

2. [each member] **Fork and clone the team repo**, if you haven't done so already.

   {{ embed_topic("appendixE-gitHub.md#tp-individual-fork-setup", "Admin " + icon_embedding + " Appendix E (extract): **tP Individual Fork Setup**", "1", indent="1") }}

3. [each member] **Add your photo to repo while ==following the prescribed tP workflow==**. Here are the steps %%(yes it is a lot of steps for such a small update, but the purpose is to learn the workflow)%%:

<div class="indented-level1">

* Read the 'tP Scheduling and Tracking' overview given below. {text="3.1"}
  {{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking-overview", "Admin " + icon_embedding + " Appendix E(extract): **tP Project Schedule Tracking (Overview)**", "1", indent="1") }}
* Create an issue to represent the task at hand e.g., `Add Jake's photo`. {text="3.2"}
  {{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking-issues", "Admin " + icon_embedding + " Appendix E(extract): **Using issues to track project tasks**", "1", indent="1") }}
* Assign the issue to yourself, to indicate you are taking responsibility for it. {text="3.3"}
  {{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking-assignees", "Admin " + icon_embedding + " Appendix E(extract): **Using issue assignees to track task allocation**", "1", indent="1") }}
* Assign the issue to the milestone `{{ version_practice }}` to indicate this task is due in `{{ version_practice }}`, as given in the panel below. {text="3.4"}
  {{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking-milestones-when", "Admin " + icon_embedding + " Appendix E(extract): **Using milestones to track task scheduling**", "1", indent="1") }}
* Create a pull request for it, while taking care to ==follow the workflow prescribed in the panel below==. Details of the photo to be added is given below the expandable panel. {text="3.5"}
  {{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking-prs-creating", "Admin " + icon_embedding + " Appendix E(extract): **Using PRs to track task progress -> Creating PRs**", "1", indent="1") }}

<div class="indented-level1">
<box>

* ##### Adding a photo {icon="https://upload.wikimedia.org/wikipedia/en/thumb/b/b1/Portrait_placeholder.png/600px-Portrait_placeholder.png?20210811085635" i-width="100px" i-class="rounded" }
  * Add a suitable photo of yourself, as described <trigger trigger="click" for="modal:mid-v12-photo">here</trigger><br>
  * The filename of the profile photo should be<br>
    `docs/images/github_username_in_lower_case.png`<br>
    Note the need for ==lower case== (<popover content="GitHub usernames are not case sensitive, but URLs in GitHub-pages are -- to avoid any mismatches, we have fixed the file name here to be lower case">%%why lowercase?%%</popover>) %%e.g. `JohnDoe123` -> `docs/images/johndoe123.png` not `docs/images/JohnDoe123.png`%%.<br>
    If your photo is in jpg format, ==name the file as `.png`== anyway.
</box>
</div>

<modal large header="Admin {{ icon_embedding }} Choosing a profile photo" id="modal:mid-v12-photo">
<include src="tp-deliverables-website-fragment.md#profile-photo"/>
</modal>

* Get a team member to review the PR. For example, the reviewer can check if,<br>
  {{ icon_tick }} the file is in the right location,<br>
  {{ icon_tick }} the file name is as expected,<br>
  {{ icon_tick }} the PR is sent from a fork, and is from a separate branch,<br>
  {{ icon_tick }} commit messages comply with the [Git Conventions]({{ baseUrl }}/admin/standardsAndConventions.html). {text="3.6"}
{{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking-prs-reviewing", "Admin " + icon_embedding + " Appendix E(extract): **Using PRs to track task progress -> Reviewing PRs**", "1", indent="1") }}

* Merge the PR.<br>
  After that, sync your local repo and your fork with the team repo. {text="3.7"}
{{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking-prs-merging", "Admin " + icon_embedding + " Appendix E(extract): **Using PRs to track task progress -> Merging PRs**", "1", indent="1") }}

* Good job on merging the first PR into the team repo! {text="3.8"}
</div>

4. [each member] **Update the AboutUs page ==as parallel PRs==**. In this step, we are going to attempt sending parallel PRs that update the same page, which means there is a potential for merge conflicts (hence, you get to practice resolving merge conflicts in a team project):

<div class="indented-level1">

* Create an issue, and a PR, for the following task, similar to steps 3.2-3.5 above (==do not merge the PR yet==). {text="4.1"}

<div class="indented-level1">
<box>

****Updating the _AboutUs_ page:****

This page  (in the `/docs` folder) is used for course admin purposes. ==Please follow the format closely== or else our scripts will not be able to give credit for your work. Similarly, ==do not split the given `.md` files further into multiple files==, as our grading script will check the given files only.

* Add your own details.
* There is no need to mention the tutor/lecturer, but OK to do so too.
* Indicate the different roles played and responsibilities held by each team member. You can reassign these <trigger trigger="click" for="modal:midv11-rolesAndResponsibilities">roles and responsibilities %%(as explained in Admin {{ icon_embedding }} Project Scope)%%</trigger> later in the project, if necessary.

</box>
</div>

<modal large header="Admin {{ icon_embedding }} Project Scope (extract): roles and responsibilities" id="modal:midv11-rolesAndResponsibilities">
<include src="tp-expectations.md#roles"/>
</modal>

* #r#Wait until all team members have sent the PR## for the above step.<br>
  Reviews each other's PRs while waiting.{text="4.2"}

{{ show_faq("tpOneMemberNotDone") }}

* Merge one of the PRs sent in step 4.1 (e.g., the one that arrived first). If this causes conflicts in other PRs, resolve those conflicts.<br>
  {{ icon_tip }} [This week's tP briefing video `tP Briefing video (Part 2a -- v1.1, Workflow)`]({{ baseUrl }}/schedule/week7/index.html) has a section on how to resolve conflicts in PRs.{text="4.3"}
* Merge remaining PRs one at a time, while resolving merge conflicts as needed.{text="4.4"}
* Check the AboutUs page in your teams repo to confirm if the page appears as expected. [Here]({{ url_ab3_upstream_website}}/AboutUs.html) is an example.<br>
  If something is not right, you might have to create another PR to rectify it.{text="4.4"}

</div>

5. Congrats! You are done with this workflow practice session. It might have felt like a lot of 'jumping through hoops' for very little gain but as you go through the tP, this 'workflow overhead' is expected to feel progressively less 'draggy'. Hopefully, it will be almost second nature to you by the time you finish the tP.

</div>
{#====================================================================================================================#}
<span id="heading_divide_mvp_features">{{ icon_team }} Divide MVP features among members</span>
<div id="desc_divide_mvp_features">

<box type="info" seamless>

Although MVP version is scheduled to be released in `{{ version_mvp }}` and not in the current iteration `{{ version_first }}`, in this task we refine the MVP features and divide them among the team members, because MVP is the first full product version anyway (i.e., there is nothing earlier that we can aim our plans at).
</box>

* {{ icon_team }} **Re-confirm MVP feature design**. Recall that you decided on features to include in the MVP version of the product. Revisit that design. Ensure the following (you may refine the MVP feature design if necessary).
  * It consists of not only<br>
    **the most essential features** of the target product, but also,<br>
    **the simplest implementation of those features** %%(e.g., when adding a new feature to track birthdays of contacts, the simplest implementation of it could be simply adding a new text field for the contact)%%.
  * It will **still be a working product** (i.e., it _can_ be used)<br>
    %%Reason: As we are following the breadth-first iterative approach, each intermediate version should be a working product.%%
* {{ icon_team }} **Divide the features among the team members** i.e., who will be implementing which feature.
  * Reminder: We recommend that the work to be ==divided primarily based on features/enhancements, not by components==.

{{ show_faq("tpNotEnoughMvpFeaturesToDivide") }}

<box>

**{{ icon_tip }} Ways to level up your tP game:**{.text-success}

Consider the feature flaws and implementation bugs in the panels below that could cost you marks if they remained in the final version %%(these panels are extracts from the final product evaluation instructions given in the practical exam)%%. If they are avoided from the start, there is no need to hunt them down and fix them later.<br>
Tip: Especially ==note the part on _overzealous input validation_==, which is a common issue found in tPs.

<panel header="Admin {{ icon_embedding  }} tP: Practical Exam (PE) → Guidelines for bug triaging (extract 1)" peek>
<include src="tp-pe-bug-triaging-guidelines-fragment.md#triaging-functionality-bugs" />
</panel>
<panel header="Admin {{ icon_embedding  }} tP: Practical Exam (PE) → Guidelines for bug triaging (extract 2)" peek>
<include src="tp-pe-bug-triaging-guidelines-fragment.md#triaging-feature-flaws" />
</panel>

{{ show_faq("tpMultiStepCmd") }}

</box>
</div>
{#====================================================================================================================#}
<span id="heading_plan_the_next_iteration">{{ icon_team }} Plan the next iteration (`{{ version_mvp }}`)</span>
<div id="desc_plan_the_next_iteration">

* {{ icon_team }} **Plan the next iteration**. As you know, you should follow the _breadth-first iterative_ process. Therefore, first you must decide what functionalities should be in the product if you had only two weeks to implement it. You have done that already when you chose user stories for {{ version_mvp }}, translated that to features, and even drafted the UG based on those features. You can tweak that plan further at this point if you wish.
  * ==**Aim to produce a _working_ [MVP](https://en.wikipedia.org/wiki/Minimum_viable_product)**== at the end of this iteration even if the functionalities are not polished (polishing can be done in a later iteration).
  * **Avoid depth-first implementations**: "I'll do the back-end part of feature X in this iteration" is not acceptable as that is not in the spirit of breadth-first iterative process. Remember, we are pretending this to be the last iteration; why would you implement the back-end part of a feature in the last iteration?<br>
    It is OK to add simpler versions of bigger features, but not OK to add partial features that can't be used yet.
* {{ icon_team }} **Divide the work among the team members** i.e., the work required for the current iteration.
* {{ icon_individual }} **Reflect the above plan in the issue tracker** by creating and assigning issues to yourself and to the corresponding milestone. The panel below explains the full workflow we prescribe you to follow in the tP.
  {{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking", "Admin " + icon_embedding + " Appendix E(extract): **Project schedule tracking**", "1", indent="1") }}
</div>
{#====================================================================================================================#}
<span id="heading_start_the_next_iteration">{{ icon_team }} Start the next iteration</span>
<div id="desc_start_the_next_iteration">

* **Stronger teams are welcome to stay one week ahead of the tP schedule.**{.text-success}
  So, feel free to move on to next week's tp tasks, and get started on the next iteration (i.e., `{{ version_first }}`).
</div>
{#====================================================================================================================#}
<span id="heading_start_implementing_first_version">{{ icon_individual }} Start implementing {{ version_mvp }}</span>
<div id="desc_start_implementing_first_version">

<div class="indented-level2">

<box>

{{ icon_tip }} **You may <tooltip content="i.e., copy-paste, not clone/fork">re-purpose/adopt</tooltip> code** from any of the below to be used in your tP, provided you give credit to the source (and do not claim such code as yours).
* The iP code of any of your team members, or of any other person in the course.
* Code from [AddressBook-Level2](https://se-education.org/addressbook-level2/) or any code used in course activities e.g., personbook

</box>

</div>

* Start implementing {{ version_mvp }}, by adding code in small steps, while working in parallel, aiming to produce a VERY simple working version after one week, and a bit more functional version at the end of iteration (i.e., after two weeks).

* See the panel below the project workflow we prescribe for the tP.

{{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking", "Admin " + icon_embedding + " Appendix E(extract): **Project schedule tracking**", "1", indent="1") }}

</div>
{#====================================================================================================================#}
<span id="heading_ensure_you_know_tp_expectations">%%{{ icon_individual }} Ensure you know tP expectations%%</span>
<div id="desc_ensure_you_know_tp_expectations">

* If you haven't done so already, make sure you know individual and team expectations of the tP

{{ embed_topic("tp-expectations.md#functionalityExpectations", "Admin " + icon_embedding + " tP: Functionality Expectations", "3", indent="1") }}
{{ embed_topic("tp-expectations.md#individualExpectations", "Admin " + icon_embedding + " tP: Individual Expectations (and ==guidance on work distribution==)", "3", indent="1") }}
{{ embed_topic("tp-expectations.md#teamExpectations", "Admin " + icon_embedding + " tP: Team Expectations", "3", indent="1") }}
{{ embed_topic("tp-supervision.md#making-project-decisions", "Admin " + icon_embedding + " tP → Supervision (Extract) → **Tutor's role in making project decisions**", "3", indent="1") }}
</div>
{#====================================================================================================================#}
<span id="heading_start_proper_milestone_management">{{ icon_team }} Start proper milestone management</span>
<div id="desc_start_proper_milestone_management">

* **Set up the issue tracker** as described in the panel below, if you haven't done so already.

{{ embed_topic("appendixE-gitHub.md#issue-tracker-setup", "Admin " + icon_embedding + " Appendix E(extract): **Setting up the issue tracker**", "1", indent="1") }}

* **Start proper schedule tracking and milestone management** as explained in the panel below.

{{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking", "Admin " + icon_embedding + " Appendix E(extract): **Project schedule tracking**", "1", indent="1") }}

<div class="indented">

{{ icon_tip }} **Try to achieve all milestone requirements, but do not fret if you miss a few**.  You will get full marks for this aspect as long as you achieve about 75% of the milestone requirements on average. Yes, that's a pretty low bar, but we have set it low in order to reduce workload and stress. Ideally, you should achieve 90-100%.
</div>
</div>
{#====================================================================================================================#}
<span id="heading_use_github_to_manage_milestones">{{ icon_team }} Use GitHub to manage milestones</span>
<div id="desc_use_github_to_manage_milestones">

* We ==recommend== using the GitHub issue tracker and its _milestones_ feature to manage your project milestones, as explained in the following panels.

{{ embed_topic("appendixE-gitHub.md#issue-tracker-setup", "Admin " + icon_embedding + " Appendix E(extract): **Setting up the issue tracker**", "1", indent="2") }}
{{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking", "Admin " + icon_embedding + " Appendix E(extract): **Project schedule tracking**", "1", indent="2") }}

</div>
{#====================================================================================================================#}
<span id="heading_rename_packages">%%{{ icon_team_rep }} [Optional] Rename packages/classes%%</span>
<div id="desc_rename_packages">

* **If you wish to rename AB3 packages/classes** to fit your product, this is the best time to do so (i.e., before starting any functionality changes), as such changes cause widespread changes to the codebase, causing many merge conflicts with any other ongoing PRs.
* **Renaming packages/classes is optional**. It is fine to keep the existing ones. But if you decide to rename them, do it quickly, and probably best done by one person in one shot (to minimize merge conflicts).

</div>
{#====================================================================================================================#}
<span id="heading_add_first_functionality_increment">{{ icon_individual }} Add the first functionality increment</span>
<div id="desc_add_first_functionality_increment">

<box type="important" seamless>

**Each member is expected to <tooltip content="i.e., merge at least one PR">merge _some_ code</tooltip> in each <tooltip content="{{ version_first }}, {{ version_mvp }}, {{ version_alpha }}, etc."> iteration</tooltip>.**<br>
  %%Reason: As each iteration focuses on a different learning outcome, it is better for you to take part in each of them fully.%%

{{ show_faq("tpNoPrInIteration") }}
</box>
<box type="tip" seamless>

**Prefer smaller PRs**.<br>
  %%Reason: The **ability to divide work into small yet meaningful PRs** is another intended learning outcome.%%

* For example, suppose you are asked to implement a feature F in the current iteration. Instead of creating one big PR for it, you can start with a smaller PR that implements a very VERY simple version of F, followed by a few more PRs that improve F incrementally.
* %%{{ icon_resource }} Side reading : [blog post] [Small Pull Requests: 6 reasons why they are the best choice](https://blog.codacy.com/small-pull-requests).%%
</box>

****Steps:****

* {{ icon_individual }} **Select a code change to implement**, as follows:{text="S1." t-class="fw-bold"}
  * Consider the feature that you have been assigned to implement for the upcoming MVP version of the product (which will be released by the iteration `{{ version_mvp }}`, not by the current iteration `{{ version_first }}`).
  * Pick a small code change that you'll need to do to implement that feature. This is a small code change contributing towards the feature, not the entire feature itself. %%Examples: add parser support for a new command word, add a field to the person class%%.<br>
   This code change should not 'break' the code base though (e.g., it should not refer to a class that you plan to add in a future PR but doesn't exist yet). Ideally, it should not cause any existing tests to break either. That is, the change should take the codebase forward in a meaningful way.
* {{ icon_individual }} **Implement that code change while following the workflow** that you practiced in the previous week. A summary of the steps:{text="S2."}
    * Create an issue for it. Assign it to yourself. Assign it to milestone `{{ version_first }}`.
    * Create a PR from a separate branch in your fork. Assign it to `{{ version_first }}`.
    * Get the PR reviewed.
    * Get the PR merged. Close the corresponding issue.
* {{ icon_individual }} **Continue to implement more code changes** (i.e., repeat S1 and S2) to implement more code changes that move you towards your MVP feature(s). Recommended to create <tooltip content="i.e., while waiting for one PR to be merged, create a new PR to fix another issue">parallel PRs</tooltip>, when implementing code changes with no/low dependency between them.{text="S3."}
* {{ icon_team }} **Wrap up the milestone** When the iteration period is over, do the following:{text="S4."}
  * Move any pending issues/PRs to the next milestone (i.e., `{{ version_mvp }}`). %%As you do not need to release a product version at the end of this iteration, we can freely move any pending work to the next iteration.%%
  * Close the milestone.
  * There is no need to do a product release.

{{ show_faq("tpHowMuchCodeInV12", is_compact=1) }}
{{ show_faq("tpIterationDeadline", is_compact=1) }}
{{ show_faq("tpMissingIterationDeadlines", is_compact=1) }}
{{ show_faq("tpUpdateTestsWithCode", is_compact=1) }}
{{ show_faq("tpCodecovFails", is_compact=1) }}
{{ show_faq("tpIsCiPassingCompulsory", is_compact=1) }}
{{ show_faq("tpAddChangesInFeatureBranch", is_compact=1) }}
{{ show_faq("tpUpdateDocsWithCode", is_compact=1) }}
{{ show_faq("tpChangeFeatureSpec", is_compact=1) }}
{{ show_faq("tpRationaleForCurrentDesign", is_compact=1) if cs2103 }}

</div>
{#====================================================================================================================#}
<span id="heading_add_junit_tests">{{ icon_individual }} Add some JUnit Tests</span>
<div id="desc_add_junit_tests">

* We recommend that each person adds some JUnit tests to test their tP code.

* Some examples from [AddressBook-Level2](https://github.com/se-edu/addressbook-level2):
  * <tooltip content="Software Under Test">SUT</tooltip>[`seedu.addressbook.common.Utils.java`](https://github.com/se-edu/addressbook-level2/blob/master/src/seedu/addressbook/common/Utils.java)<br>
    Tests: [`seedu.addressbook.common.UtilsTest.java`](https://github.com/se-edu/addressbook-level2/blob/master/test/java/seedu/addressbook/common/UtilsTest.java)<br>
    {{ icon_info }} Note how **the test class is in the same package as the SUT** (although in a different folder). Advantage: the test class has access to all non-private members of the SUT, including _package private_ members.
  * SUT: [`seedu.addressbook.parser.Parser.java`](https://github.com/se-edu/addressbook-level2/blob/master/src/seedu/addressbook/parser/Parser.java)<br>
    Tests: [`seedu.addressbook.parser.ParserTest.java`](https://github.com/se-edu/addressbook-level2/blob/master/test/java/seedu/addressbook/parser/ParserTest.java)<br>
    {{ icon_info }} Note how some of the test methods follow a different naming convention e.g., `parse_emptyInput_returnsIncorrect()`. Cross-check the coding standard to confirm if this naming convention is allowed.
  * SUT: [`seedu.addressbook.data.AddressBook.java`](https://github.com/se-edu/addressbook-level2/blob/master/src/seedu/addressbook/data/AddressBook.java)<br>
    Tests: [`seedu.addressbook.data.AddressBookTest.java`](https://github.com/se-edu/addressbook-level2/blob/master/test/java/seedu/addressbook/data/AddressBookTest.java)
</div>
{#====================================================================================================================#}
<span id="heading_plan_the_first_product_release">{{ icon_team }} Plan the first product release (`{{ version_mvp }}`)</span>
<div id="desc_plan_the_first_product_release">
<box type="warning" seamless>

Note that the product you deliver at the end of this iteration must be working although the functionality is basic.
</box>

* **Revise the iteration target, if necessary** e.g., if `{{ version_first }}` iteration felt like your progress is much slower than you anticipated, you can explore if MVP can be trimmed-down even further, to increase your chances of reaching it in time.
* **Enumerate the plan: decide tasks, order, timeline.**
  1. Figure out what !!tasks!! needs to be done to reach `{{ version_mvp }}` product version.
  1. Decide if there is a certain !!order!! in which they need to be done (based on dependencies between them)
  1. Decide the !!timeline!! on which you need to finish each.
* **Document the plan: create issues, assign milestone, and members.**
  1. Create issues to match the tasks you enumerated above.<br>
     {{ icon_tip }} In the issue description, you can mention when a task needs to be done (e.g., `due: Monday`). Alternatively, you can create a bunch of labels for recording due dates (e.g., {{ as_tag('due:Monday') }})
  1. Assign them to the milestone `{{ version_mvp }}`.
  1. Assign each of those issues to the person responsible for doing it.

</div>
{#====================================================================================================================#}
<span id="heading_deliver_first_version">{{ icon_team }} Manage the iteration, and deliver `{{ version_mvp }}`</span>
<div id="desc_deliver_first_version">

<div tags="m--cs2103">


<div id="level-up-ug-updates" class="indented">
<box>

**{{ icon_tip }} Ways to level up your tP game:**{.text-success}

* **Consider updating the UG as you go**{.text-success}. As you implement a feature/enhancement, consider updating the user guide (UG) to match the new behavior.
* **Start reviewing each other's PRs**{.text-success} _seriously_, and giving thoughtful review comments (i.e., as opposed to approving after a superficial look), if you haven't done so already.

{{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking-prs-reviewing", "Admin " + icon_embedding + " Appendix E(extract): **Using PRs to track task progress -> Reviewing PRs**", "1", indent="1") }}


</box>
</div>

<box type="important" seamless>

#r#**Finishing the iteration on time is no longer 'optional'!**## From {{ version_mvp }} iteration, the {{ as_tag( 'v1._ on time', tag_style='dark') }} item in the [tP dashboard]({{ url_tp_progress_dashboard_team }}) will turn red and remain red if the iteration wasn't wrapped up properly by the deadline (i.e., Thu 23:59).<br>
 %%Reason: Learning to meet project deadlines is an intended learning outcome. As this is the third tP iteration, you should be able to finish iterations on time by now.%%
</box>

* {{ icon_team }} **Manage the iteration** `{{ version_mvp }}`, and reach the milestone `{{ version_mvp }}` (which delivers product version `{{ version_mvp }}`)
* {{ icon_team }} **Aim to deliver on time**, as that is linked to our tP learning outcome of this iteration. This means you need to monitor progress, and course-correct as you go.
  * Revise the MVP design further, if needed. If you think some of the ongoing work intended for the current iteration may not finish in time, you can reassign them to a future iteration, provided they are not _essential_ for the `{{ version_mvp }}` %%(i.e., you can still get a 'working product' without them)%%.
  * <tooltip content="e.g., change scope">Revise</tooltip> or <tooltip content="i.e., reassign to a future milestone">reschedule</tooltip> issues/PR accordingly.
* **Do a release on GitHub**, when the product `{{ version_mvp }}` is ready. Requirements:
  * **==Write a fairly detailed _Release Note_==** in the text field GitHub provides for the description of the release. In particular, describe what has been changed (compared to AB3). This is just an itemized list of _What's New_ -- no need to be as elaborate as a user guide.<br>
    **Include screenshots** (or screen recordings) of your product in action, featuring the changes you've done.<br>
    {{ icon_important_big_red }} <span class="text-danger">These release notes will be checked by the teaching team</span> to verify (a) that they are written reasonably well, and, (b) that the features mentioned in there show the product has reached the MVP level of functionality.
  * **Upload the JAR file** as well. Instructions for creating a JAR file can be found in [as described in the tP Developer Guide]({{ url_ab3_fork_website }}/DevOps.html#making-a-release).
* **Wrap up the milestone** on GitHub, when you are done with this iteration and the MVP has been released.

{{ show_faq("tpPrReviewRigor", is_compact=1) }}
{{ show_faq("tpGuiTestAutomation", is_compact=1) }}
{{ show_faq("tpWorksLocallyFailsCi", is_compact=1) }}
{{ show_faq("tpPrPassCiButFailedAfterMerging") }}

%%Some other relevant FAQs, repeated from last week:%%

{{ show_faq("tpUpdateTestsWithCode", is_compact=1) }}
{{ show_faq("tpCodecovFails", is_compact=1) }}
{{ show_faq("tpIsCiPassingCompulsory", is_compact=1) }}
{{ show_faq("tpAddChangesInFeatureBranch", is_compact=1) }}
{{ show_faq("tpUpdateDocsWithCode", is_compact=1) }}
{{ show_faq("tpChangeFeatureSpec", is_compact=1) }}
</div>
<div tags="m--cs2113">

* When the {{ version_mvp }} is ready, do a release on GitHub. Remember to upload the jar file as well.
* Wrap up the milestone on GitHub.

{{ embed_topic("appendixE-gitHub.md#tp-schedule-tracking", "Admin " + icon_embedding + " Appendix E(extract): **Project schedule tracking**", "1", indent="1") }}
</div>
</div>
{#====================================================================================================================#}
<span id="heading_wrap_up_first_version">{{ icon_team }} Wrap up {{ version_mvp }}</span>
<div id="desc_wrap_up_first_version">

* **Wrap up the milestone** using a git tag `{{ version_mvp }}`. When the milestone deadline is near (e.g., 0.5 days before the deadline), if you think some of the ongoing work intended for the current milestone may not finish in time, you can reassign them to a future milestone, provided they are not _essential_ for the `{{ version_mvp }}` (i.e., you can still get a 'working product' without them).

</div>
{#====================================================================================================================#}
<span id="heading_start_updating_uml_diagrams">{{ icon_individual }} Start updating UML diagrams in the DG</span>
<div id="desc_start_updating_uml_diagrams">

<box type="tip" seamless>

This is a good time to get familiar with the diagramming tools used by the tP.
</box>

* {{ icon_individual }} **Each member is recommended to update at least one UML diagram in the DG**, to match the changes you've done so far in `{{ version_alpha }}`. You may do this towards the end of `{{ version_alpha }}`, or soon after you finish it.
* **Deadline**: This is not part of `{{ version_alpha }}`. So, you can do this even *after* you are done with the `{{ version_alpha }}` release that is due Thursday 23:59.<br>
  As this is a regular weekly task, the usual deadline applies i.e., Friday {{ time_lecture_start }}, and as usual, if you miss the deadline, catching up within a few days will still turn it green.
* Updating the DG text to match the diagrams is optional (it can be done later).
* FYI, the panel below has some DG tips, some of which are related to drawing diagrams.

<div class="indented">
<panel type="light" minimized>
<div slot="header" class="card-title">

<span> {{ icon_tip }} Admin {{ icon_embedding }} tP Deliverables → DG → Tips</span>
</div>
<div id="dgTips">

<include src="tp-deliverables-dg-fragment.md#dgTips" />
</div>
</panel>
<p/>
</div>
{{ show_faq("tpWhyUpdateDiagramsEarly", is_compact=1) }}
{{ show_faq("dgAddNewUml", is_compact=1) }}
{{ show_faq("noEffectOnUml", is_compact=0) }}

</div>
{#====================================================================================================================#}
<span id="heading_do_an_informal_demo">{{ icon_team }} Do an informal demo of {{ version_mvp }}</span>
<div id="desc_do_an_informal_demo">

<div id="demo">

1. **Run your app using the latest released version `{{ version_mvp }}`** <span tags="m--cs2103">(or `{{ version_mvp }}b`, if applicable)</span>. {% if cs2113 %}
1. **Take screenshots** of each available feature in action.
1. **Add those screenshots to the shared workspace.**<br>You can also add the screenshots to your _project notes_ document with an appropriate heading e.g., `{{ version_mvp }} features demo`, and reuse them as necessary in the documentation.{% else %}
1. **Take screenshots** of ==each updated feature in action== (if the feature is not obvious from the screenshot, you can annotate the screenshot to draw attention to where the feature appears in the screenshot).
1. **Add those screenshots to your _project notes_ document** (the same document specified in [this page](teamList.md)) with an appropriate heading e.g., `{{ version_mvp }} features demo`.<br> Alternatively, you can screen-record a demo, upload it to somewhere, and post the link in the project notes document.{% endif %}
</div>
</div>
{#====================================================================================================================#}
<span id="heading_do_a_postmortem">{{ icon_team }} Do a postmortem of the previous iteration</span>
<div id="desc_do_a_postmortem">

* Discuss with the team how the iteration went (i.e., what worked well, what didn't), and your **plans to improve the process** (not the product) in the next iteration.
* **Submission:** Keep notes about the discussion in your shared _project notes document_ so that the tutor can check them later.

<box type="tip" seamless>

**Like to try a new Git workflow?** If you feel you are now comfortable with the forking workflow, and now you would like to practice another one, your team  can choose to follow the <trigger trigger="click" for="modal:postmortemTip-featurebranchworkflow">feature branch workflow</trigger> from now on.
</box>

<modal large header="TextBook {{ icon_embedding }}" id="modal:postmortemTip-featurebranchworkflow">
<include src="../book/gitAndGithub/featureBranchFlow/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>
</div>
{#====================================================================================================================#}
<span id="heading_plan_the_alpha_version">{{ icon_team }} Plan the alpha version (`{{ version_alpha }}`)</span>
<div id="desc_plan_the_alpha_version">

<box type="secondary" icon=":fas-quote-left:" seamless>

%%The first 90 percent of the code accounts for the first 90 percent of the development time. The remaining 10 percent of the code accounts for the other 90 percent of the development time.%%

%%<small>--Tom Cargill, Bell Labs</small>%%
</box>

* **Decide the scope:** Start by deciding what features you would include in the final product !!if you had only one more week to deliver!! them. In this iteration, aim to deliver at least a <popover content="i.e., the feature is working and accessible to users, although it might not handle all the corner cases, and the UI/UX might not be fully polished yet">fully-fledged (albeit not-yet-polished)</popover> version of those features.<br>
  **:thinking: What's the hurry to add _all_ features right now?** We will be enforcing a strict _feature freeze_ at the end of `{{ version_penultimate }}` (more details in the panel below). Given you also need time to polish the features before the feature freeze starts (during which code changes will be severely restricted), it makes sense to finish the bulk of the feature implementation in this iteration (`{{ version_alpha }}`), so that you have time to test and polish it in `{{ version_penultimate }}`.

<div class="indented-level1">

<panel header="Admin {{ icon_embedding }} tP → **{{ version_final }} (extract) → More details on the feature freeze**" peek>

<include src="tp-tasks-fragment.md#feature-freeze-details" />
</panel>
<p/>
</div>

* **Plan the iteration**: Decide the order/timeline for those features, record that plan using issues, and assign team members to those issues. Plan tasks based on priority, while staying breadth-first.
</div>
{#====================================================================================================================#}
<span id="heading_deliver_the_alpha_version">{{ icon_team }} Deliver the alpha version (`{{ version_alpha }}`)</span>
<div id="desc_deliver_the_alpha_version">

* **Follow the iteration plan** you devised above,  to deliver the features.<br>
Resist the temptation to try to deliver each of those features/enhancements in one PR. It is better to deliver a minimal version first, and improve it through subsequent PRs.
* **Manage the iteration** better than the previous iteration (hopefully), as per what you learned/decided during the `{{ version_mvp }}` postmortem.
* **Release `{{ version_alpha }}`.** Include a jar file and detailed release notes (as before, the release notes should describe _what's-new-since-the-last-release-note_).
<box>

##### {{ icon_tip }} Ways to level up your tP game:{.text-success}

1. <span class="text-success">**Use parallel PRs:**</span> We encourage you to try sending parallel PRs (i.e., send another PR while the previous PR you sent is waiting to be merged) if you haven't done that yet.<br>
   Reason: It's important to learn how to do that, because in most real projects it is common to have ==multiple open PRs from the **same author**==.<br>
   {{ icon_important_big_red }} We require each student to have parallel PRs at least once during the tP %%so that we can confirm you are able to handle parallel PRs%%.
1. **Maintain the defensiveness of the code:**{.text-success} Use assertions, exceptions, and logging in your code, as well as other defensive programming measures (refer this week's topic on _defensive programming_ for more details) when appropriate. This will be considered when grading your tP code quality.<br>
   Remember to [enable assertions in your IDEA run configurations](https://se-education.org/guides/tutorials/intellijUsefulSettings.html) and [in the gradle file](https://se-education.org/guides/tutorials/gradle.html#enabling-assertions).
</box>

{{ show_faq("tpFeatureDesignChoice", is_compact=1) }}
{{ show_faq("tpHowMuchToGetFullMarks", is_compact=0) }}

%%Some other relevant FAQs, repeated from last week:%%

{{ show_faq("tpGuiTestAutomation", is_compact=1) }}
{{ show_faq("tpWorksLocallyFailsCi", is_compact=1) }}
{{ show_faq("tpPrPassCiButFailedAfterMerging") }}
{{ show_faq("tpCodecovFails", is_compact=1) }}
{{ show_faq("tpChangeFeatureSpec", is_compact=1) }}

</div>
{#====================================================================================================================#}
<span id="heading_start_on_the_penultimate_version">{{ icon_individual }} Start the next iteration</span>
<div id="desc_start_on_the_penultimate_version">
<div class="indented">

As you did in the previous iteration,
* **Plan the next iteration** (steps are given below as a reminder):
  * {{ icon_team }} Decide which enhancements will be added to the product in this iteration, assuming this is the last iteration.
  * {{ icon_team }} If possible, split that into two incremental versions `{{ version_penultimate }}` and `{{ version_penultimate }}b`.
  * {{ icon_team }} Divide the work among team members.
  * {{ icon_individual }} Reflect the above plan in the issue tracker.
* {{ icon_individual }} **Start implementing** the features as per the plan made above.
* {{ icon_team }} **Track the progress** using GitHub issue tracker, milestones, labels, etc.

In addition,
* **Maintain the defensiveness of the code**: Remember to use assertions, exceptions, and logging in your code, as well as other defensive programming measures when appropriate.<br>
  {{ icon_important_big_red }} Remember to [enable assertions in your IDEA run configurations](https://se-education.org/guides/tutorials/intellijUsefulSettings.html) and [in the gradle file](https://se-education.org/guides/tutorials/gradle.html#enabling-assertions).
* {{ icon_tip }} Recommend: **Each PR should also update the relevant parts of documentation and tests**. That way, your documentation/testing work will not pile up towards the end.

</div>
</div>
{#====================================================================================================================#}
<span id="heading_make_code_more_defensive">{{ icon_individual }} Make the code more defensive</span>
<div id="desc_make_code_more_defensive">

* **Improve the defensiveness of the code**: We recommend you add assertions, exceptions, and logging to your code.<br>
  {{ icon_important_big_red }} Remember to enable assertions in your,
  * [IDEA run configurations](https://stackoverflow.com/questions/18168257/where-to-add-compiler-options-like-ea-in-intellij-idea) -- if your IntelliJ is set not to use Gradle when running the project)
  * [the `build.gradle` file](https://stackoverflow.com/questions/48396274/how-to-enable-assertions-in-the-gradle-run-task) -- if you use Gradle to run the project, or if your IntelliJ is using Gradle to run the project
</div>
{#====================================================================================================================#}
<span id="heading_update_dg_with_design_details">{{ icon_individual }} Update the DG with design details</span>
<div id="desc_update_dg_with_design_details">

<box type="important" seamless>

**Do this before next week Wednesday ({{ get_date(date_w11_start, 2, time="") }})** so that the added sequence diagrams can get peer feedback via the DG peer review that will happen during this week's tutorial. Diagrams you add before the deadline will receive feedback while diagrams added later will not.
</box>

* **Update the Developer Guide** as follows:
  * ==Each member should describe the implementation of at least one enhancement she has added== (or planning to add). <br>
    Expected length: 1+ page per person{% if cs2113 %}
  * Describing the design at a multiple-levels (e.g., first, describe at _architecture-level_, then describe at _component-level_) is optional. It is also acceptable to have one _Design & Implementation_ section in which you describe the entire thing at the class- and object-level.{% endif %}
  * The description can contain things such as,
    * How the feature is implemented (or is going to be implemented).
    * Why it is implemented that way.
    * Alternatives considered.
  * Minimally, add sequence diagrams to enhance your DG wherever they can be useful.
<div class="indented-level2">

<panel type="success" peek>
<div slot="header" class="card-title">

##### <span class="text-white"> {{ icon_tip }} Admin {{ icon_embedding }} tP Deliverables → DG → Tips</span>
</div>
<div id="dgTips">

<include src="tp-deliverables-dg-fragment.md#dgTips" />
</div>
</panel>
<p/>
</div>
</div>
{#====================================================================================================================#}
<span id="heading_make_code_reposense_compatible">{{ icon_individual }} Ensure the code is RepoSense-compatible</span>
<div id="desc_make_code_reposense_compatible">

<div id="midV13-repoSenseCompatible">

* **Ensure your code is <tooltip content="i.e., RepoSense can detect your code as yours">RepoSense-compatible</tooltip>** and the **code it attributes to you is indeed the code written by you**, as explained below:
  * Go to the [tp Code Dashboard]({{ url_tp_dashboard }}). Click on the `</>` icon against your name and verify that the ==lines attributed to you (i.e., lines marked as green)== reflects your code contribution correctly. This is important because some aspects of your project grade (e.g., code quality) will be graded based on those lines.<br>
  &nbsp;&nbsp;&nbsp;&nbsp;<img src="images/greenLines.png" width="600">
  <p/>

  * More info on how to make the code RepoSense compatible:

{{ embed_topic("tools.md#reposense", "Admin " + icon_embedding + " Tools → RepoSense", "1", indent="2") }}

{{ show_faq("tpFeatureTakeovers") }}

</div>
</div>
{#====================================================================================================================#}
<span id="heading_settle_code_authorship">{{ icon_individual }} Settle code authorship</span>
<div id="desc_settle_code_authorship">

<box type="important" seamless>

#r#Do this before the feature freeze begins## (i.e., Friday 10am). Any changes done after that will be subjected to the limits of the feature freeze.
</box>

* **Ensure your code is <tooltip content="i.e., RepoSense can detect your code as yours">RepoSense-compatible</tooltip>** and the **code it attributes to you is indeed the code written by you**, as explained below:
  * Go to the [tp Code Dashboard]({{ url_tp_dashboard }}). Click on the `</>` icon against your name and verify that the ==lines attributed to you (i.e., lines marked as green)== reflects your code contribution correctly. This is important because some aspects of your project grade (e.g., code quality) will be graded based on those lines.<br>
  &nbsp;&nbsp;&nbsp;&nbsp;<img src="images/greenLines.png" width="600">
  <p/>

  * More info on how to make the code RepoSense compatible:

{{ embed_topic("tools.md#reposense", "Admin " + icon_embedding + " Tools → RepoSense", "1", indent="2") }}

{{ show_faq("tpFeatureTakeovers") }}

</div>
{#====================================================================================================================#}
<span id="heading_smoke_test_catcher">{{ icon_individual }} Smoke-test CATcher</span>
<div id="desc_smoke_test_catcher">

* **This activity is <span class="text-danger">compulsory</span> and counts for `3` participation points.** Please do it before the weekly deadline.
<div class="indented-level2">

<box dismissible>

%%**{{ icon_info }} Some background:** As you know, our <tooltip content="i.e., Practical Exam">PE</tooltip> includes peer-testing tP products under exam conditions. At the beginning, we used GitHub as the platform for that -- which was not optimal (e.g., it was hard to ensure the compulsory labels have been applied). As a remedy, some ex-students have been developing an app called <tooltip content="CAT stands for Crowd-sourced Anonymous Testing">CATcher</tooltip> that we'll be using for the PE. We still use GitHub to record bugs reported in the PE but CATcher acts as a layer between you and GitHub, to ensure the bugs you report meet PE requirements.%%
</box>

This week, we would like you to smoke-test the CATcher app **to ensure it can work with your OS, Browser, GitHub account**, by following the steps given in the panel below.
<p/>

<panel type="info" header="**Steps for smoke-testing CATcher:**" peek>

1. **Go to the CATcher Web version** at https://catcher-org.github.io/CATcher/ using ==the same computer (i.e., not a mobile device) that you plan to use for the practical exam==.
   * Use a common browser such as Chrome, Edge, Firefox, Safari
   * Allow popups from https://catcher-org.github.io/
   * If you encounter other problems at the app launch, refer to the [Notes on using CATcher](https://catcher-org.github.io/ug/).
1. **Login**: Choose the _session_ `{{ course_pair }} Smoke Test`, and submit.
   <pic eager src="images/catcherLogin.png"></pic>
1. In the next screen, login to CATcher using your GitHub account.<br>
   If the app asks for public repo access permissions, grant it (just go with the default settings).
1. **Let CATcher create a repo named `catcher-smoke-test`** in your GitHub account, when it asks for permission. That repo will be used to hold the bug reports you will create in this testing session.
1. **Use CATcher (not the GitHub Web/Mobile interface) to create 1-2 <tooltip content="i.e., bug reports containing some random content">dummy bug reports</tooltip>**. The steps are similar to how you would enter bug reports in the GitHub issue tracker. Include at least one screenshot in one of those bug reports.<br>
   {{ icon_tip }} you can ==copy-paste screenshots== into the bug description.<br>
   {{ icon_tip }} You can use Markdown syntax in the bug descriptions.<br>
   {{ icon_info }} The `severity` and `type` labels are compulsory.
1. **If you encounter any problems while using CATcher**, report them at the [CATcher issue tracker](https://github.com/CATcher-org/CATcher/issues).
1. **Do NOT delete the `catcher-smoke-test` repo** created by CATcher in your GitHub account (keep it until the end of the semester) as our scripts will look for it later to check if you have done this activity.

</panel>
<p/>
</div>

{% if cs2103 and catcher_load_testing %}
* **[Heads up] Load-testing CATcher will be done during the upcoming {{ lecture_name }}** ({{ get_date(date_w10_start, 4, time="") }}), during the first 15 minutes of
{{ lecture_name_short }}. This is ==different from smoke-testing== you did above, and this will count for participation separately.<br>
  Therefore, remember to ==attend the {{ lecture_name_short }} (via Zoom or F2F) at least for the first 15 minutes== (this activity cannot be done any other time).
{% endif %}

</div>
{#====================================================================================================================#}
<span id="heading_update_ug_dg">{{ icon_individual }} Update UG and DG</span>
<div id="desc_update_ug_dg">
<include src="tp-tasks-fragment.md#alert-time-sensitive" />

* {{ icon_important_big_red }} **Update the User Guide** to match the current version of the product. %%Reason: testers will need to refer to the UG during the practical exam dry run%%.
  * {% if cs2103 %}Remove mentions of any features not implemented yet, if any. As you are not allowed to change features during the iteration {{ version_final }}, there is no point keeping those in the UG.<br>
  Alternatively, clearly{% else %}Clearly{% endif %} indicate which features are not implemented yet %%e.g. tag those features with a `Coming soon`%%.
  * For those features already implemented, ensure their descriptions match the exact behavior of the product %%e.g. replace mockups with actual screenshots%%

{{ embed_topic("tp-deliverables.md#tp-deliverables-ug", "Admin " + icon_embedding + " tP → Deliverables → **User Guide**", "3", indent="1") }}


* **Save the UG as a PDF file** ==using [this technique](https://se-education.org/guides/tutorials/savingPdf.html) exactly==. You'll need this file later when you create a product release. There is no specific file name convention for this version of the UG, but do use a reasonable file name: e.g., `Contacts-Pro-User-Guide.pdf`.

{{ embed_topic("tp-tasks-fragment.md#caution-on-pdf-conversion", "Admin " + icon_embedding + " tP → **Caution on PDF conversions**", "3", indent="1") }}
{{ embed_topic("tp-constraints.md#Constraint-PDF-Friendly", "Admin " + icon_embedding + " tP Constraints → **Constraint-PDF-Friendly**", "2", indent="1") }}
{{ embed_topic("tp-constraints.md#Constraint-File-Size", "Admin " + icon_embedding + " tP Constraints → **Constraint-File-Size**", "2", indent="1") }}

* **Similarly, update the Developer Guide (DG), and save it as PDF file.**

{{ embed_topic("tp-deliverables.md#tp-deliverables-dg", "Admin " + icon_embedding + " tP → Deliverables → **Developer Guide**", "3", indent="1") }}
{{ embed_topic("tp-grading-bugs-fragment.md#dgBugs", "Admin " + icon_embedding + " tP Grading → **Possible DG Bugs**", "3", indent="1") }}


<div tags="m--cs2103">

* **Update the _landing page_ (`docs/index.md`)**: Update to look like a real product (rather than a project for learning SE) if you haven't done so already. In particular, ==update the `Ui.png` to match the current product (<trigger trigger="click" for="modal:v13-tipsForProductScreenshot">{{ icon_tip }} tips</trigger>)==.

<modal large header="Admin → Project Deliverables → Website -> Tips for Product Screenshots" id="modal:v13-tipsForProductScreenshot">
 <include src="tp-deliverables-website-fragment.md#tips-for-product-screenshot"/>
</modal>
</div>


</div>
{#====================================================================================================================#}
<span id="heading_alpha_test_product">{{ icon_team }} Alpha-test the product</span>
<div id="desc_alpha_test_product">

1. **Create a label `alpha-bug`** in your issue tracker.
1. **Plan the alpha test**:
   * Decide who will be testing which feature. Suggested: Assign two members (exclude the feature author) to test each feature.
   * Set a deadline (suggested: should be earlier in the iteration, as you need time to fix the reported bugs).
1. **Start testing** as soon as the `{{ version_alpha }}` jar file is ready.<br>
   ==Test using the JAR file==. If you have already added some more features since you released `{{ version_alpha }}`%%, you are free to do a new release (e.g., `{{ version_alpha }}.1`) and use that for alpha testing too.%%<br>
   Use the same steps we use in the PE, reproduced in the panel below.

{{ embed_topic("tp-ped-fragment.md#tp-jar-testing-steps", "Admin " + icon_embedding + " Practical Exam (Extract) → **Steps for testing a tP JAR file**", "1", indent="1", status="expanded") }}

4. **Report bugs** you found, and ==even suggestions for improvements==.
   * If in doubt, report anyway.
   * ==Apply the `alpha-bug` label== to the bug report, as our grading scripts will look for it when assessing your contribution level for this task.
   * {{ icon_important_big_red }} For this individual tP tasks to be marked as done, you need to submit at least 5 issues labelled `alpha-bug` %%i.e., If someone submit 5 alpha bugs, it is marked as 'done' for that person (irrespective of how many alpha-bugs other team members submit)%%.

<box type="tip" seamless>

If you want to smoke-test your JAR file on an OS not available within your team, you can post a request in the forum to see if anyone else in the class can help you smoke-test it on that OS.
</box>

<box type="tip" seamless>

The panel below contains guidelines your peers will use when determining bugs in the final product -- knowing them might be useful in preventing such bugs in your product in the first place. You may skip the 'General' section.
{{ embed_topic("tp-pe-bug-triaging-guidelines-fragment.md", "Admin " + icon_embedding + " Practical Exam → **Guidelines for determining bugs**", "3", indent="1") }}
</box>

<panel type="info" header="**Some testing tips** to get you started (not an exhaustive list)..." peek >

* If your app references date/time of the computer it is running on (e.g., to calculate time elapsed), test if it can work if the computer date/time is configured to be in different formats -- different computers might use different date formats.
* Test against all typical user mistakes %%e.g., typing two spaces instead of one%%
* If sorting is involved, verify the sorting behavior follows real world expectations %%e.g., lexicographical vs alphabetical order%%
* Input validation:
  * test valid and invalid inputs, typical and non-typical inputs
  * when a range is involved (e.g., start and end time), test for start-same-as-end and start-later-than-end cases
  * test command parameters: compulsory parameters missing, optional parameters are not given, parameters are duplicated, unexpected parameters are given, typos in parameter names, parameter names appearing inside the parameter value
* User-visible messages:
  * Are they specific enough? %%e.g., does the error message indicate what exactly is the error and how to rectify it?%%
  * Are they consistent with the UG?
  * Are they complete, and accurate?
* Clean up actions:
  * If a feature is supposed to clear/delete data, ensure all relevant data are deleted.
  * If there are multiple windows, ensure all windows are closed when the application exits.
* Does the application <popover content="good: gives an error message; bad: fails silently, crashes, corrupts data">fail gracefully</popover> when pushed beyond its limits?
* UI:
  * Does it work as expected when, used in different resolutions and display scaling settings?
  * Does it work as expected when, there are many data items, more than the display area can show at a time?
  * When a command is run, does all parts of the UI updates as expected? e.g., when an item is deleted, does that item disappear from the list of items currently shown?
</panel>

</div>
{#====================================================================================================================#}
<span id="heading_fix_alpha_test_bugs">{{ icon_individual }} Fix alpha-test bugs, fine-tune features{{ ", improve code quality" if cs2103 }}</span>
<div id="desc_fix_alpha_test_bugs">

* **Fix bugs found** during alpha testing.
* **Fine-tune features**, if needed. <br>
  Here is another reminder about what you can and can't do during {{ version_final }} _feature freeze_.

<div class="indented-level1">

<panel header="Admin {{ icon_embedding }} tP → **{{ version_final }} (extract) → More details on the feature freeze**" minimized>

<include src="tp-tasks-fragment.md#feature-freeze-details" />
</panel>
<p/>
</div>

<include src="tp-tasks-fragment.md#level-up-coverage" />

{{ show_faq("tpMustWeFixAllBugs", is_compact="1") }}
{{ show_faq("tpRenameAbReferences") }}

</div>
{#====================================================================================================================#}
<span id="heading_demo_penultimate_version">~~{{ icon_team }} Demo {{ version_penultimate }}~~</span>
<div id="desc_demo_penultimate_version">

<div id="demo">

{% if cs2103 %}==**To reduce workload, this deliverable <span class="text-danger">has been removed from tP requirements</span> this semester.**=={% endif %}
<s>

* ~~As was done in `{{ version_mvp }}`,~~
  * ~~Run your application using the ==JAR file== that you released for `{{ version_penultimate }}`.~~
  * ~~Take screenshots of each available feature in action (or screen-record a demo -- need not be polished).~~
  * ~~Add those screenshots (or upload the demo video somewhere and give the link) to your _project notes_ document with an appropriate heading e.g., `{{ version_penultimate }} features demo`.~~
</s>
</div>
</div>
{#====================================================================================================================#}
<span id="heading_add_sd_to_dg">{{ icon_individual }} Add sequence diagrams to the developer guide</span>
<div id="desc_add_sd_to_dg">

* Add sequence diagrams to enhance your DG wherever they can be useful. Note that diagrams you add in this week will receive feedback while diagrams added later will not.
* {{ icon_tip }} Try to do this before {{ day_first_tutorial }} so that the added sequence diagrams can get peer feedback via the DG peer review that will happen during this week's tutorial.
</div>
{#====================================================================================================================#}
<span id="heading_deliver_penultimate_version">{{ icon_individual }} Deliver {{ version_penultimate }}</span>
<div id="desc_deliver_penultimate_version">

* **Finish implementing the features** you intend to have in the final version.

<div class="indented-level1">

<include src="tp-tasks-fragment.md#level-up-coverage" />
</div>

* **Do a release on GitHub and upload the following files**, ==each as a separate asset==. <span class="text-danger">Do this before the deadline as PE-D testers will start downloading these files ahead of time.</span>:
  1. {{ version_penultimate }} JAR file
  1. UG PDF file
  1. DG PDF file
* ==IMPORTANT: ensure your jar file was generated using Java 17 and can work on all major OS'es using JDK 17.==

{{ embed_topic("tp-constraints.md#Constraint-Java-Version", "Admin " + icon_embedding + " tP Constraints → Constraint-Java-Version", "2", indent="1") }}

* Wrap up the milestone on GitHub.
</div>
{#====================================================================================================================#}

<span id="heading_release_as_a_jar_file">{{ icon_team }} Release {{ version_penultimate }}</span>
<div id="desc_release_as_a_jar_file">

* {{ icon_important_big_red }} **Do a <tooltip content="resulting in a jar file on GitHub that can be downloaded by potential users">proper product release</tooltip>** [as described in the Developer Guide]({{ url_ab3_fork_website }}/DevOps.html#making-a-release). Do the release by the given deadline. <br>
  ==Do a smoke-test to ensure the jar file works== (if the released jar file is broken, it will be omitted from the PE-D).<br>
  * Include the following files in the release (as separate assets):
    1. **JAR** file
    1. **UG** (PDF file) -- uploaded as an 'asset' (similar to the JAR file), not embedded in the release note.
    1. **DG** (PDF file) -- similar to the UG
  * You may choose any suitable filename, but recommended not to have spaces or special characters in the JAR file name.
  * It is optional to write detailed release notes for this version.
* **You can do an _additional_ release before the [PE dry run (PE-D)](tp-ped.html)** if you wish, as long as you do it <span class="text-danger">before 10 am Friday</span>. {% if cs2103 %}That additional release is still considered part of {{ version_penultimate }} and therefore, not subjected to the feature freeze.{% endif %} When doing this additional release, do not delete the previous release %%(reason: it is good to preserve the release history)%% -- testers are expected to test the latest release file anyway. You may use any suitable version number for this JAR file e.g., `{{ version_penultimate }}.1`.<br>
  Waiting till Friday 10am to release the `{{ version_penultimate }}` is strongly discouraged because if you miss that deadline, your team will not be able to benefit from the PE-D at all. It is better to have an earlier release to fall back on in case that happens.
* As before, wrap up the milestone %%(i.e., reschedule/close any remaining issues/PRs and close the milestone).%%

<modal large header="" id="modal:v13-jar-desc">
<include src="tp-tasks-fragment.md#feature-freeze-details"/>
</modal>
</div>
{#====================================================================================================================#}
<span id="heading_wrap_up_penultimate_version">{{ icon_team }} Wrap up {{ version_penultimate }}</span>
<div id="desc_wrap_up_penultimate_version">

* as before %%(i.e., reschedule/close any remaining issues/PRs and close the milestone)%%
</div>
{#====================================================================================================================#}
<span id="heading_review_others_dg">{{ icon_individual }} Review others' DG</span>
<div id="desc_review_others_dg">

* To be done during the tutorial. Please don't do this task before the tutorial as others need time to update their DGs.
* ==Read _all_ instructions== before you start the activity.
* **Find the team choices you have been allocated to review**, as given in the panel below.

{% macro get_review_allocation_for_team(reviewing_team) -%}
{%- set reviewed_team = "" -%}
{% for allocation in team_review_allocation -%}
{% if allocation[0] == reviewing_team %}{% set reviewed_team %}{{ allocation[1] }}{% endset %}{% endif %}
{%- endfor %}{{ reviewed_team }}
{%- endmacro %}

{% macro get_pr_link(team_id) -%}
<a href="https://github.com/nus-{{ course | lower}}-{{ semester }}/{{ tp_repo_name }}/pulls?q=is%3Aopen+is%3Apr+{{ team_id }}+" class="badge bg-primary">PR</a>
{%- endmacro  %}

{% macro get_dg_link(team_id) -%}
<a href="https://{{ semester }}-{{ team_id | lower}}.github.io/{{ tp_repo_name }}/DeveloperGuide.html" class="badge bg-primary">DG</a>
{%- endmacro  %}

{% macro get_links(team_id) -%}
`{{ team_id }}`  {{ get_dg_link(team_id) }} {{ get_pr_link(team_id) }}
{%- endmacro  %}

<div class="indented-level1">

<panel header="Allocation for DG review" >

<d-table sortable searchable>
Your GitHub  | First choice | Second choice | Third choice
-------------|--------------|---------------|-------------
{% if not tp_dg_review_allocation | length %}Allocation ... | ... not ... | .... available ... | ... yet. {% else %}{% for allocation in tp_dg_review_allocation %}`{{ allocation[0] }}` | {{ get_links(allocation[1]) }} | {{ get_links(allocation[2]) }} | {{ get_links(allocation[3]) }}
{% endfor %}{% endif %}
</d-table>
</panel>
</div>

* **Decide which of the given team(s) to review**:
  * Open the <span class="badge bg-primary">DG</span> link of the team allocated as 'First choice'.
  * Confirm that the DG has significant updates, to the diagrams in particular. If it doesn't, you can try the DG of the 'Second choice' team, and failing that, 'Third choice' team.
  * If neither _one_ of the three has enough updates but collectively they have enough updates, you can also review all of them.
  * Failing all above, you can pick any other team(s) to review.
  * Try to give at least 4 comments in total.
  * If the PR already has reviews, you can give your own input of the existing review comments too.

* **Go to the <span class="badge bg-primary">PR</span>** of the team(s) you have chosen to review.
* **Review the `Design` and the `Implementation` sections w.r.t possible DG bugs** (given further down); add your observations as comments.<br>

<div class="indented-level2">

<box>

* In the PR, add _review comments_ (i.e., in the {{ show_as_rounded_tab(':octicon-diff: files changed') }} tab) in the corresponding place of the code.
  * In this case, choose the {{ button('Start a review', button_style="success") }} option rather than {{ button('Add single comment') }} option.
* But ==if the 'files changed' tab is too laggy, you can add a normal comment instead== in the {{ show_as_rounded_tab(':octicon-comment-discussion: conversation') }} tab.<br>
  * In this case, enter each observation as a separate comment %%(reason: our bot will count the number of comments you have given to determine if you qualify for participation points)%%
* As you know, it is better to phrase your comments as question/doubts (e.g., `Is this format correct? Should it be ... instead?`) rather than directives (e.g., `Change this to ...`).<br>
  Where possible, use screenshots from their DG in your comments, preferably with annotations. This is particularly useful when commenting on diagrams. An example given below:<br>
  <pic eager src="images/ReviewCommentExample.png"></pic>
* The understanding you gain from this exercise can indirectly determine how well you do in your own project. Note that your comments will be reviewed by a tutor later.
<!--
* Do not finalize the review at this stage. Just keep adding comments.
* <span class="text-success">**The understanding you gain from this exercise can indirectly determine how well you do in your own project.**</span> ==If you have even the slightest doubt about your observations in this exercise, please discuss it with the tutor== to ensure you have the right understanding of the criteria used.
-->
</box>

<box border-left-color="green">

##### <span class="text-success">DG - Possible Bugs</span>
{{ icon_important_big_red }} Pay attention to these as they are same as the final evaluation criteria of the DG.<br>

{{ embed_topic("tp-grading-bugs-fragment.md#umlDiagramBugs", "Admin " + icon_embedding + " tP Grading → DG Bugs → UML Diagrams → Possible Bugs", "3", indent="1", status="expanded", type="danger") }}
{{ embed_topic("tp-grading-bugs-fragment.md#generalDocBugs", "Admin " + icon_embedding + " tP Grading → General Documentation Bugs", "3", indent="1", status="expanded", type="danger") }}

Also see:
{{ embed_topic("tp-deliverables-dg-fragment.md#dgTips", "Admin " + icon_embedding + " tP: Deliverables → DG → Tips", "3", indent="1", status="peek", type="success") }}

</box>

</div>

<!--
* **Discuss your comments/observations/doubts with the tutor** and other team members to confirm the comments you entered are correct.
* **Update your review comments if necessary**, based on the discussion you just had. After that, you can submit the review.<br>
-->
* **After the tutorial**, if you are unsure about a concern raised by a reviewer, you can post in the [forum]({{ url_forum }}) to seek the opinion of the teaching team.
</div>
{#====================================================================================================================#}
<span id="heading_finish_remaining_tasks">Finish any remaining `{{ version_penultimate }}` tasks</span>
<div id="desc_finish_remaining_tasks">

* Use this extra week to finish any leftover tasks from the previous week.
</div>
{#====================================================================================================================#}
<span id="heading_attend_the_PED">{{ icon_individual }} Take part in the practical exam dry run</span>
<div id="desc_attend_the_PED">

* The practical exam dry run (PE-D) will be held in this {{ lecture_name }}. It is ==graded==. See the panel below for more info.

{{ embed_topic("tp-ped.md#tp-practicalexam-dry-run", "Admin " + icon_embedding + " tP Deliverables → **Practical Exam - Dry Run**", "1", indent="1") }}
</div>
{#====================================================================================================================#}
<span id="heading_alpha_test">{{ icon_individual }} Alpha-test the product</span>
<div id="desc_alpha_test">

Test the product yourself (test each other's features) using the JAR file, report the bugs in the issue tracker, and fix them in due course.
</div>
{#====================================================================================================================#}
<span id="heading_start_fixing_PED_bugs">{{ icon_team }} Fix PE-D bugs</span>
<div id="desc_start_fixing_PED_bugs">
{% if cs2103 %}
1. ****Note the following details of the _feature freeze_ enforced in this iteration****:

<include src="tp-tasks-fragment.md#feature-freeze-details" />
{% endif %}

{{ '2' if cs2103 else '1' }}. ****Triage bugs you received in the PE-D****, by following the procedure given below:

{{ embed_topic("tp-ped-fragment.md#after-ped", "Admin " + icon_embedding + " tP → Deliverables → **After the PE-D**", "3", indent="1") }}

{% if not cs2103 %}
2. ****Do your own testing****. Don't rely on PE-D alone to find bugs. The panel below contains guidelines your peers will use when determining bugs in the final product -- knowing them might be useful in preventing such bugs in your product in the first place.
{{ embed_topic("tp-pe-bug-triaging-guidelines-fragment.md", "Admin " + icon_embedding + " Practical Exam → **Guidelines for determining bugs**", "3", indent="1") }}
{{ embed_topic("tp-grading-bugs-fragment.md#ugBugs", "Admin " + icon_embedding + " tP Grading → **Possible UG Bugs**", "3", indent="1") }}
{{ embed_topic("tp-grading-bugs-fragment.md#dgBugs", "Admin " + icon_embedding + " tP Grading → **Possible DG Bugs**", "3", indent="1") }}{% endif %}

3. ****Fix bugs**** that you deem as important enough to be fixed in {{ version_final }}. Also keep in mind that bug fixing can cause regressions which you'll have to catch and fix.<br>
   **Look for more bugs, and fix them too** (i.e., don't limit to bugs found in the PE-D only).
{% if cs2103 %}
<box>

****High-level workflow for deciding what to do for each PE-D bug****

1. **Is it something you think you'll never fix** even if you were to continue this project in future?<br>
   If yes, you can leave it unfixed and reject it if the same is reported in the PE. Caution: If the PE tester disagrees and the teaching team agrees with the tester's justification, the bug might result in a penalty %%(why say '_might_ result ...'? Because only when the bug density exceeds a certain bar that bugs will be penalised)%%.<br>
   {{ icon_info }} How to decide if a PE bug can be rejected? Refer to <trigger trigger="click" for="modal:pedTriagingWorkflow-peBugTriagingGuidelines">PE Bug Triaging Guidelines</trigger> for details (you may skip the 'General' section).
1. **Else, is it something you may consider fixing in a future version** but was not important enough to have done in {{ version_penultimate }}?<br>
   If yes, you can expect to categorise it as `NotInScope` if the same is reported in the PE (<trigger trigger="click" for="modal:pedTriagingWorkflow-peNotInScope">eligibility criteria</trigger>).
1. **Else, it is something you should have fixed in the current version.**
   * You may fix it in this iteration. If left unfixed, it can be reported as a bug in PE, and _might_ result in a penalty eventually.{text="3.a)"}
   * Alternatively, you can list it under 'Planned Enhancements' in the DG so that it becomes immune to PE bug reporting (caution: there is a limit on how many items you can list as panned enhancements -- see the panel below for more details).<br>
     In addition, you can also update the UG to mitigate its impact on users (e.g., keep users informed of it).{text="3.b)"}

{{ embed_topic("tp-deliverables.md#tp-deliverables-dg", "Admin " + icon_embedding + " tP → Deliverables → Developer Guide", "3", indent="3") }}

{{ show_faq("tpFeatureDesignChoice") }}
</box>

<modal large header="" id="modal:pedTriagingWorkflow-peBugTriagingGuidelines">
<include src="tp-pe-bug-triaging-guidelines-fragment.md"/>
</modal>
<modal large header="" id="modal:pedTriagingWorkflow-peNotInScope">
<include src="tp-pe-bug-triaging-guidelines-fragment.md#how-to-prove-out-of-scope"/>
</modal>
{% endif %}

{% if cs2103 %}4. ****Submit peer evaluations for PE-D testers****: Submit your peer-evaluation of PE-D testers to indicate how well they helped your team.<br>
   Deadline: {{ timing_badge("by " + get_date(date_w13_start, 2), "danger") }}<br>
   The submission is to be done via the TEAMMATES system.<br>
   Only one team member needs to submit on behalf of the team but discuss among team members first.<br>
   Base the evaluation on the quality/usefulness of the bugs reported as well as the quantity.<br>
   Here are the two questions you'll need to answer in the evaluation:

<div class="indented-level2">
<panel type="seamless" header="Q1: Performance of PE-D testers" minimized>

In this context, a good bug report,

* has a descriptive title,
* has enough details,
* severity/type labels chosen are not too far off,
* is written in a non-confrontational tone, and
* points out a potentially problematic behavior (or a good way to improve the product)

Rate each tester on the following scale:

Poor | Below expectations | Meets expectations | Exceeds expectations | Greatly exceeds expectations
----|---|---|---|---
no bug reports from this tester | just a few bug reports, and none are good | 3-5 good bug reports | 6-8 good bug reports | 9 or more good bug reports

</panel>
<panel type="seamless" header="Q2: Rank PE-D testers" minimized>

Rank the PE-D testers based on their performance (give rank 1 to the top performing tester):

`Tester A`: rank __<br>
`Tester B`: rank __<br>
...

</panel><p/>
</div>

<div class="indented-level1">

PE-D bug titles will be prefixed with tester ID e.g., (`[PE-D][Tester A] UG does not load`) to make it easy for you to <tooltip content="using GitHub issue tracker's filters/search box">filter</tooltip> bugs reported by each tester.<br>
</div>


{% endif %}
</div>
{#====================================================================================================================#}
<span id="heading_draft_the_ppp">{{ icon_individual }} {% if cs2103 %}[Optional] {% endif %}Draft the PPP</span>
<div id="desc_draft_the_ppp">
{% if cs2113 %}<include src="tp-tasks-fragment.md#alert-time-sensitive" />{% endif %}

* **Create the first version of your _Project Portfolio Page (PPP)_**{% if cs2103 %} if you opt to submit a PPP -- the panel below to learn when you should opt to submit it.{% endif %}.{% if cs2113 %}==Each member needs to create a PPP== to describe your contribution to the project.{% endif %}

{{ embed_topic("tp-deliverables.md#tp-deliverables-ppp", "Admin " + icon_embedding + " tP → Deliverables → Project Portfolio Page", "2", indent="1", status="peek") }}
{% if cs2113 %}

<box type="tip" seamless>

Convert the PPP to a PDF to see if the page-count is within expectations (the PDF version can be longer than what you would expect by looking at the HTML version).
</box>
{% endif %}
</div>
{#====================================================================================================================#}
<span id="heading_prepare_for_demo">{{ icon_team }} ~~Prepare for the demo rehearsal~~</span>
<div id="desc_prepare_for_demo">

<div class="indented-level2">
Not applicable this semester
</div>

<!--
* You will do a product demo during the tutorial to serve as a rehearsal for the final project demo at {{ version_final }}
  * ==**Follow final demo instructions** (given in the panel below)== as much as possible .
  * **Cover all features**, not just the ones added in the recent iteration.
  * **Make it a 'well prepared' demo** i.e., know in advance exactly what you'll do in the demo.

\{\{ embed_topic("tp-deliverables.md#tp-deliverables-demo", "Admin " + icon_embedding + " tP → Final Demo (extract)", "3", indent="2") }}
-->
</div>
{#====================================================================================================================#}
<span id="heading_prepare_final_deliverables">{{ icon_team }} Prepare final deliverables</span>
<div id="desc_prepare_final_deliverables">

* Final deliverables are due early next week. You are advised to start preparing them well in advance of the submission deadline as any deadline overruns can result in penalties.

</div>
{#====================================================================================================================#}
<span id="heading_double_check_reposense_compatibility">{{ icon_team }} Double-check RepoSense compatibility</span>
<div id="desc_double_check_reposense_compatibility">

* {{ icon_important_big_red }} Once again, double-check to ensure the code attributed to you by RepoSense is correct.

{{ embed_topic("tp-tasks-fragment.md#midV13-repoSenseCompatible", "Admin " + icon_embedding + " tP → mid-" + version_final + " → Making the Code RepoSense-Compatible", "1", indent="1") }}
</div>
{#====================================================================================================================#}
<span id="heading_try_pdf_conversion_early">{{ icon_team }} Try PDF conversions early</span>
<div id="desc_try_pdf_conversion_early">

* Take note of the following project constraint:

{{ embed_topic("tp-constraints.md#Constraint-PDF-Friendly", "Admin " + icon_embedding + " tP Constraints → Constraint-PDF-Friendly", "2", indent="1") }}
{{ embed_topic("tp-constraints.md#Constraint-File-Size", "Admin " + icon_embedding + " tP Constraints → Constraint-File-Size", "2", indent="1") }}

* Take note of the following info about the PDF conversion, appearing in next week's project tasks. Particularly, note the suggestion to try PDF conversions early.

{{ embed_topic("tp-tasks-fragment.md#caution-on-pdf-conversion", "Admin " + icon_embedding + " tP → " + version_final + " → Caution on PDF conversions", "3", indent="1") }}
</div>
{#====================================================================================================================#}
<span id="heading_do_final_tweaks">{{ icon_individual }} Do final polish-ups</span>
<div id="desc_do_final_tweaks">

* Continue with any remaining bug fixing and test/code-quality/documentation improvements.

</div>
{#====================================================================================================================#}
<span id="heading_submit_final_deliverables">{{ icon_individual }}{{ icon_team }} Submit final deliverables</span>
<div id="desc_submit_final_deliverables">

* **Deadline** for all {{ version_final }} submissions is **{{ date_final_submission | date(format_normal)}} {{ time_final_submission }}:00** unless stated otherwise. Note that <span class="text-danger">{{ time_final_submission }}:01 is considered late</span>, as per the Canvas deadline mechanism.
* {{ icon_important_big_red }} **Penalty for late submission** (per file): <br>
  ==-1 mark for missing the deadline (up to 2 hour of delay).==<br>
  -2 for an _extended delay_ (up to 24 hours late).<br>
  Penalty for delays beyond 24 hours is determined on a case by case basis.
  * Even a one-second delay is considered late, irrespective of the reason.
  * For submissions done via Canvas, the submission time is the timestamp shown by Canvas.
  * When determining the late submission penalty, **we take the latest submission** even if the same exact file was submitted earlier. Do not submit the same file multiple times if you want to avoid unnecessary late submission penalties.
  * The whole team is penalized for problems in team submissions %%e.g., a -1 penalty for a team submission will be a -1 penalty for each team member%%.{% if not cs2103 %}<br>
    Only the respective student is penalized for problems in individual submissions.{% endif %}
* **Submit via the Canvas assignment we have set up**.
  {% if has_t %}{{ course}}T students: documents should be submitted to both courses. It's not enough to submit to CS2101 side only.{% endif %}
* {{ icon_important_big_red }} **Follow submission instructions closely**. ==Any non-compliance will be penalized==. e.g. wrong file name/format.<br>
  Canvas might automatically add a file name suffix (e.g., `*-1.pdf`, `*-2.pdf`, ...) if you upload a file multiple times. You can safely ignore that suffix.
* **Do not update the code during the 14 days after the deadline.** Get our permission first if you need to update the code in the repo during that _code-freeze_ period.
  * You can update issues/milestones/PRs even during the _code-freeze_ period.{% if cs2113 or cs2103 %}
  * [{{ course }}T only] You can update the source code of the docs (but not functional/test code) if your CS2101 submission deadline is later than our submission deadline. However, a code-freeze period of 1-2 days is still recommended, so that there is a clear gap between the tP submission and subsequent docs updates.<br>
   On a related note, there is no need to additional stylistic 'beautifications' to the docs before submitting to CS2101 side. The two teaching teams have agreed that there will be no extra credit for such additional  beautifications.{% endif %}
  * You can update the code during the code-freeze period if the change is related to a late submission approved by us.
  * You can continue to evolve your repo after the code-freeze period.

<div class="indented">

++**Submissions:**++
</div>

<div class="indented">
<div id="tip-how-to-convert-to-pdf">

<box id="caution-on-pdf-conversion" type="important" seamless>

**Don't take PDF conversion lightly:**{.text-danger} **To convert the UG/DG{% if cs2113 %}/PPP{% endif %} into PDF format**, go to the generated page in your project's github.io site and use [this technique](https://se-education.org/guides/tutorials/savingPdf.html) to save as a pdf file. ==Using other techniques  or not following the settings suggested in the given technique can result in issues== such as missing background colors, poor quality resolution, unnecessarily large files (the last two can be considered as bugs).

**The PDF versions of the UG/DG{% if cs2113 %}/PPP{% endif %} should be _usable_** by the target readers, even if not as neat/optimized as the Web versions. For example, margins and page breaks need not be optimized, but they should not hinder the reader either. Assume some will occasionally choose the PDF version over the Web version %%e.g, for printing, offline viewing, annotating etc.%%

**PE uses the PDF versions of UG/DG, not the Web version!**{.text-danger} Any problems in those PDF files (e.g., broken links, messed up formatting) can be reported as bugs.

**Ensure hyperlinks in the pdf files work**. ==Broken/non-working hyperlinks in the PDF files will be considered as bugs==. Again, use the conversion technique given above to ensure links in the PDF files work.

**PDF files should**,
  * **be paginated** at a reasonable page size (e.g., A4). %%Reason: single-page PDF files don't work well in some PDF viewers, and not suitable for printing either.%%
  * **allow copying text** so that readers can copy text from them %%(e.g., copy an example command from the UG)%%.

**Try the PDF conversion early**. If you do it at the last minute, you may not have time to fix any problems in the generated PDF files (such problems are more common than you think).
</box>
</div>

<box type="tip" seamless>

**Side benefits for early submissions:**{.text-success} Given that _using buffers to reduce the risk of deadline overruns_ is a learning outcome of this course, we strongly encourage setting an internal submission deadline a few hours earlier than the actual deadline. As an incentive, we plan to perform some checks on early submissions and inform you if we found issues with your submission %%(e.g., incorrect file name/format)%%, thus giving you a chance to fix them before the deadline and avoid a penalty for it.

</box>

<box type="tip" seamless>

**You may use automated tools to improve documentation:**{.text-success} e.g., tools such as Grammarly may be used to improve the writing quality and find grammar errors.

</box>

<box type="info" seamless>

**The icon {{ icon_team }} indicates team submissions.** Only one person need to submit on behalf of the team but we recommend that others help verify the submission is in order.<br>
==We will not entertain requests to limit late penalties of team submissions to one person== even if the delay was one person's fault. That is, the responsibility (and the penalty) for team submissions are to be shared by the whole team rather than burden one person with it.

</box>
</div>

* **Product**:{icon="fas-users"}
  * Do a release on GitHub, tagged appropriately e.g., `{{ version_final }}` or `{{ version_final }}b`.{% if cs2103 %}<br>
    Writing detailed release notes is optional.<br>
    No need to include UG/DG pdf files in the release.{% endif %}
  * Upload the jar file to Canvas.<br>
    File name: `[team ID][ProductName].jar` %%e.g. [{{ example_team_id }}][ContactsPlus].jar%%<br>
    {{ icon_important }} Recommended to <span class="text-danger">avoid spaces and special characters in the product name</span> as it can cause problems when running the JAR file using the command line.<br>
    %%{{ icon_info }} This name requirement is for the JAR file you upload to Canvas only. You may name the JAR file you upload to GitHub in any reasonable way.%%

{{ embed_topic("tp-deliverables.md#tp-deliverables-executable", "Admin " + icon_embedding + " tP → Deliverables → Executable", "3", indent="2") }}


* **Source Code**: Push the code to GitHub and tag with the version number.{icon="fas-users"}

{{ embed_topic("tp-deliverables.md#tp-deliverables-sourcecode", "Admin " + icon_embedding + " tP → Deliverables → Source Code", "3", indent="1") }}

<box type="info" seamless>

Reminder: double-check to ensure the code attributed to you by RepoSense is correct.

{{ embed_topic("tp-tasks-fragment.md#midV13-repoSenseCompatible", "Admin " + icon_embedding + " tP → Making the Code RepoSense-Compatible", "1") }}
</box>

* **User Guide**:{icon="fas-users"}
  * Convert to pdf and upload to Canvas.
  * File name: `[TEAM_ID][ProductName]UG.pdf`  %%e.g., [{{ example_team_id }}][ContactsPlus]UG.pdf%%

{{ embed_topic("tp-deliverables.md#tp-deliverables-ug", "Admin " + icon_embedding + " tP → Deliverables → User Guide", "3", indent="2") }}

* **Developer Guide**:{icon="fas-users"}
  * submission is similar to the UG
  * File name: `[TEAM_ID][ProductName]DG.pdf` %%e.g. [{{ example_team_id }}][ContactsPlus]DG.pdf%%

{{ embed_topic("tp-deliverables.md#tp-deliverables-dg", "Admin " + icon_embedding + " tP → Deliverables → Developer Guide", "3", indent="2") }}


* **{% if cs2103 %}[Optional] {% endif %}Project Portfolio Page (PPP)**:{icon="fas-user"}
  * HTML version: make available on `github.io`{% if cs2113 %}
  * PDF file: submission is similar to the UG<br>
    File name: `[TEAM_ID][Your full Name as Given in Canvas]PPP.pdf` %%e.g., [{{ example_team_id }}][Leow Wai Kit, John]PPP.pdf%%<br>
    {{ icon_info }} Use `-` in place of `/` if your name has it e.g., `Ravi s/o Veegan` → `Ravi s-o Veegan` (reason: Windows does not allow `/` in file names){% else %}
  * See the panel below to learn when you should opt for this submission.{% endif %}

{{ embed_topic("tp-deliverables.md#tp-deliverables-ppp", "Admin " + icon_embedding + " tP → Deliverables → Project Portfolio Page", "3", indent="2", status=("peek" if cs2103 else "minimized")) }}


* **Product Website**: Update website (home page,<span tags="m--cs2103"> `Ui.png`,</span> `AboutUs.md` etc.) on GitHub. Ensure the website is auto-published.{icon="fas-users"}

{{ embed_topic("tp-deliverables.md#tp-deliverables-website", "Admin " + icon_embedding + " tP → Deliverables → Product Website", "3", indent="2") }}
</div>
{#====================================================================================================================#}
<span id="heading_wrap_up_final_milestone">{{ icon_team }} Wrap up the milestone</span>
<div id="desc_wrap_up_final_milestone">

* As usual, wrap up the milestone on GitHub %%i.e., close issues/PRs/milestone (no code changes allowed)%%. Note that the deadline for this is the same for everyone (i.e., does not depend on your tutorial).
</div>
{#====================================================================================================================#}
<span id="heading_demo_the_product">{{ icon_team }}{% if cs2103 %}~~Submit the demo video~~{% else %}Submit the demo video{% endif %}</span>
<div id="desc_demo_the_product">

<div id="demo-instructions" >

<div class="indented-level2">

<pic eager src="{{baseUrl}}/admin/images/v05demo.png" style="width: 250px"><p></pic>

{{ embed_topic("tp-deliverables.md#tp-deliverables-demo", "Admin " + icon_embedding + " tP → Deliverables → Demo", "3", status=("peek" if cs2103 else "minimized")) }}
<p/>
</div>

<!--
* **Venue:** Same as the tutorial venue unless informed otherwise. You'll be using the TV at your regular tutorial table (not the projector) for the demo.
* **Schedule:** Your demo timing is same as your tutorial time in week 13.
  * Teams `1` and `3` will start at 05-minutes mark (e.g., 11.05 am), and teams `2` and `4` start at 30-minutes mark (e.g., 11.30 am).
  * Please ==arrive _before_ time== and remain outside the venue until called in. Late arrival or absence is liable to a penalty.
  * Any delay in starting the presentation is deducted out of your time allotment %%e.g., if you are scheduled to demo at 11.05-11.23 am (i.e., 18 minutes), you'll have to stop at 11.23 am even if you start at 11.10 am.%%
* You should bring your own adapter if the display adapters available in your tutorial venue don't work for you.
-->
</div>
</div>
{#====================================================================================================================#}
<span id="heading_prepare_for_PE">{{ icon_individual }} Prepare for the practical exam</span>
<div id="desc_prepare_for_PE">

{{ embed_topic("tp-pe-fragment.md#pe-overview", "Admin " + icon_embedding + " tP → **PE Overview**", "3", indent="2", type="success") }}

<p/>
{{ embed_topic("tp-pe-fragment.md#pe-preparation", "Admin " + icon_embedding + " tP → **PE Preparation, Restrictions**", "3", indent="2", type="success") }}

* After reading the above 2, we ==strongly recommend you read ahead the info given in the item {{ thumb_small("5" if cs2103 else "6")}} below== as well, to know in advance what will happen during the PE itself.
</div>
{#====================================================================================================================#}
<span id="heading_attend_the_PE">{{ icon_individual }} Take part in the practical exam</span>
<div id="desc_attend_the_PE">

* Ensure you read the instructions on **PE Preparation** (given in item {{ thumb_small("5" if cs2103 else "5")}} above)
* Attend the practical test, to be done during the {{ lecture_name }}.

{{ embed_topic("tp-pe-fragment.md#pe-phases", "Admin " + icon_embedding + " tP → **PE Phases**", "3", indent="1", type="success") }}
</div>
{#====================================================================================================================#}
<span id="heading_attend_the_makeup_PE">{{ icon_individual }} %%[if needed] Attend the re-scheduled practical exam%%</span>
<div id="desc_attend_the_makeup_PE">

* In the very unlikely event that the PE had to be cancelled due to technical issues, attend the makeup PE on this day.
* Note: This is <span class="text-danger">not an alternative option for students who could not attend the PE</span>, as all students need to do the PE at the same time.
</div>
{#====================================================================================================================#}
<span id="heading_do_post_release_tasks">{{ icon_team }}/{{ icon_individual }} Attend to post-release tasks</span>
<div id="desc_do_post_release_tasks">

This is the time to attend to post-release tasks (as `{{ version_final }}` was considered a public release). In the context of our course, this translates to attending to the remaining phases of the PE.

</div>
{#====================================================================================================================#}

{% macro show_tp_page(week_num) %}
{{ show_xp_page(week_num, weekly_tp_tasks['week' + week_num], 'tp-tasks-fragment.md') }}
{% endmacro %}
{#====================================================================================================================#}

{% macro show_admin_tp_page(week_num) %}
{% call show_admin_page("tp-w" + week_num) %}
{{ show_tp_page(week_num) }}
{% endcall %}
{% endmacro %}
