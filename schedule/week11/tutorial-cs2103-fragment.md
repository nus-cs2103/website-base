{% from "common/macros.njk" import as_tag, embed_topic, get_date, thumb, show_as_tab, timing_badge with context %}
{% from "common/topics.njk" import panopto with context %}

{% if semester == 'AY2425S1' %}
<box>

#### Week 11 Tutorial Video

{{ icon_graded }} **Graded activity:** The in-video quiz in this video will be used to assess participation for this tutorial.

**Deadline** to watch this tutorial (and answer the in-video quiz): {{ as_tag(get_date(date_w12_start, 0, time='23:59'), tag_style="danger") }}

**Before watching the video:**

1. If you did not attend the last weekly briefing (in which we did the CATcher load testing), watch the first 15 minutes of [the briefing recording]({{ url_canvas_home }}), as the question discussed during that time is highly related to this tutorial.
1. As usual, learn [this week's topics](topics.md) (and ideally, submit the Canvas quiz), so that you have the necessary knowledge for this tutorial.

{{ panopto("0a31323f-762e-466b-aa18-b2170087f030", desc="++Week 11 Tutorial++ (30 minutes)", start_week="11") }}
</box>
{% endif %}

#### {{ thumb(1) }} Exercise: Equivalence partitions, boundary values

* Do the following exercise as directed by the tutor.

<div class="indented">
  <include src="../../book/testCaseDesign/summary/exercises/q-essay-dayParameter.md" />
</div>
<br>

#### {{ thumb(2) }} Exercise: Combining multiple test inputs

* Do the following exercise similar to the previous one.

<div class="indented">
  <include src="../../book/testCaseDesign/combiningTestInputs/mix/q-testCasesForConsumeMethod.md" />
</div>
<br>

#### {{ thumb(3) }} Exercise: Apply design patterns

* Do the following exercise similar to the previous one.

<div class="indented">
  <include src="../../book/designPatterns/more/combiningDesignPatterns/q-essay-getNotified.md" />
</div>
<br>

#### {{ thumb(4) }} Exercise: Patterns in the tP

1. Does AB3 use the _MVC_ pattern?
1. Does AB3 use the _Observer_ pattern?
