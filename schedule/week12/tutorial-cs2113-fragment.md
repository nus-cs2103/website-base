{% from "common/macros.njk" import embed_topic, thumb, show_as_tab, timing_badge with context %}
{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}

<!--
#### {{ thumb(1) }} Demo rehearsal

* Do a project demo dry run (as per project demo instructions given below) for your tutor.

<div class="indented-level2">
{{ embed_topic("../../admin/tp-deliverables.md#tp-deliverables-demo", "Admin " + icon_embedding + " tP → Deliverables → **Demo**", "3") }}
</div>
-->
{% call topic_preamble(reuse=false) %}
**There is no formal tutorial in this week**. Use the tutorial slot for project work.

Attempt this question by yourself. The model answer will be released later.
{% endcall %}
<p/>

#### {{ thumb(1) }} Exercise: test case design

<include src="../../admin/common-tutorials.mbdf#design-test-cases-isvalidday" />