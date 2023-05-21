{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-supervision") %}
<div id="main">

<div tags="m--cs2113 m--cs2103">

Your tutor will serve as your _project supervisor_ too.
</div>
<div tags="m--tic4001 m--tic4002">

One of the lecturers will be assigned as your team's tutor (aka project supervisor).
</div>
<div tags="m--cs2113 m--cs2103">

**The supervisor's main job (in the context of this course) is to observe, facilitate self/peer learning, evaluate, and give feedback.**

{{ Session_name }} time is the main avenue for meeting your supervisor. In addition, you can meet the supervisor at other times, as many times you need, subject to availability in his/her schedule.
</div>
<div tags="m--cs2113 m--cs2103 m--tic4002" id="making-project-decisions">

**=={% if tic4002 %}It is not appropriate for instructors{%else%}Tutors are not allowed{% endif %} to contribute to graded components of your project work.==** For example, if you are faced with a design decision in your project, a tutor will not make that decision for you.<br>
 %%Reason: to ensure fairness across teams, and to ensure the work you submit for grading is entirely your own%%

Following from the above, **don't expect instructors to answer questions that are specific to graded deliverables** (e.g., ask which design alternative is better -- that's a decision you need to make yourself). <span tags="m--cs2103 m--cs2113">At best, the instructor can channel the question to the professor.</span> However, ==you can still raise such questions in the course forum== where the professor can answer the question in a general way that's not unfair to other teams (and other teams can benefit from the answer as well).

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
