{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-Gradle", "Automate project builds using Gradle", "primary") }}

Use Gradle to automate some of the build tasks of the project, as follows:

* Gradle support is provided as a separate branch named `add-gradle-support` in the Duke repo. ==Merge that branch to your `master` branch==.{text="Step 1."}

<mermaid>
{{ "%%{init: { 'theme': 'default', 'gitGraph': {'mainBranchName': 'master'}} }%%" }}
gitGraph
commit id: "m1"
branch add-gradle-support
checkout add-gradle-support
commit id: "b1"
commit id: "b2"
checkout master
commit id: "m2"
commit id: "m3"
merge add-gradle-support id: "Merge branch ..."
</mermaid>

* Go to the [_Gradle tutorial_ @SE-EDU](https://se-education.org/guides/tutorials/gradle.html).{text="Step 2."}
  * If you are new to Gradle, read the _Basics_ section to get an overview of Gradle.{texts="['2a.','2b.', '2c.']"}
  * Next, follow [==_scenario 2_== of the _Adding Gradle to the project_ section](https://se-education.org/guides/tutorials/gradle.html#:~:text=click%20it.-,Scenario%202,-%3A%20You%20are), to add Gradle to your project.
  * Read the rest of the tutorial to find how to use Gradle to build, run, test, etc.

<p/>

Requirements for this increment:

* **Minimal**: Set up Gradle so that you can build and run Duke using Gradle. After doing this, you can move to the next increment.
* **Recommended** (to be done at a later time): Be able to run JUnit tests using Gradle (this can only be done after you've reached the `A-JUnit` increment).
* **Stretch goal** (to be done at a later time): Use Gradle to automate more things in your project, as you progress through the project.


{% call show_ai_guidance("A-Gradle") %}
If you are new to merging branches, you can get AI's help to guide you along. Example:

<tabs>
  <tab header="Sample prompt (less AI)">
{% call mdblock() %}
Gradle support provided as a separate branch named `add-gradle-support`.
I have fetched that branch and merged it to my `master` branch. Check if I did it correctly.
{% endcall %}
  </tab>
  <tab header="Sample prompt (more AI)">
{% call mdblock() %}
Gradle support is supposed to be provided as a separate branch named `add-gradle-support`.
1. Check if that branch is in my fork.
2. I have not fetched or pulled that branch to my local repo. I need to merge that branch to my `master` branch. What are the steps? Explain each step.
{% endcall %}
</tab>
  <tab header="Sample prompt (even more AI)">
{% call mdblock() %}
Gradle support is provided as a separate branch named `add-gradle-support` in my fork.
I need to merge that branch to my `master` branch.
Go ahead and do it. Also explain the steps you took.
{% endcall %}
</tab>
</tabs>

After mering the branch and setting it up in the IDE:

{% call mdblock() %}
How do I check if Gradle is working?
{% endcall %}

{% call mdblock() %}
When I run my app in IDE, I face this error (see the screenshots I've attached). This happened after I added Gradle support to the project. How do I fix it?
{% endcall %}

{% endcall %}
