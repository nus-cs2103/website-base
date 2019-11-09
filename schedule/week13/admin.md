{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import show_admin_sections_to_read, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(13, "admin") }}

{% call show_admin_summary() %}

1. Submit peer evaluations 1 & 2 on TEAMMATES {{ timing_badge("by Thursday 2359") }}
{% endcall %}

<div id="additional">

#### {{ thumb(1) }} Submit peer evaluations 1 & 2 on TEAMMATES {{ timing_badge("by Thursday 2359", "secondary") }}

* There are ==two peer evaluations to submit==
* ==There will be bonus marks for <tooltip content="i.e., those who are close to the overall consensus">good</tooltip> peer evaluations==.
* For reference, here are the detailed criteria to be used:
<div class="indented-level2">

##### Peer Evaluation - (Part 1)

<panel type="info" header="Admin → tP → Grading → **UG**" expanded>

<include src="../../admin/project-grading.md#projectGrading-userGuide-instructions" />
</panel>

<panel type="info" header="Admin → tP → Grading → **DG**" expanded>

<include src="../../admin/project-grading.md#projectGrading-devGuide-instructions" />
</panel>

<panel type="info" header="Admin → tP → Grading → **Feature**" expanded>

<include src="../../admin/project-grading.md#projectGrading-featureQuality-instructions" />
</panel>

<panel type="primary" header="Admin → tP → Grading → **Effort**" expanded>

<include src="../../admin/project-grading.md#projectGrading-effort-instructions" />
</panel>
<p/>

##### Peer Evaluation - (Part 2)

<panel type="warning" header="Admin → Peer Evaluations → **Conduct & Competency**" expanded>

<include src="../../admin/peerEvaluations.md#peerEvaluation-criteria" />
</panel>

</div>
</div>
