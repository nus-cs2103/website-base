{% from "common/macros.njk" import embed_topic, get_date, show_as_tab, timing_badge with context %}

<include src="../../admin/common-notices.mbdf#tutorial-start" />

<box type="info" header="**In-video quizzes can earn you bonus participation points!**" dismissible >

<include src="../../admin/participation.md#in-video-quiz-info" />

Answering in-video quizzes can earn you [bonus participation points](../../admin/participation.md).
</box>

{% if S == "2" %}
<box type="important" dismissible>

**Heads up: PE rescheduled!**{.text-danger}

Due to the Good Friday holiday, the [team project practical exam](../../admin/tp-pe.html) that we usually do on the last lecture day ({{ get_date(date_w13_start, 7, format=format_normal, time="1400-1600") }}) has been ==rescheduled on the following day (**{{ get_date(date_w13_start, 8, format=format_normal, time="1400-1600") }}**)==. Please keep your calendar clear on that slot.
</box>
{% endif %}
