{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-supervision") %}
<div id="main">

<div tags="m--cs2113 m--cs2103">

Your tutor will serve as your _project supervisor_ too.
</div>
<div tags="m--tic4001">

One of the lecturers will be assigned as your team's tutor (aka project supervisor).
</div>

**The supervisor's main job is to observe, facilitate self/peer learning, evaluate, and give feedback.**

{{ "Lecture" if module == "TIC4001" else "Tutorial" }} time is the main avenue for meeting your supervisor. In addition, you can meet the supervisor at other times, as many times you need, subject to availability in his/her schedule.

Note that **it is not the supervisor’s job to chase you down and give help**. It is up to you to get as much feedback from the as you need. You are free to request more feedback from the supervisor as necessary. Similarly, it is not the job of the supervisor to lead your project to success. 

</div>

{% endcall %}
