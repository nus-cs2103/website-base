{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. {{ icon_individual }} Start on the full version of the new features
1. {{ icon_individual }} Update DG with design details {{ timing_badge("IMPORTANT!") }}
1. {{ icon_team }}  Do a release
1. {{ icon_individual }} Make code RepoSense-compatible
{% endcall %}

<div id="body">

#### {{ thumb(1) }} {{ icon_individual }} Start on the full version of the new features

* Start on implementing the full version of your new feature(s). Aim to finish it in v1.3 (v1.4 can serve as a buffer). As before, you can divide the work into even smaller increments %%e.g., aim to deliver a v1.2.1 at the end of this week%%.
* Continue to do deliberate project management using GitHub issue tracker, milestones, labels, etc. as you did in v1.2.
* {{ icon_tip }} We recommend that **each PR also updates the relevant parts of documents and tests**. That way, your documentation/testing work will not pile up towards the end.
* {{ icon_tip }} There is [a way to get GitHub to auto-close the relevant issue when a PR is merged](https://help.github.com/articles/closing-issues-using-keywords/) ([example](https://github.com/se-edu/addressbook-level4/pull/888)).

#### {{ thumb(2) }} {{ icon_individual }} Update DG with design details {{ timing_badge("IMPORTANT!", "secondary") }}

<div class="indented">
<box>

{{ icon_important_big_red }} Do a sincere job on this task because this is your only chance to get tutor feedback on the DG before it is graded at v1.4.
</box>
</div>

* **Update the Developer Guide** as follows:
  * ==Each member should describe the implementation of at least one enhancement she has added== (or planning to add). <br>
    Expected length: 1+ page per person
  * The description can contain things such as,
    * How the feature is implemented.
    * Why it is implemented that way.
    * Alternatives considered.
  * The stated objective is to explain the implementation to a future developer, but a hidden objective is to show evidence that you can document deeply-technical content using prose, examples, diagrams, code snippets, etc. appropriately. To that end, you may also describe features that you plan to implement in the future, even beyond v1.4 (hypothetically).
  * For an example, see [the description of the undo/redo feature implementation in the AddressBook-Level3 developer guide](https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/addressbook-level4/DeveloperGuide.html#undo-redo-feature).

#### {{ thumb(3) }} {{ icon_team }} Do a release

* {{ icon_important_big_red }} **Do a <tooltip content="resulting in a jar file on GitHub that can be downloaded by potential users">proper product release</tooltip>** [as described in the Developer Guide](https://nus-{{ module | lower }}-{{ semester }}.github.io/addressbook-level3/DeveloperGuide.html#making-a-release). You can name it something like `v1.2.1`. ==Ensure that the jar file works as expected== by doing some manual testing. %%Reason: You are _required_ to do a proper product release for v1.3. Doing a trial at this point will help you iron out any problems in advance. It may take additional effort to get the jar working especially if you use third party libraries or additional assets such as images.%%

#### {{ thumb(4) }} {{ icon_individual }} Make code RepoSense-compatible


* **Ensure your code is <tooltip content="i.e., RepoSense can detect your code as yours">RepoSense-compatible</tooltip>**, as explained below:

<div class="indented-level2">
{{ embed_topic("tools.md#reposense", "Admin " + icon_embedding + " Tools → RepoSense", "midv13_repoSenseCompatibility", "1") }}
</div>


</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w10-mid-v13", show_main_text) }}