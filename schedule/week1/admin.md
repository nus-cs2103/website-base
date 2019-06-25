{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(1, "admin") }}

<div id="additional">

%%Admin info relevant to the week's will appear in this tab.%%

<panel type="danger" header="**Admin {{icon_embedding }} Using this website [essential info]** :glyphicon-star:" expandable>
  <include src="../../admin/usingThisWebsite.md#essential"/>
</panel>
<panel type="info" header="**Admin {{icon_embedding }} Using this website [more info]** :glyphicon-star::glyphicon-star::glyphicon-star:" expandable>
  <include src="../../admin/usingThisWebsite.md#more"/>
</panel>
<panel type="warning" header="**Admin {{icon_embedding }} Weekly schedule** :glyphicon-star::glyphicon-star:" expandable>
  <include src="../../admin/weeklySchedule.md#main"/>
</panel>
<panel type="success" header="**Admin {{icon_embedding }} Module overview** :glyphicon-star::glyphicon-star::glyphicon-star::glyphicon-star:" expandable>
  <include src="../../admin/moduleOverview.md#main"/>
</panel><p/>

</div>

{% import "common/macros.njk" as macros with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read with context %}

{{ macros.show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week1, is_flat=false ) }}

