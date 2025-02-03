{% from "common/macros.njk" import embed_topic, get_date, show_as_tab, timing_badge with context %}
{% from "common/topics.njk" import  panopto with context %}

<box type="important" seamless>

**Umm... you've finished [Week 1 tasks](../week1/index.html) already, right?** If not, please finish them first before starting on this week's tasks.

</box>

<box type="tip" seamless>

**Noticed any issues (==even minor typos==) in the course website (or in resources in [se-edu/guides](https://se-education.org/guides/))?** Have suggestions for improvements, or noticed a part that wasn't clear?<br>
**You can earn [bonus participation points](../../admin/participation.md)** by reporting them in the [forum]({{ url_forum }}).<br>
</box>

<panel type="info" header="##### ==[MUST-WATCH]== Briefing Videos for Week 2" peek >

<include src="../../admin/courseBriefings.md#course-briefing-w2" />
</panel>
<p/>
<box type="info">

****Week 2->3 Briefing**** (Week 2 Recap + Week 3 Preview) will be done in hybrid mode -- you can attend it F2F %%(@{{ lecture_venue }} {{ get_date(date_w2_start, 4, format=format_normal, time="from 4pm") }})%%, join via Zoom, watch the recording later, or skip it altogether).<br>

==**iP Help Session**== %%({{ get_date(date_w2_start, 4, format=format_normal, time="from 4.50pm") }})%%: This above weekly briefing will be followed by a F2F session to help those who are stuck in the iP due to technical difficulties. To attend that help session, be in {{ lecture_venue }} at least by 4.50pm.


</box>
<p/>

{{ embed_topic("../../admin/weeklySchedule.md#before-attempting-tasks", "Admin " + icon_embedding + " Weekly Schedule → Extract", "3", status="expanded") }}
<p/>


<box type="info" seamless>

**Week 2 Canvas quiz will open by week 1 Wednesday** (earlier than the normal opening time of Friday 4pm).

</box>
<p/>

