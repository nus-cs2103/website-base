{% from "common/macros.njk" import embed_topic, show_as_tab, timing_badge with context %}
{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}

{% if semester == 'AY2627S1' %}
<box type="important" light>

##### **Adjustments due to the long weekend this week...**

* **Week 8 tutorial**: Will be released as a pre-recorded video by Tuesday. #r#Deadline to complete the tutorial tasks: Week 9 Monday.## More info in the [Tutorial page]({{ baseUrl }}/schedule/week8/tutorial.md).
* **Week 8→9 briefing**: Will be done at the usual time, but Zoom only (i.e., no F2F option). As usual, you can join the Zoom meeting live or watch the recording later.
* **Other tP/admin deadlines** will remain as before. If the deadline falls within the holiday period, you are recommended to finish the task early (i.e., before the holiday), but you can also do them _after_ the holidays if the deadline is flexible %%(e.g., weekly tP tasks)%%, or during the holiday period itself (if you prefer to stick with your regular weekly schedule).
</box>
{% else %}

<include src="../../admin/common-notices-fragment.md#try-tutorial-task-before" />
{% endif %}