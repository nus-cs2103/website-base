{% macro show_main_text() %}
<div id="main">

You will start the tP in week 3, while the iP is ongoing. You will deliver the tP iteratively, planning the project as if you are aiming for a `v2.0` but delivering only the iterations `v1.0` to `v1.4` during the module. The `v1.4` is the version that will be subjected to final project grading.

Given below is the high-level timeline of the project.

Week  | Stage     | Activities
------|-----------|-----------
**3** |kick-off | <span id="kickoff-overview">Set up a project meeting time. Familiarize with AB3</span>
**4** |inception| <span id="inception-overview">Start weekly project meetings. Start a collaborative doc to take project notes. Decide on a overall project direction %%(user profile, problem addressed).%%</span>
**5** |v1.0     | <span id="v10-overview">Start documenting requirements %%(user stories, use cases, NFRs).%%</span>
**6** |mid-v1.1 | <span id="mid-v11-overview">Set up project repo. Get familiar with the code base. Draft the UG.</span>
**7** |v1.1     | <span id="v11-overview">Transfer documentation to the repo %%(AboutUs; ContactUs; README; UG; DG: user stories, glossary, NFRs, use cases)%%, draft a rough project plan.</span>
**8** |mid-v1.2 | <span id="mid-v12-overview">Start proper milestone management. Start adding a minimal version of the new feature.</span>
**9** |v1.2     | <span id="v12-overview">Deliver/demo a minimal version of the new features.</span>
**10**|mid-v1.3 | <span id="mid-v13-overview">Start on the full version of the new features. Update DG with design/implementation details. Make code RepoSense-compatible. Try doing a proper release.</span>
**11**|v1.3     | <span id="v13-overview">Deliver the meat of the feature, release as a jar file, release updated user guide, peer-test released products, verify code authorship.</span>
**12**|mid-v1.4 | <span id="mid-v14-overview">Tweak as per peer-testing results, draft Project Portfolio Page, practice product demo.</span>
**13**|v1.4     | <span id="v14-overview">Final tweaks to docs/product, release product, demo product, evaluate peer projects.</span>

More details of each stage is provided elsewhere is this website.

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-timeline", show_main_text) }}
