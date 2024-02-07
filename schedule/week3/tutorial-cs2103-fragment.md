{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

<box>

As this is the first tutorial, given below are general details about our tutorials, in case you did not read that page before:

{{ embed_topic(baseUrl+"/admin/tutorials.md#main", "Admin " + icon_embedding + " Tutorials", "2", indent=0) }}
</box>
<p/>

#### {{ thumb(0) }} **[{{ course }} students only] Form teams**

<include src="../../admin/common-tutorials-fragment.md#form-teams" />


#### {{ thumb(1) }} **Introduce yourselves**

<include src="../../admin/common-tutorials-fragment.md#introduce-yourselves" />


#### {{ thumb(2) }} **Find coding standard violations**

<include src="../../admin/common-tutorials-fragment.md#exercise-coding-standard-violations" />


#### {{ thumb(3) }} **Decide a weekly project meeting time**

<include src="../../admin/common-tutorials-fragment.md#decide-meeting-time" />


#### {{ thumb(4) }} **Help team members troubleshoot iP problems**

<include src="../../admin/common-tutorials-fragment.md#help-troubleshoot-ip" />

