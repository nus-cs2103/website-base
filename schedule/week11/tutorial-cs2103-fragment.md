{% from "common/macros.njk" import embed_topic, thumb, show_as_tab, timing_badge with context %}

#### {{ thumb(0, thumb_style="secondary") }} %%Demo {{ version_penultimate }}%%

<div class="indented-level2">

%%The tutor to confirm the following has been done.%%

{{ embed_topic("../../admin/tp-tasks.mbdf#desc_demo_penultimate_version", "Admin " + icon_embedding + " tP v1.3: Demo", "3") }}
</div>
<p/>

<div class="indented-level2">
<box type="success" border-left-color="green" icon="">

You may release a newer version to be used for the PE dry run, but make sure it is released <span class="text-danger">by {{ day_lecture }} 10am</span>.
</box>
</div>


<!--
#### {{ thumb(2) }} Exercise: test case design
* Divide into two sub-teams and do the following exercises on the white board. Both sub-teams should do both exercises.
<div class="indented-level2">
  <include src="../../book/testCaseDesign/summary/exercises/q-essay-dayParameter.md" />
  <include src="../../book/testCaseDesign/combiningTestInputs/mix/q-testCasesForConsumeMethod.md" />
</div>
-->
#### {{ thumb(1) }} Exercise: Equivalence partitions, boundary values

* Do the following exercise as directed by the tutor.

<div class="indented-level2">
  <include src="../../book/testCaseDesign/summary/exercises/q-essay-dayParameter.md" />
</div>
<br>

#### {{ thumb(2) }} Exercise: Combining multiple test inputs

* Do the following exercise similar to the previous one.

<div class="indented-level2">
  <include src="../../book/testCaseDesign/combiningTestInputs/mix/q-testCasesForConsumeMethod.md" />
</div>
<br>

#### {{ thumb(3) }} Exercise: Apply design pattern

* Do the following exercise similar to the previous one.

<div class="indented-level2">
  <include src="../../book/designPatterns/more/combiningDesignPatterns/q-essay-getNotified.md" />
</div>
<br>

#### {{ thumb(4) }} Exercise: Patterns in the tP

1. Does AB3 use the _MVC_ pattern?
1. Does AB3 use the _Observer_ pattern?
