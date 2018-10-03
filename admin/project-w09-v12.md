{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<p class="lead" style="color: purple"><md>{{ far_calendar_check }} <include src="project-timeline.md#v12-overview" inline /></md></p>

**v1.2 Summary of Milestone**

Milestone | Minimum acceptable performance to consider as 'reached'
--------- | -------------------------------------------------------
{{ icon_individual }} Contributed code to the product as described in mid-v1.2 progress guide | some code merged
{{ icon_individual }} Described implementation details in the Developer Guide | some text and some diagrams added to the developer guide (at least in a PR), comprising at least one page worth of content
{{ icon_team }} v1.2 managed using GitHub features (issue tracker, milestones, etc.) | A new version git tagged `v1.2` is in your repo.<br> Milestone v1.2 _wrapped up_ as explained in <trigger trigger="click" for="modal:v12-projectTracking">[Admin {{ icon_embedding }} Appendix E: GitHub: Project Schedule Tracking]</trigger>.

<modal large title="Admin {{ icon_embedding }} Appendix E: GitHub: Project Schedule Tracking" id="modal:v12-projectTracking">
  <include src="appendixE-gitHub.md#project-schedule-tracking"/>
</modal>

  
### v1.2 Project Management

* {{ icon_team }} Manage, and close, the v1.2 milestone using GitHub.

### v1.2 Product

* {{ icon_individual }} Merge some code into the `master` branch of your team repo.

### v1.2 Documentation

* **User Guide**: Update as necessary.
  * If a feature has been released in this version, remove the `Coming in v2.0` annotation from that feature. Also replace UI mock-ups with actual screenshots.
  * If a feature design has changed, update the descriptions accordingly.

* **Developer Guide**:
  * ==Each member should describe the implementation of at least one enhancement she has added== (or planning to add). <br>
    Expected length: 1+ page per person
  * The description can contain things such as,
    * How the feature is implemented.
    * Why it is implemented that way.
    * Alternatives considered.
  * The stated objective is to explain the implementation to a future developer, but a hidden objective is to show evidence that you can document deeply-technical content using prose, examples, diagrams, code snippets, etc. appropriately. To that end, you may also describe features that you plan to implement in the future, even beyond v1.4 (hypothetically).
  * For an example, see [the description of the undo/redo feature implementation in the AddressBook-Level4 developer guide](https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/addressbook-level4/DeveloperGuide.html#undo-redo-feature).
  

### v1.2 Demo

Do an informal demo of the new feature during the tutorial. ==Each team member should demo their own work, using commit tagged as `v1.2` in the `master` branch== %%&nbsp;i.e. only features included in the current release should be demoed%%.

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w09-v12", show_main_text) }}