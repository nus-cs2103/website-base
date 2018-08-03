{% macro show_main_text() %}
<div id="main">

Your tutor will serve as your _project supervisor_ too.

**The supervisor's main job is to observe, facilitate self/peer learning, evaluate, and give feedback.**

Tutorial time is the main avenue for meeting your supervisor. In addition, you can meet the supervisor before/after the tutorial, or any other time, as many times you need, subject to availability in his/her schedule. 

Note that **it is not the supervisor’s job to chase you down and give help**. It is up to you to get as much feedback from the as you need. You are free to request more feedback from the supervisor as necessary. Similarly, it is not the job of the supervisor to lead your project to success. 

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-supervision", show_main_text) }}