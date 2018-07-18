{% import "common/macros.njk" as macros with context %}

%%Given below are some preparatory tasks you can do as you wait for the module to start:%% 

<span class="activity-desc">Getting ready for the module:<span>

<div class="indented">

<!-- --------------------------------------------------------------------------------------------- -->

<panel no-close >
<span slot="header" class="card-title">Learn how to form project teams {{ one_star }}</span>

==Delay forming teams== until your place in a tutorial is confirmed. 

<panel type="danger" src="../../admin/project-teams.md#main" header="Admin {{ icon_embedding }} Team Forming :star:" expanded />
</panel>

<!-- --------------------------------------------------------------------------------------------- -->

<panel  no-close >
<span slot="header" class="card-title">[Exchange students only] Know how to sign up for tutorials {{ three_stars }}</span>

Exchange students need to use the ORATUT system to register for the tutorials. You must have received the instructions from UG office on how/when to go about the registration process. If not, please talk to UG office. When we can see your appeal on ORATUT, we can allocate you to the tutorial slot.  
</panel>

<!-- --------------------------------------------------------------------------------------------- -->

<panel no-close > 
<span slot="header" class="card-title">Create a GitHub account {{ one_star }}</span>
<panel header="Admin {{ icon_embedding }} Appendix E (Using GitHub) → Creating a GitHub account" expanded >
  <include type="danger" src="../../admin/appendixE-gitHub.md#githubAccount"/>
</panel>
</panel>

<!-- --------------------------------------------------------------------------------------------- -->

<panel no-close > 
<span slot="header" class="card-title"><md>Submit the pre-module survey ==(Compulsory)== :alarm_clock:</md> {{ one_star }}</span>

_Pre-Module Survey_ will be available on IVLE **Week 1 Monday - Friday 2359 :alarm_clock:**. %%We need all of you to submit it because it tells us some important information about you, especially your GitHub username.%%
</panel>

<!-- --------------------------------------------------------------------------------------------- -->

<panel no-close > 
<span slot="header" class="card-title">Join the Slack channel {{ two_stars }}</span>

<panel header="%%**Admin {{ icon_embedding }} Tools → Communication**%%" expanded>
  <include type="danger" src="../../admin/tools.md#communication" />
</panel>

</panel>

<!-- --------------------------------------------------------------------------------------------- -->

<panel no-close >
<span slot="header" class="card-title">Prepare to meet module expectations {{ two_stars }}</span>

<panel header="%%**Admin {{ icon_embedding }} Module Expectations**%%" expanded>
  <include type="danger" src="../../admin/moduleExpectations.md#main" />
</panel>
 
</panel>

<!-- --------------------------------------------------------------------------------------------- -->

</div> <!-- end indentation -->

<br>

%%Given below are some module _admin info_ to read around this time:%%  

{% import "common/macros.njk" as macros with context %}

{% set admin_sections = [
  {heading: "FAQ: Where is everything?", priority: "1", source: "appendixC-faq.md#admin-faq-whereIsEverything"},
  {heading: "Programming Language", priority: "2", source: "programming-languages.md#main"},
  {heading: "Text Books", priority: "2", source: "textbooks.md#main"},
  {heading: "FAQ: What's different between CS2103 and CS2103T?", priority: "4", source: "appendixC-faq.md#admin-faq-cs2103Vscs2103t"},
  {heading: "FAQ: Why the workload is so high?", priority: "4", source: "appendixC-faq.md#admin-faq-highWorkload"},
  {heading: "FAQ: What are the extra requirements to get an A+?", priority: "4", source: "appendixC-faq.md#admin-faq-aPlus"}]
%}

{{ macros.show_admin_sections_to_read(admin_sections) }}

