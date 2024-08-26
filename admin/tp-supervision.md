{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import embed_topic with context %}

{% call show_admin_page("tp-supervision") %}
<div id="main">

<div tags="m--cs2113 m--cs2103">

Your tutor will serve as your _project supervisor_ too.
</div>
<div tags="m--cs2113 m--cs2103">

**The tutor's main job (in the context of this course project) is to observe, facilitate self/peer learning, and evaluate.** They will not be telling you how to do the project (such guidance is given in other ways e.g., via the course website), or lead/manage the project for you. So, you are expected to self-manage the project. However, if you are facing difficulties, you are welcome/encouraged to keep the tutor informed, so that s/he can take necessary actions.
</div>
<div tags="m--cs2113 m--cs2103" id="making-project-decisions">

**==Tutors are not allowed to contribute to graded components of your project work.==** For example, if you are faced with a design decision in your project, a tutor will not make that decision for you. See the panel below for more details.

{{ embed_topic("appendixB-policies.md#policy-feedbackOnProjectWork", "Admin " + icon_embedding + " Policy on feedback for project work", indent=1, level=2) }}

<box type="tip" seamless>

**How to make project decisions** (given instructors are not going to make them for you)? Here are some tips:

* **Quickly try out the alternatives**. Rather than get into a _analysis-paralysis_ state, quickly prototype the alternatives to figure out which works better.
* **Go with the team consensus/majority.** As most project components are graded by peers, the majority view within the team is a good approximation of how the result will be judged.
* **Go with the simpler alternative** that's good enough for the current iteration. That way, if the decision was the wrong one, you'll find out sooner and the cost will be less. A common rookie pitfall is the temptation to look for an _ideal_ future-proof solution -- usually, there is no such thing. Most alternatives can get the job done, it's just that costs and benefits vary.
* **Look at what other teams are doing.** That will help you detect if you are going in the wrong direction entirely, and also might lead you to more alternatives to consider.
* **Keep an eye on the results**: e.g., Did the design alternative you chose make the code more complex, harder to test, easier to break, harder to modify etc. This will help you decide if you made the right choice.
* **If you realized you picked the wrong alternative,** change if you can. Often, the choice you picked may still be good enough to survive the project. In that case, leave it be, but make a mental note about it (you can even document it in the Developer Guide) for future reference -- that's how you build up _experience_.

</box>
</div>

</div>

{% endcall %}
