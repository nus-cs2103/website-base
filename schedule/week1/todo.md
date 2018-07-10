{% import "common/macros.njk" as macros with context %}

%%Given below are some _setting up_ tasks you can do as you wait for the module to start:%% 

<span class="activity-desc">Getting ready for the module:<span>

<div class="indented">

<!-- --------------------------------------------------------------------------------------------- -->

<panel no-close >
<span slot="header" class="panel-title">[{{ module }} students only] Forming teams {{ one_star }}</span>

==Delay forming teams== until your place in a tutorial is confirmed. 

<panel type="danger" src="../../admin/teams.md#main" header="%%Admin {{ icon_embedding }}%% Team Forming :star:" />
</panel>

<!-- --------------------------------------------------------------------------------------------- -->

<panel  no-close >
<span slot="header" class="panel-title">[Exchange students only] Signing up for tutorial {{ three_stars }}</span>

Exchange students need to use the ORATUT system to register for the tutorials. You must have received the instructions from UG office on how/when to go about the registration process. If not, please talk to UG office. When we can see your appeal on ORATUT, we can allocate you to the tutorial slot.  
</panel>

<!-- --------------------------------------------------------------------------------------------- -->

<panel no-close > 
<span slot="header" class="panel-title">Create a GitHub Account {{ one_star }}</span>
<include type="danger" src="../../admin/appendixE-gitHub.md#githubAccount"/>
</panel>

<!-- --------------------------------------------------------------------------------------------- -->

<panel no-close > 
<span slot="header" class="panel-title"><md>Submit Pre-Module Survey ==(Compulsory)== :alarm_clock:</md> {{ one_star }}</span>

_Pre-Module Survey_ will be available on IVLE **Week 1 Monday - Friday 2359 :alarm_clock:**. %%We need all of you to submit it because it tells us some important information about you, especially your GitHub ID.%%
</panel>

<!-- --------------------------------------------------------------------------------------------- -->

<panel no-close > 
<span slot="header" class="panel-title">Join the Slack Channel {{ two_stars }}</span>

<panel header="%%**Admin {{ icon_embedding }} Tools → Communication**%%" expanded>
  <include type="danger" src="../../admin/tools.md#communication" />
</panel>

</panel>

<!-- --------------------------------------------------------------------------------------------- -->

<panel no-close >
<span slot="header" class="panel-title">Brush up your Java {{ two_stars }}</span>

This module requires you to write Java code almost every week, staring from the very first week. If your Java skills are shaky, do brush up your Java programming skills. 

In particular, you may want to **have a look at the new Java 8 features** such as `streams`, `lambdas`, `Optionals`, that may not have been covered in previous Java modules.
</panel>

<!-- --------------------------------------------------------------------------------------------- -->

</div> <!-- end indentation -->

<br>

%%Given below are some module _admin info_ to read around this time:%%  

{% import "common/macros.njk" as macros with context %}

{% set admin_sections = [
  {heading: "FAQ: Where is everything?", priority: "1", source: "appendixC-faq.md#admin-faq-whereIsEverything"},
  {heading: "Project: Overview", priority: "1", source: "project-overview.md#main"},
  {heading: "Project: The Product", priority: "1", source: "project-product.md#main"},
  {heading: "Project: Scope", priority: "1", source: "project-scope.md#main"},
  {heading: "Text Books", priority: "2", source: "textBooks.md#main"},
  {heading: "Programming Language", priority: "2", source: "programming-languages.md#main"},
  {heading: "Project: Constraints", priority: "2", source: "project-constraints.md#main"},
  {heading: "Project: Timeline", priority: "2", source: "project-timeline.md#main"},
  {heading: "FAQ: What's different between CS2103 and CS2103T?", priority: "4", source: "appendixC-faq.md#admin-faq-cs2103Vscs2103t"},
  {heading: "FAQ: Why the workload is so high?", priority: "4", source: "appendixC-faq.md#admin-faq-highWorkload"},
  {heading: "FAQ: What are the extra requirements to get an A+?", priority: "4", source: "appendixC-faq.md#admin-faq-aPlus"}]
%}

{{ macros.show_admin_sections_to_read(admin_sections) }}

