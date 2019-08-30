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

* **Review two PRs** created by your classmates. PRs can be found [here]({{ module_org }}/duke/pulls). You will be notified separately whose PRs to review. To find the target PR, you can use a filter `author:AuthorUsername` e.g., `author:johnDoe`

<div class="indented">

<box type="success">

We expect the PR peer-review to be mutually beneficial to the reviewer and the author. i.e., you receive suggestions on how to improve your code, and get to learn alternative designs by reading others' code.
</box>

{{ icon_tip }} **Tips for reviewers**:
* Read the blog post [**10 tips for reviewing code you don’t like**](https://developers.redhat.com/blog/2019/07/08/10-tips-for-reviewing-code-you-dont-like/) - by David Lloyd (a Red Had developer). In particular, follow the tip about phrasing objections as questions.
* Comment on coding standard violations.
* Feel free to ask for more info from the author, to help you understand the code/design. For example, you can ask why the author chose to write the code in a specific way.
* Feel free to compliment the author when appropriate %%e.g., _hey, I like how clean this bit of code is_ :+1:%%
* You can also suggest alternatives for the author to consider.
* You can use Markdown (more specifically, [GFMD](https://guides.github.com/features/mastering-markdown/)) in your comments.

{{ icon_tip }} **Tips for authors**:
* Don't get into arguments with reviewers.
* Thank reviewers for their inputs.
</div>

<br/>

#### {{ thumb(2) }} Add increments: `A-Gradle`,`A-CheckStyle`, `Level-10`, `A-Varargs`

* **Add the following increments**. As before, do each enhancement in a separate branch and merge to the `master` branch only when ready (if you push incomplete features into the `master` branch, it can confuse others reviewing your PR).
<br>
{{ icon_tip }} If you have completed any of them in previous weeks, just add the corresponding tag (no need to create a branch).

<include src="dukeFragment.md" boilerplate var-header="**`A-Gradle`: Gradle**" var-fragment="extensions.mbdf#A-Gradle" />
<include src="dukeFragment.md" boilerplate var-header="**`A-CheckStyle`: CheckStyle**" var-tag="optional" var-fragment="extensions.mbdf#A-CheckStyle" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-10`: GUI**" var-fragment="text.md#level10" />
<include src="dukeFragment.md" boilerplate var-header="**`A-Varargs`: Varargs**" var-tag="if-applicable" var-fragment="extensions.mbdf#A-Varargs" />

<p/>


<br>
</div>
</div>
{% endmacro %}

{{ show_admin_page("ip-w04", show_main_text) }}