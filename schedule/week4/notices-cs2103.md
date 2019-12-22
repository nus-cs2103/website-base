{% from "schedule/index.md" import show_week_pagetop, show_week_summary with context%}
{% from "common/macros.njk" import embed_topic with context%}
{{ show_week_pagetop(4, "notices") }}

<box dismissible>

{{ icon_important_big_red }} We strongly recommend you to **have a team project meeting _before_ the tutorial**. Do the following during the meeting:
* **Finish the tP tasks allocated for the week.** For example, if you don't have a preliminary project idea by this week's tutorial (as per the tP schedule), the tutor will not be able to give feedback on it.
  * Note that the timeliness of tP tasks (i.e., the deadline is the midnight before the tutorial) is graded under the _project management_ component of the tP. 
  * Keep notes of the meeting, and update project documents -- the tutor will ask for those during the tutorial.
* **Help each other finish iP tasks.** Tasks allocated to this week are especially troublesome and some peer help can be very useful.
* **If you can, do the post-lecture quiz together**; while the deadline for the quiz is Thursday midnight, doing it before the tutorial will help you identify unclear areas, which you can then clarify during the tutorial.

</box>
<box dismissible>

{{ icon_tip }} **Dealing with technical problems**: Unlike tutorial questions for which instructors have model solutions, given the complexity of industry tools we use (Gradle, Travis, Git, ...) and the rapid pace they are updated, instructors don't have ready solutions to most technical problems you face in this module. The only realistic way to solve those problems at a large scale is crowd-sourcing i.e., someone else who faced a similar problem might know how to fix it. Here are some tips:
* Don't request to meet the prof/tutor to solve the problem. That can only work if the person is supposed to know how to solve all technical problems, which is not the case.
* Often, technical problems arise due to deviations in how you perform a step or a difference in your environment. **Get your team to meet for a weekly work-together session**. When you do the iP tasks together, it is easy to compare with each other and figure out what deviation is causing the problem. That is, crowd-source your team first.
* Failing the above, **post in the forum**.
  * Give full details of the problem e.g., screenshots, code snippets, stack traces, etc.
  * If the problem is code-related, push the current state of the code to a branch and give the link to the branch. That gives a chance for someone to reproduce the state of your project in their computer.
  * Avoid addressing the question to one person (e.g., the prof), unless really necessary. Doing so will discourage others from answering that question.
  * Remember to thank those you try to help, and close the issue after the issue has been resolved.
* Failing the above, **raise the issue during the tutorial**. Perhaps someone in the other team knows how to fix it.
* Some technical problems can take a longer time to resolve. Therefore, plan ahead and schedule your work much earlier than the deadline.
* Some problems might not get resolved at all; while waiting for a solution, explore alternatives and workarounds.

Further reading:
<div class="indented-level2">

{{ embed_topic("../../admin/appendixD-help.md", "Admin " + icon_embedding + " Appendix D: How to Get Help", "4") }}
</div>

</box>

{{ show_week_summary(4) }}
