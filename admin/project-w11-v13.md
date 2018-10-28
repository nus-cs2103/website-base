{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<p class="lead" style="color: purple"><md>{{ far_calendar_check }} <include src="project-timeline.md#v13-overview" inline /></md></p>

**v1.3 Summary of Milestone**

Milestone | Minimum acceptable performance to consider as 'reached'
--------- | -------------------------------------------------------
{{ icon_individual }} Contributed code to v1.3 | code merged
{{ icon_individual }} Code is RepoSense-compatible | as stated in mid-v1.3
{{ icon_team }} v1.3 jar file released on GitHub | as stated
{{ icon_team }} v1.3 milestone properly wrapped up on GitHub | as stated
{{ icon_team }} Documentation updated to match v1.3 | at least the User Guide and the `README.adoc` is updated

### v1.3 Project Management

Ensure your code is RepoSense-compatible, <trigger trigger="click" for="modal:v13-reposense">as explained in mid-v1.3</trigger>.

<modal large title="Admin {{ icon_embedding }} Project → v1.3 (extract)" id="modal:v13-reposense">
  <include src="reposenseCompatibility.md" />
</modal>

### v1.3 Product

* As before, move the product towards v2.0.

* {{ icon_important_big_red }} **Do a <tooltip content="resulting in a jar file on GitHub that can be downloaded by potential users">proper product release</tooltip>** [as described in the Developer Guide](https://nus-{{ module | lower }}-{{ semester }}.github.io/addressbook-level4/DeveloperGuide.html#making-a-release). Do some manual tests to ensure the jar file works.

### v1.3 Documentation

<tip-box>

{{ icon_important_big_red }} v1.3 user guide should be updated to match the current version of the product. %%&nbsp;Reason: v1.3 will be subjected to a trial _acceptance testing_ session%%

</tip-box>

* **README page**: Update to look like a real product (rather than a project for learning SE) if you haven't done so already. In particular, ==update the `Ui.png` to match the current product==.
  
* **User Guide**: ==This document will be used by acceptance testers==. Update to match the current version. In particular,
  * Clearly indicate which features are not implemented yet %%e.g. tag those features with a `Coming in v2.0`%%.
  * For those features already implemented, ensure their descriptions match the exact behavior of the product %%e.g. replace mockups with actual screenshots%%
 
* **Developer Guide**: As before, update if necessary.
  
* **AboutUs page**: Update to reflect current state of roles and responsibilities.  

**Submission**: Must be included in the version tagged `v1.3`.


### v1.3 Demo

* Do a quick demo of the main features ==using the jar file==. Objective: demonstrate that the jar file works.


### v1.3 Testing (_aka_ Practical Exam Dry Run)

=={{ icon_important_big_red }} See info in the panel below:==
<br>
{{ embed_topic("project-deliverables.md#project-deliverables-practicalexam-dry-run", "Admin " + icon_embedding + " Project Deliverables → **Practical Exam - Dry Run**", "v13-peDryRun", "1") }}

</div>
</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w11-v13", show_main_text) }}