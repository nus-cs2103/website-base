{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. Review some peer PRs
1. Add increments: `A-Gradle`,`A-CheckStyle`, `Level-10`, `A-Varargs`
{% endcall %}

<div id="body">


#### {{ thumb(1) }} Review some peer PRs

* **Review two PRs** created by your classmates. PRs can be found [here]({{ module_org }}/duke/pulls).
  * The allocation of which PRs to review will be specified in [this page]({{team_IDs_page}}) (you will be notified when the allocation is ready).
  * To find the target PR, you can use a filter `author:AuthorUsername` e.g., `author:johnDoe`
  * If the student you have been allocated to review has not created a PR by Monday, you can review another PR of your choice.

<div class="indented-level2">

<box type="success">

We expect the PR peer-review to be mutually beneficial to the reviewer and the author. i.e., you receive suggestions on how to improve your code, and get to learn alternative designs by reading others' code.
</box>

<panel header="##### Guidelines for PR reviewers/authors" expanded>

**Guidelines for reviewers**:
* If you are new to GitHub PRs, see [GitHub help on how to review PRs](https://help.github.com/en/articles/about-pull-request-reviews).
* Read the blog post [**10 tips for reviewing code you don’t like**](https://developers.redhat.com/blog/2019/07/08/10-tips-for-reviewing-code-you-dont-like/) - by David Lloyd (a Red Hat developer). In particular, follow the tip about phrasing objections as questions.
* Rather than give one overall comment for the entire PR, add specific comments at relevant places of the code.
* Comment on coding standard violations.
* Feel free to ask for more info from the author, to help you understand the code/design. For example, you can ask why the author chose to write the code in a specific way.
* Feel free to compliment the author when appropriate %%e.g., _hey, I like how clean this bit of code is_ :+1:%%
* You can also suggest alternatives for the author to consider. Feel free to refer back to your own PR if you think a comparison would benefit the author. ==You are very welcome to offer to help the author with the project== (in your PR review, or outside of it) if you think the author needs such help i.e., as an informal mentor. Such mentoring will help both the author and you to become stronger programmers.
* You can use Markdown (specifically, [GitHub-Flavored Markdown](https://guides.github.com/features/mastering-markdown/)) in your comments.
* At the end of the review, we recommend you to choose `Comment` (i.e., not `Approve` or `Request changes`)

**Guidelines for authors**:
* Don't get into arguments with reviewers. If you disagree with the reviewer, you can explain your own view in a non-confrontational way without trying to prove your way is better.
* Thank reviewers for their inputs.

</panel>
<p/>
</div>

* {{ icon_tip }} **Use the iP Code Dashboard to view others' code**: You can now easily view [iP code written by classmates](https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/ip-dashboard), using the `Links → iP Code Dashboard` item in the top navigation menu. Click on the <span class="badge badge-light"><md>%%**</>**%%</md></span>&nbsp;icon corresponding to a student name to see the code written by that person. We encourage you to read others’ code and learn from them. If you adopt solutions from others (also encouraged), please follow our reuse policy. 

<div class="indented-level2">

{{ embed_topic("appendixB-policies.md#policy-reuse", "Admin " + icon_embedding + " **Module Policies → Policy on Reuse**", "1") }}
</div>

<br/>

#### {{ thumb(2) }} Add increments: `A-Gradle`,`A-CheckStyle`, `Level-10`, `A-Varargs`

* **Add the following increments**. As before, do each enhancement in a separate branch and merge to the `master` branch only when ready (if you push incomplete features into the `master` branch, it can confuse others reviewing your PR).
<br>
{{ icon_tip }} If you have completed any of them in previous weeks, just add the corresponding tag (no need to create a branch).

<include src="dukeFragment.md" boilerplate var-header="**`A-Gradle`: Gradle**" var-fragment="extensions.mbdf#A-Gradle" />
<include src="dukeFragment.md" boilerplate var-header="**`A-CheckStyle`: CheckStyle**" var-tag="optional" var-fragment="extensions.mbdf#A-CheckStyle" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-10`: GUI**" var-fragment="text.md#Level-10" />
<include src="dukeFragment.md" boilerplate var-header="**`A-Varargs`: Varargs**" var-tag="if-applicable" var-fragment="extensions.mbdf#A-Varargs" />

<p/>


<br>
</div>
</div>
{% endmacro %}

{{ show_admin_page("ip-w04", show_main_text) }}