{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<p class="lead" style="color: purple"><md>{{ far_calendar_check }} <include src="project-timeline.md#inception-overview" inline /></md></p>

It is not too early to set an overall direction for your project.

* **Set up a weekly project meeting time/venue with your team members**
  
  We recommend at least one face-to-face project meeting per week. %%The project meeting time can be used to discuss project related things, but also, can be used as a time for team members to work on the project tasks individually (having all members in the same place will facilitate easier collaboration and more peer-learning).%%
  
* **Play around with AB4**
  
  Download the latest released version %%(i.e., the jar file)%% of AB4 from [its upstream repo](https://se-edu.github.io/addressbook-level4/UserGuide.html) and play around with it to familiarize with its current features.

* **Decide project direction, target user profile, and problem addressed**
  
  Use your first project meeting to discuss with your team members and decide your project direction, target user profile, and the value proposition of the product, as described in <trigger trigger="click" for="modal:v10-scope">[Admin {{ icon_embedding }} Project Scope]</trigger> 

<modal large title="Admin {{ icon_embedding }} Project Scope (Extract)" id="modal:v10-scope">
  <include src="project-scope.md#project-direction"/>
</modal>

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w03-inception", show_main_text) }}