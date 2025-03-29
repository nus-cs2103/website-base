{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import embed_topic with context %}


{% call show_admin_page("appendixF-teamworkIssues") %}
<frontmatter>
pageNav: 5
</frontmatter>
<div id="main">

## In general ...

**First, some general principles related to handling teamwork issues:**

* **tP is graded almost entirely based on individual work.**{.text-info} Even when a component is evaluated for the entire team (e.g., product design), each member will be given a mark based on that members' contribution to the component, and the quality of that contribution. This also means **your tP grade is determined almost entirely by your own work**, not the work of your team members. Even if all other team members are low-performing, you should still be able to get a good grade without increasing your workload significantly than otherwise, in theory.{texts="['GP1.', 'GP2.', 'GP3.', 'GP4.', 'GP5.', 'GP6.']" t-class="fw-bold text-info"}
* **Team members are NOT _required_ to do an equal share of work.**{.text-info} Following from GP1, every member can decide how much they want to contribute to the project. This gives students the flexibility to control their tP workload based on their own expectations and motivations.
* **Managing team issues is a learning outcome.**{.text-info} You are recommended to keep the teaching team informed of any teamwork issues you are facing but keep in mind that solving such issues is part of the 'project management' aspect, which is a tP deliverable. So, the teaching team will refrain from direct interventions except in severe cases.
* **Be professional, kind, and civil to the team members, even if they are not meeting your expectations.**{.text-info} A below par performances in the tP does not make someone a 'bad person'. In some cases, the person might be fighting other battles that we are unaware of %%(e.g., mental health issues, family problems, financial problems)%%. The best we can do is to be kind and supportive.<br>
**Be firm and assertive too**, when you need to. Being civil does not mean you let others walk all over you.
* **Willful negative behaviors will be graded harshly.**{.text-info} Willful negative behaviors will be graded harshly. Examples: promising things without intending to deliver, sabotaging others' work, not following what the team agreed on (i.e., going 'rogue'), using offensive language when communicating with team members.

<box>

**A general strategy for adapting the project based on available manpower**

* Ask how much each person is planning to contribute (e.g., how many hours per week can be dedicated to the tP), especially from those who seem to be contributing less. In addition, you can use past conduct to estimate how much you can expect from each person in the future.
* Get some idea about how much value each person is able to produce. Time doesn't always equal value.
* Based on the above, estimate how much 'real' manpower you have and adjust your targets accordingly.
* Stronger programmers in the team can take over the critical parts of the code. Avoid allocating critical tasks to technically-weak or unreliable members.
* Also note that in real software projects, it is not unusual to have less-than-100% members because some people need to divide their time between multiple projects. Treat this as a similar case and adapt accordingly.
</box>

## More specifically ...

**Now, some common problems and guidance on how to deal with them:**

<box type="info" seamless>

**How to inform the teaching team about a teamwork problem?** Some of the guidelines below ask you to 'inform the teaching team' about the problem. In such cases you can write to the course email `{{ course_email }}` to do so.
</box>
<!-- ============================================================================= -->
<div id="team-problems-mia-member">
<panel type="danger" header="##### CP1. MIA team member" expanded>

**Problem:** A team member is MIA from the start, or for an extended period of time.

**Guidance for the team:** It is not your responsibility to ensure a member keeps in touch with the team or/and keeps pace with the project. So, after one or two attempts to get in touch with the MIA member, proceed with the project without the missing member, but keep that member in the loop (e.g., CC all team communications to that member).

Also inform the teaching team about the MIA member.

If the member was previously allocated some future project tasks, redistribute those tasks, and adapt project targets accordingly (i.e., reduce targets because now you are operating with one fewer member).

If the missing member reappears later (by which time you may have redistributed the work to other members), there is no need to disrupt your current plan. Instead, you can suggest (or let the person figure out) ways to contribute without affecting the current project plan. For example, the person can add an additional nice-to-have feature that will not require changes to other features.

----

**Guidance for the member:** If you need to be MIA for a period of time, inform the team when you hope to be back in action. You are welcome to, but not required to, inform the team the reason for the absence (as this may be personal).
</panel></div><!-- ============================================================================= -->
<panel type="danger" header="##### CP2. Low-performing member" expanded>

**Problem:** A member is contributing less than others OR a member is available less than others OR a member is less capable than others.

**Guidance for the team:**

Try not to feel angry or 'wronged'. A low performing member cannot bring others' grade down, or necessitate others to pick up their slack. As mentioned above, your grade is based on your individual work. Just do your best for the project and assume everyone else is doing their best too, although their best may be lower than yours.

Once you identified a low-performing member, you will need to adapt your project targets and plans to match this reality that your available manpower resources is less than you anticipated before (see the 'A general strategy for adapting the project based on available manpower' box above).

----

**Guidance for the member:**

* Be sincere about how much you plan to contribute to the project, you availability, your skill level etc. and keep the team informed if circumstances change.
* ==If you are unable to do a project task (due to lack of time, skill, or other issue), inform the team promptly, rather than keep silent.== It will allow the team to plan around your inability to do the task, rather than waste more time waiting for you to respond/deliver.
* Promise only what you can do, and do what you promised, on time, and up to the expected quality. Sloppy work or late work is worse than no work.

</panel> <!-- ============================================================================= -->
<panel type="danger" header="##### CP3. Low-quality contributions" expanded>

**Problem:** A member is producing low quality work.

**Guidance for the team:** This is not as bad as it appears. Our grading scheme is fine-grained enough to penalize only the person who produced the low-quality work. For example, any bug found in the product design, features, and documentation will be assigned to the person responsible for it (the team needs to decide who is responsible), and only those assigned persons will be penalized. That said, you are encouraged to help fix quality problems of each other, for example, by reviewing each other's PRs.

To aid with assigning accountability for poor quality work, assign tasks clearly. For example, when updating a document, assign clearly who should update which part, so that if a problem was found in a specific part, it is clear who is responsible for it.

The team has a right to refuse to merge poor quality work if the quality is bad enough to jeopardize the overall quality of the product (e.g., possibly affect the behavior of other features).

To reduce the risk of members merging code that can break other features, you can enforce a stricter workflow. For example, you can configure GitHub to prevent PRs being merged unless there is an approving review.

----

**Guidance for the member:**

Appreciate when others point out quality problems of your work. They are helping you save marks.

If the team refused to accept your work, you can still earn marks for that code. You are allowed to submit such 'rejected' code for grading.

</panel> <!-- ============================================================================= -->
<panel type="danger" header="##### CP4. Technically-weak members" expanded>

**Problem:** A team member is not technically strong as the others.

**Guidance for the team:**

* You are encouraged to help this member level up. Mentorship within the team is rewarded and will improve your peer feedback, which are used not only in grading but also in selecting tutors.

----

**Guidance for the member:**

* Be honest about your weak areas. If a task given to you seems beyond your technical skills, let the team know.
* Ask for help and be receptive to help from members.
* Volunteer to do more work related to your strong areas.


</panel> <!-- ============================================================================= -->
<panel type="danger" header="##### CP5. Work delivered late" expanded>

**Problem:** A member delivers work late, or too close to the deadline, causing extra work and extra stress on the rest of the team, not to mention the risk of breaking the product due to last-minute changes.

**Guidance for the team:** You have a right to reject last-minute or late work. If you anticipate a member delivering work late, let that person know the cut-off time for the work to be accepted %%(e.g., at least 24 hours before the submission deadline)%%, and any quality bar it needs to meet %%(e.g., should come with tests)%%.

----

**Guidance for the member:**

If the team refused to accept your work, you can still earn marks for that code. You are allowed to submit such 'rejected' code for grading.

</panel> <!-- ============================================================================= -->
<panel type="danger" header="##### CP6a. No one is taking charge" expanded>

**Problem:** The project is not moving forward because no one is taking charge. Everyone seems to be waiting for someone else to take charge.

**Guidance for the team:** There is no choice but some members (at least one) has to take charge. Those who take charge are likely to score more in the 'Project Management' component.


</panel><!-- ============================================================================= -->
<panel type="danger" header="##### CP6b. Most team members are too slow/quiet" expanded>

**Problem:** All (or most) members miss deadlines, and do not contribute enough to discussions, causing the project to fall behind.

**Guidance for the team:**

* If you feel your team is in this situation, one thing you should do is to communicate this concern to others. You can do that without specifically pointing fingers or causing unpleasantness %%e.g., posting a message in your group message channel "Team, I think our tP is falling behind :-( Can we pick up the pace and be more active (e.g., review PRs faster)?"%%
* Try to evolve the product in an _incremental_ and _iterative_ fashion, and make the implementation tasks as less interdependent as possible. This way, when you get close to an iteration deadline, you can move any incomplete work (e.g., work-in-progress PRs) to the next iteration, and deliver the completed work as the next version of the product.<br>
  Note that ==the team is not obliged to delay the iteration wrap-up until _all_ team members have completed the work they promised== for the iteration. You are free to move any incomplete work into a future iteration.
* You can reduce the risk by dividing the work in a way that more reliable/active members are assigned more important parts of the work while less reliable or slow members are given optional/less-critical parts of the work.
* Setting deadlines, and 'arrowing' specific members, can help too. Examples:
  * When you submit a PR, request reviews from specific people, and also indicate a deadline e.g., `@abc and @def: if you have any comments about this PR, please submit by {date}.`
  * Set deadlines for completing critical tasks (e.g., features that other features depend on) with the understanding that others will need to takeover those features if not done on time.

</panel> <!-- ============================================================================= -->
<panel type="danger" header="##### CP7. Rude member behaviours" expanded>

**Problem:** A team member is behaving rudely, using abusive language, raising voice unnecessarily, etc.

**Guidance for the team:**

* Report such behavior to the teaching team, sooner rather than later.
* Keep evidence e.g., meeting recordings, screenshots of chat messages.

----

**Guidance for the member:** Unprofessional or uncivil behavior will affect your marks, and can lead to disciplinary action.

</panel> <!-- ============================================================================= -->
<panel type="danger" header="##### CP8. A member drops the course halfway into the project" expanded>

**Problem:** A team member drops the course halfway into the project.

**Guidance for the team:** Losing team members (or new members being added) in the middle of a project is not ideal but also not uncommon in a real project. So, consider this as a valuable learning opportunity. That said, if the change causes a significant disruption, we will take that into account when grading.

Suggested steps:

* Adjust project targets accordingly (e.g., cut down targets).
* Redistribute any essential work assigned to that member. New assignees can cut down on less-important work that were previously assigned to them, to make room for this additional work.
* If that member has done some work already, you have two options:
* Some of you take over and continue that work: In this case, you (i.e., the new assignee) should not take credit for work done by the previous assignee (but you can take credit for additional work that you did _after_ taking over). However, someone in the team still needs to take responsibility for any bugs in that work (i.e., you cannot blame bugs on someone who is no longer part of the team -- the current team is responsible for the quality of the _entire_ product).
* Remove the work done by the outgoing member: In that case, the person(s) doing the removal can take credit for the extra effort required for removing the work.

----

**Guidance for the member:** If you anticipate that you might have to drop the course later, keep the team informed about this possibility, and try to avoid taking on must-do tasks. Inform the team immediately when the decision to drop/continue is confirmed.

</panel> <!-- ============================================================================= -->
<panel type="danger" header="##### CP9. The team size is smaller/larger than the team size" expanded>

Refer the following policy:

{{ embed_topic(baseUrl+"/admin/policies-fragment.md#policy-teamSize", "Admin " + icon_embedding + " Polices:  **Policy on grading smaller/larger teams**", "2", indent="0") }}

</panel> <!-- ============================================================================= -->
</div>

{% endcall %}
