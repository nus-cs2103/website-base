<div id="additional">

%%Given below are some module _admin info_ to read around this time:%%

<panel type="danger" header="**Admin {{icon_embedding }} Using this website [essential info]** {{ glyphicon_star }}" expandable>
  <include src="../../admin/usingThisWebsite.md#essential"/>
</panel>
<panel type="info" header="**Admin {{icon_embedding }} Using this website [more info]** {{ glyphicon_star }}{{ glyphicon_star }}{{ glyphicon_star }}" expandable>
  <include src="../../admin/usingThisWebsite.md#more"/>
</panel>
<panel type="warning" header="**Admin {{icon_embedding }} Weekly schedule** {{ glyphicon_star }}{{ glyphicon_star }}" expandable>
  <include src="../../admin/weeklySchedule.md#main"/>
</panel>
<panel type="success" header="**Admin {{icon_embedding }} Module overview** {{ glyphicon_star }}{{ glyphicon_star }}{{ glyphicon_star }}{{ glyphicon_star }}" expandable>
  <include src="../../admin/moduleOverview.md#main"/>
</panel><p/>

</div>

{% import "common/macros.njk" as macros with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read with context %}

{{ macros.show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week1, is_flat=false ) }}

